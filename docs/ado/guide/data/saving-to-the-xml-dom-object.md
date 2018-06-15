---
title: XML DOM オブジェクトへの保存 |Microsoft ドキュメント
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- XML DOM object [ADO], saving to
ms.assetid: 4d20fd28-aaf8-4232-83ce-f9d1e5f93dae
caps.latest.revision: 3
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 82c9c8a04669d360362f68d8c1b0a524d954efa0
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "35272531"
---
# <a name="saving-to-the-xml-dom-object"></a>XML DOM オブジェクトへの保存
Visual Basic コードを次に示すように、MSXML の DOM オブジェクトのインスタンスを XML 形式のレコード セットを保存できます。  
  
```  
Dim xDOM As New MSXML.DOMDocument  
Dim rsXML As New ADODB.Recordset  
Dim sSQL As String, sConn As String  
  
sSQL = "SELECT customerid, companyname, contactname FROM customers"  
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _  
        "\Common Files\System\msadc\samples\NWind.mdb"  
rsXML.Open sSQL, sConn  
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree.  
...  
```  
  
## <a name="see-also"></a>参照  
 [レコードを XML 形式で保持する](../../../ado/guide/data/persisting-records-in-xml-format.md)
