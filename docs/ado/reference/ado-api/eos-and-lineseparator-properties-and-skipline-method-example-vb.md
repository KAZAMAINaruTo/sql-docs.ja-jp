---
title: "EOS と LineSeparator プロパティ SkipLine メソッドの例 (VB) |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology: drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: VB
helpviewer_keywords:
- LineSeparator property [ADO], Visual Basic example
- Skipline method [ADO], Visual Basic example
- EOS property [ADO], Visual Basic example
ms.assetid: 77ce3042-9ebc-44ba-a4ff-0f1b1fd4a9c4
caps.latest.revision: "10"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: dd0c9f048aee7463e54f9de7e55a246f3e72ee62
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2017
---
# <a name="eos-and-lineseparator-properties-and-skipline-method-example-vb"></a>EOS と LineSeparator プロパティ SkipLine メソッドの例 (VB)
この例では、一度に 1 つのテキスト ストリームの行を操作する方法を示します。 既定キャリッジ リターン/ライン フィードからの行区切り記号を変更した場合の効果 (**adCRLF**) 単に改行を (**adLF**) またはキャリッジ リターン (**adCR**) が表示されます。  
  
```  
'BeginSkipLineVB  
Private Sub cmdSkipLine_Click()  
    On Error GoTo ErrorHandler  
  
    'Declare variables  
    Dim i As Integer  
    Dim objStream As Stream  
    Dim strLine, strChar As String  
  
    'Instantiate and open stream  
    Set objStream = New Stream  
    objStream.Open  
  
    'Set line separator to line feed  
    objStream.LineSeparator = adLF  
  
    'Load text content of list box into stream  
    'One line at a time  
    For i = 0 To (List1.ListCount - 1)  
        objStream.WriteText List1.List(i), adWriteLine  
    Next  
  
    'Display the entire stream  
    Debug.Print "Whole Stream:"  
    objStream.Position = 0  
    Debug.Print objStream.ReadText  
  
    'Display the first line  
    Debug.Print "First Line:"  
    objStream.Position = 0  
    strLine = objStream.ReadText(adReadLine)  
    Debug.Print strLine  
    Debug.Print "Line length: " + Str(Len(strLine))  
  
    'Skip a line, then display another line  
    Debug.Print "Third Line:"  
    objStream.SkipLine  
    strLine = objStream.ReadText(adReadLine)  
    Debug.Print strLine  
    Debug.Print "Line length: " + Str(Len(strLine))  
  
    'Switch line separator to carriage return  
    'All items from list will be considered one line  
    'Assuming no CRs have been loaded into stream  
    Debug.Print "Whole Stream/First Line:"  
    objStream.Position = 0  
    objStream.LineSeparator = adCR  
    strLine = objStream.ReadText(adReadLine)  
    Debug.Print strLine  
    Debug.Print "Line length: " + Str(Len(strLine))  
    Debug.Print "Stream size: " + Str(objStream.Size)  
  
    'Use EOS to Determine End of Stream  
    Debug.Print "Character by character:"  
    objStream.Position = 0  
    Do Until objStream.EOS  
        strChar = objStream.ReadText(1)  
        Debug.Print strChar  
    Loop  
  
    ' clean up  
    objStream.Close  
    Set objStream = Nothing  
    Exit Sub  
  
ErrorHandler:  
    ' clean up  
    If Not objStream Is Nothing Then  
        If objStream.State = adStateOpen Then objStream.Close  
    End If  
    Set objStream = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
  
Private Sub Form_Load()  
    List1.AddItem "This is the first line"  
    List1.AddItem "This is the second line"  
    List1.AddItem "This is the third line"  
End Sub  
'EndSkipLineVB  
```  
  
## <a name="see-also"></a>参照  
 [EOS プロパティ](../../../ado/reference/ado-api/eos-property.md)   
 [LineSeparator プロパティ (ADO)](../../../ado/reference/ado-api/lineseparator-property-ado.md)   
 [SkipLine メソッド](../../../ado/reference/ado-api/skipline-method.md)
