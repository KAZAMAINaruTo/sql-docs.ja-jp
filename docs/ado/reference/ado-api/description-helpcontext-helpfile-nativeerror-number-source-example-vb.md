---
title: "エラー オブジェクトのプロパティの例 (VB) |Microsoft ドキュメント"
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
- Number property [ADO], Visual Basic example
- Source property [ADO], Visual Basic example
- NativeError property [ADO], Visual Basic example
- Description property [ADO], Visual Basic example
- HelpFile property [ADO], Visual Basic example
- SQLState property [ADO], Visual Basic example
- HelpContext property [ADO], Visual Basic example
ms.assetid: 5c728458-d85c-497c-afcf-2cfa36c3342a
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 43385a04975c36109c420d3137c205bd184b121f
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>説明、HelpContext、HelpFile、以下、数、ソース、および SQLState のプロパティの例 (VB)
この例は、によってエラーが発生し、トラップ、表示、[説明](../../../ado/reference/ado-api/description-property.md)、 [HelpContext](../../../ado/reference/ado-api/helpcontext-helpfile-properties.md)、 [HelpFile](../../../ado/reference/ado-api/helpcontext-helpfile-properties.md)、[以下](../../../ado/reference/ado-api/nativeerror-property-ado.md)、 [数](../../../ado/reference/ado-api/number-property-ado.md)、[ソース](../../../ado/reference/ado-api/source-property-ado-error.md)、および[SQLState](../../../ado/reference/ado-api/sqlstate-property.md)結果のプロパティ[エラー](../../../ado/reference/ado-api/error-object.md)オブジェクト。  
  
```  
'BeginDescriptionVB  
Public Sub Main()  
  
    Dim Cnxn As ADODB.Connection  
    Dim Err As ADODB.Error  
    Dim strError As String  
  
    On Error GoTo ErrorHandler  
  
    ' Intentionally trigger an error  
    Set Cnxn = New ADODB.Connection  
    Cnxn.Open "nothing"  
  
    Set Cnxn = Nothing  
    Exit Sub  
  
ErrorHandler:  
  
    ' Enumerate Errors collection and display  
    ' properties of each Error object  
    For Each Err In Cnxn.Errors  
        strError = "Error #" & Err.Number & vbCr & _  
            "   " & Err.Description & vbCr & _  
            "   (Source: " & Err.Source & ")" & vbCr & _  
            "   (SQL State: " & Err.SQLState & ")" & vbCr & _  
            "   (NativeError: " & Err.NativeError & ")" & vbCr  
        If Err.HelpFile = "" Then  
            strError = strError & "   No Help file available"  
        Else  
            strError = strError & _  
               "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _  
               "   (HelpContext: " & Err.HelpContext & ")" & _  
               vbCr & vbCr  
        End If  
  
        Debug.Print strError  
    Next  
  
    Resume Next  
End Sub  
'EndDescriptionVB  
```  
  
## <a name="see-also"></a>参照  
 [Description プロパティ](../../../ado/reference/ado-api/description-property.md)   
 [Error オブジェクト](../../../ado/reference/ado-api/error-object.md)   
 [HelpContext、HelpFile プロパティ](../../../ado/reference/ado-api/helpcontext-helpfile-properties.md)   
 [HelpContext、HelpFile プロパティ](../../../ado/reference/ado-api/helpcontext-helpfile-properties.md)   
 [以下のプロパティ (ADO)](../../../ado/reference/ado-api/nativeerror-property-ado.md)   
 [Number プロパティ (ADO)](../../../ado/reference/ado-api/number-property-ado.md)   
 [Source プロパティ (ADO エラー)](../../../ado/reference/ado-api/source-property-ado-error.md)   
 [SQLState プロパティ](../../../ado/reference/ado-api/sqlstate-property.md)

