---
title: "ビューの追加メソッドの例 (VB) |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- Append method [ADOX]
ms.assetid: b5b4c082-ac29-4f49-a8b8-e21b554c9b0d
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 6c4672189074eb65e4220bcdbeacbd471c4d7911
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="views-append-method-example-vb"></a>ビューの追加メソッドの例 (VB)
次のコードを使用する方法を示しています、[コマンド](../../../ado/reference/ado-api/command-object-ado.md)オブジェクトおよび[ビュー](../../../ado/reference/adox-api/views-collection-adox.md)コレクション[Append](../../../ado/reference/adox-api/append-method-adox-views.md)メソッドを基になるデータ ソースに新しいビューを作成します。  
  
```  
' BeginCreateViewVB  
Sub Main()  
    On Error GoTo CreateViewError  
  
    Dim cmd As New ADODB.Command  
    Dim cat As New ADOX.Catalog  
  
    ' Open the Catalog  
    cat.ActiveConnection = _  
        "Provider='Microsoft.Jet.OLEDB.4.0';" & _  
        "Data Source='Northwind.mdb';"  
  
    ' Create the command representing the view.  
    cmd.CommandText = "Select * From Customers"  
  
    ' Create the new View  
    cat.Views.Append "AllCustomers", cmd  
  
    'Clean up  
    Set cat.ActiveConnection = Nothing  
    Set cat = Nothing  
    Set cmd = Nothing  
    Exit Sub  
  
CreateViewError:  
  
    Set cat = Nothing  
    Set cmd = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
' EndCreateViewVB  
```  
  
## <a name="see-also"></a>参照  
 [ActiveConnection プロパティ (ADOX)](../../../ado/reference/adox-api/activeconnection-property-adox.md)   
 [Append メソッド (ADOX ビュー)](../../../ado/reference/adox-api/append-method-adox-views.md)   
 [カタログ オブジェクト (ADOX)](../../../ado/reference/adox-api/catalog-object-adox.md)   
 [ビュー オブジェクト (ADOX)](../../../ado/reference/adox-api/view-object-adox.md)   
 [ビューのコレクション (ADOX)](../../../ado/reference/adox-api/views-collection-adox.md)

