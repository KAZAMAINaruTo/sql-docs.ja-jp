---
title: Irow::getcolumns と ISequentialStream を使用して BLOB データのフェッチ |Microsoft ドキュメント
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: ''
ms.component: native-client-ole-db-rowsets
ms.reviewer: ''
ms.suite: sql
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- fetching BLOB data
- ISequentialStream interface
- GetColumns method
- BLOBs, fetching
ms.assetid: b57decda-b0c1-4ef6-8c81-491956de2890
caps.latest.revision: 29
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
monikerRange: '>= aps-pdw-2016 || = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: dc3e658b6cda86ff9783ae7a176ba7f0bf741117
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="fetching-blob-data-using-irowgetcolumns-and-isequentialstream"></a>IRow::GetColumns と ISequentialStream を使用した BLOB データのフェッチ
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

  次の関数は**irow::getcolumns**と**ISequentialStream**大きなデータをフェッチします。  
  
```  
void InitializeAndExecuteCommand()  
{  
    ULONG iidx;  
    WCHAR* wCmdString=OLESTR("SELECT * FROM MyTable");  
    // Do the initialization, create the session, and set command text.  
    hr = pICommandText->Execute(NULL, IID_IRow, NULL,   
                         &cNumRows,(IUnknown **)&pIRow)))  
    //Get 1 column at a time.  
    for(ULONG i=0; i < NoOfColumns; i++)  
      GetSequentialColumn(pIRow, iidx);  
    // Do the clean up.  
}  
HRESULT GetSequentialColumn(IRow* pUnkRow, ULONG iCol)  
{  
    HRESULT hr = NOERROR;  
    ULONG cbRead = 0;  
    ULONG cbTotal = 0;  
    ULONG cColumns = 0;  
    ULONG cReads = 0;  
    ISequentialStream* pIStream = NULL;  
    WCHAR* pBuffer[kMaxBuff]; //50 chars read by ISequentialStream::Read()  
    DBCOLUMNINFO* prgInfo;  
    OLECHAR* pColNames;  
    IColumnsInfo* pIColumnsInfo;  
    DBID columnid;  
    DBCOLUMNACCESS column;  
    hr = pUnkRow->QueryInterface(IID_IColumnsInfo,   
                            (void**) &pIColumnsInfo);  
    if(FAILED(hr))  
        goto CLEANUP;  
    hr = pIColumnsInfo->GetColumnInfo(&cColumns, &prgInfo, &pColNames);  
    // Get Column ID.  
    columnid = (prgInfo + (iCol))->columnid;  
    IUnknown* pUnkStream = NULL;  
    ZeroMemory(&column, sizeof(column));  
    column.columnid = prgInfo[iCol].columnid;  
    // Ask for Iunknown interface pointer.  
    column.wType = DBTYPE_IUNKNOWN;  
    column.pData = (LPVOID*) &pUnkStream;  
  
    hr = pUnkRow->GetColumns(1, &column);  
    // Get ISequentialStream from Iunknown pointer retrieved from  
    // GetColumns().  
    hr = pUnkStream->QueryInterface(IID_ISequentialStream,   
                                   (LPVOID*) &pIStream);  
    ZeroMemory(pBuffer, kMaxBuff * sizeof(WCHAR));  
    // Read 50 chars at a time until no more data.  
    do  
    {  
        hr = pIStream->Read(pBuffer, kMaxBuff, &cbRead);  
        cbTotal = cbTotal + cbRead;  
        // Process the data.  
    } while(cbRead > 0);  
  // Do the cleanup.  
    return hr;  
}  
```  
  
## <a name="see-also"></a>参照  
 [IRow を使用して BLOB データのフェッチ](http://msdn.microsoft.com/library/badbd6ac-20aa-4891-a14f-48d38e7f30de)  
  
  
