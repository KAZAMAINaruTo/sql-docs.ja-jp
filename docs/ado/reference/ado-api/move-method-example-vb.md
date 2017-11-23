---
title: "メソッドの例 (VB) の移動 |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: reference
ms.technology: drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: VB
helpviewer_keywords: Move method [ADO], Visual Basic example
ms.assetid: 55eb797a-0205-40d2-a797-55b216d1d3bb
caps.latest.revision: "10"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: e9486a181dd283ea481594515214c6028b283c8a
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2017
---
# <a name="move-method-example-vb"></a>メソッドの例 (VB) を移動します。
この例では、[移動](../../../ado/reference/ado-api/move-method-ado.md)ユーザー入力に基づいてレコード ポインターを配置する方法です。  
  
```  
'BeginMoveVB  
  
    'To integrate this code  
    'replace the data source and initial catalog values  
    'in the connection string  
  
Public Sub Main()  
    On Error GoTo ErrorHandler  
  
    ' connection and recordset variables  
    Dim rstAuthors As ADODB.Recordset  
    Dim Cnxn As ADODB.Connection  
    Dim strCnxn As String  
    Dim strSQLAuthors As String  
     ' record variables  
    Dim varBookmark As Variant  
    Dim strCommand As String  
    Dim lngMove As Long  
  
    ' Open connection  
    Set Cnxn = New ADODB.Connection  
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _  
        "Initial Catalog='Pubs';Integrated Security='SSPI';"  
    Cnxn.Open strCnxn  
  
    ' Open recordset from Authors table  
    Set rstAuthors = New ADODB.Recordset  
    rstAuthors.CursorLocation = adUseClient  
    ' Use client cursor to allow use of AbsolutePosition property  
    strSQLAuthors = "SELECT au_id, au_fname, au_lname, city, state FROM Authors ORDER BY au_lname"  
    rstAuthors.Open strSQLAuthors, strCnxn, adOpenStatic, adLockOptimistic, adCmdText  
  
    rstAuthors.MoveFirst  
  
    Do  
        ' Display information about current record and  
        ' ask how many records to move  
  
        strCommand = InputBox( _  
            "Record " & rstAuthors.AbsolutePosition & _  
            " of " & rstAuthors.RecordCount & vbCr & _  
            "Author: " & rstAuthors!au_fname & _  
            " " & rstAuthors!au_lname & vbCr & _  
            "Location: " & rstAuthors!city & _  
            ", " & rstAuthors!State & vbCr & vbCr & _  
            "Enter number of records to Move " & _  
            "(positive or negative).")  
  
          ' this is for exiting the loop  
        'lngMove = CLng(strCommand)  
  
        lngMove = CLng(Val(strCommand))  
        If lngMove = 0 Then  
            MsgBox "You either entered a non-number or canceled the input box. Exit the application."  
            Exit Do  
        End If  
  
        ' Store bookmark in case the Move goes too far  
        ' forward or backward  
        varBookmark = rstAuthors.Bookmark  
  
        ' Move method requires parameter of data type Long  
        rstAuthors.Move lngMove  
  
        ' Trap for BOF or EOF  
        If rstAuthors.BOF Then  
            MsgBox "Too far backward! Returning to current record."  
            rstAuthors.Bookmark = varBookmark  
        End If  
        If rstAuthors.EOF Then  
            MsgBox "Too far forward!  Returning to current record."  
            rstAuthors.Bookmark = varBookmark  
        End If  
    Loop  
  
    ' clean up  
    rstAuthors.Close  
    Cnxn.Close  
    Set rstAuthors = Nothing  
    Set Cnxn = Nothing  
    Exit Sub  
  
ErrorHandler:  
    ' clean up  
    If Not rstAuthors Is Nothing Then  
        If rstAuthors.State = adStateOpen Then rstAuthors.Close  
    End If  
    Set rstAuthors = Nothing  
  
    If Not Cnxn Is Nothing Then  
        If Cnxn.State = adStateOpen Then Cnxn.Close  
    End If  
    Set Cnxn = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
'EndMoveVB  
```  
  
## <a name="see-also"></a>参照  
 [Move メソッド (ADO)](../../../ado/reference/ado-api/move-method-ado.md)   
 [Recordset オブジェクト (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)
