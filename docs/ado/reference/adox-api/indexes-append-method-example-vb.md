---
title: インデックスの追加メソッドの例 (VB) |Microsoft ドキュメント
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: ado
ms.technology:
- drivers
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
dev_langs:
- VB
helpviewer_keywords:
- Append method [ADOX]
ms.assetid: 50f87e27-1bf9-427c-9b1d-704a672434d2
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 4abb71f0e2f51fa200e3005bd532b91aefaeae79
ms.sourcegitcommit: bb044a48a6af9b9d8edb178dc8c8bd5658b9ff68
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2018
---
# <a name="indexes-append-method-example-vb"></a>インデックスの追加メソッドの例 (VB)
次のコードでは、新しいインデックスを作成する方法を示します。 テーブル内の 2 つの列にインデックスがあります。  
  
```  
Attribute VB_Name = "IndexesAppend"  
Option Explicit  
  
' BeginCreateIndexVB  
Sub Main()  
    On Error GoTo CreateIndexError  
  
    Dim tbl As New Table  
    Dim idx As New ADOX.Index  
    Dim cat As New ADOX.Catalog  
  
    'Open the catalog.  
    cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _  
        "Data Source='Northwind.mdb';"  
  
    ' Define the table and append it to the catalog.  
    tbl.Name = "MyTable"  
    tbl.Columns.Append "Column1", adInteger  
    tbl.Columns.Append "Column2", adInteger  
    tbl.Columns.Append "Column3", adVarWChar, 50  
    cat.Tables.Append tbl  
    Debug.Print "Table 'MyTable' is added."  
  
    ' Define a multi-column index.  
    idx.Name = "multicolidx"  
    idx.Columns.Append "Column1"  
    idx.Columns.Append "Column2"  
  
    ' Append the index to the table.  
    tbl.Indexes.Append idx  
    Debug.Print "The index is appended to table 'MyTable'."  
  
    'Delete the table as this is a demonstration.  
    cat.Tables.Delete tbl.Name  
    Debug.Print "Table 'MyTable' is deleted."  
  
    'Clean up.  
    Set cat.ActiveConnection = Nothing  
    Set cat = Nothing  
    Set tbl = Nothing  
    Set idx = Nothing  
    Exit Sub  
  
CreateIndexError:  
    Set cat = Nothing  
    Set tbl = Nothing  
    Set idx = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
' EndCreateIndexVB  
```  
  
## <a name="see-also"></a>参照  
 [Append メソッド (ADOX インデックス)](../../../ado/reference/adox-api/append-method-adox-indexes.md)   
 [Index オブジェクト (ADOX)](../../../ado/reference/adox-api/index-object-adox.md)   
 [Indexes コレクション (ADOX)](../../../ado/reference/adox-api/indexes-collection-adox.md)
