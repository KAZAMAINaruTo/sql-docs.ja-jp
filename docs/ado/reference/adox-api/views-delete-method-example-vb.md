---
title: "ビューの削除の方法の例 (VB) |Microsoft ドキュメント"
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
- Delete method [ADOX]
ms.assetid: 17df2a83-4166-4df8-8c17-0a33aaac8582
caps.latest.revision: 9
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: d8990c77ac61b8c85ffe4d6d48cfcc80cdab77f6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="views-delete-method-example-vb"></a>ビューの削除の方法の例 (VB)
次のコードを使用する方法を示しています、[削除](../../../ado/reference/adox-api/delete-method-adox-collections.md)カタログからビューを削除する方法です。  
  
```  
' BeginDeleteViewVB  
Sub Main()  
    On Error GoTo DeleteViewError  
  
    Dim cat As New ADOX.Catalog  
  
    ' Open the catalog  
    cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _  
        "Data Source='Northwind.mdb';"  
  
    'Delete the View  
    cat.Views.Delete "AllCustomers"  
  
    'Clean up  
    Set cat.ActiveConnection = Nothing  
    Set cat = Nothing  
    Exit Sub  
  
DeleteViewError:  
    Set cat = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
' EndDeleteViewVB  
```  
  
## <a name="see-also"></a>参照  
 [Delete メソッド (ADOX コレクション)](../../../ado/reference/adox-api/delete-method-adox-collections.md)   
 [ビューのコレクション (ADOX)](../../../ado/reference/adox-api/views-collection-adox.md)

