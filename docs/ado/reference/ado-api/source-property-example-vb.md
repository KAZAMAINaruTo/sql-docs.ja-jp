---
title: "ソースのプロパティの例 (VB) |Microsoft ドキュメント"
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
helpviewer_keywords: Source property [ADO], Visual Basic example
ms.assetid: 7c83eb01-71c7-4c5d-9778-6270471c8164
caps.latest.revision: "10"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 953cd75d0924ef2dafdcfda11e8e111411a533f9
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2017
---
# <a name="source-property-example-vb"></a>ソース プロパティの例 (VB)
この例で、[ソース](../../../ado/reference/ado-api/source-property-ado-recordset.md)を 3 つを開いてプロパティ[レコード セット](../../../ado/reference/ado-api/recordset-object-ado.md)オブジェクトが別のデータ ソースに基づきます。  
  
```  
'BeginSourceVB  
  
    'To integrate this code  
    'replace the data source and initial catalog values  
    'in the connection string  
  
Public Sub Main()  
    On Error GoTo ErrorHandler  
  
    Dim Cnxn As ADODB.Connection  
    Dim rstTitles As ADODB.Recordset  
    Dim rstPublishers As ADODB.Recordset  
    Dim rstPublishersDirect As ADODB.Recordset  
    Dim rstTitlesPublishers As ADODB.Recordset  
    Dim cmdSQL As ADODB.Command  
    Dim strCnxn As String  
    Dim strSQL As String  
  
    ' Open a connection  
    Set Cnxn = New ADODB.Connection  
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _  
        "Initial Catalog='Pubs';Integrated Security='SSPI';"  
    Cnxn.Open strCnxn  
  
    ' Open a recordset based on a command object  
    Set cmdSQL = New ADODB.Command  
    Set cmdSQL.ActiveConnection = Cnxn  
    strSQL = "Select title, type, pubdate FROM Titles ORDER BY title"  
    cmdSQL.CommandText = strSQL  
    Set rstTitles = cmdSQL.Execute()  
  
    ' Open a recordset based on a table  
    Set rstPublishers = New ADODB.Recordset  
    strSQL = "Publishers"  
    rstPublishers.Open strSQL, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable  
    'rstPublishers.Open strSQL, Cnxn, , , adCmdTable  
     ' the above two lines of code are identical  
  
    ' Open a recordset based on a table  
    Set rstPublishersDirect = New ADODB.Recordset  
    rstPublishersDirect.Open strSQL, strCnxn, , , adCmdTableDirect  
  
    ' Open a recordset based on an SQL string.  
    Set rstTitlesPublishers = New ADODB.Recordset  
    strSQL = "SELECT title_ID AS TitleID, title AS Title, " & _  
        "publishers.pub_id AS PubID, pub_name AS PubName " & _  
        "FROM publishers INNER JOIN Titles " & _  
        "ON publishers.pub_id = Titles.pub_id " & _  
        "ORDER BY Title"  
    rstTitlesPublishers.Open strSQL, strCnxn, , , adCmdText  
  
    ' Use the Source property to display the source of each recordset.  
    MsgBox "rstTitles source: " & vbCr & _  
        rstTitles.Source & vbCr & vbCr & _  
        "rstPublishers source: " & vbCr & _  
        rstPublishers.Source & vbCr & vbCr & _  
        "rstPublishersDirect source: " & vbCr & _  
        rstPublishersDirect.Source & vbCr & vbCr & _  
        "rstTitlesPublishers source: " & vbCr & _  
        rstTitlesPublishers.Source  
  
    ' clean up  
    rstTitles.Close  
    rstPublishers.Close  
    rstTitlesPublishers.Close  
    Cnxn.Close  
    Set rstTitles = Nothing  
    Set rstPublishers = Nothing  
    Set rstTitlesPublishers = Nothing  
    Set Cnxn = Nothing  
    Exit Sub  
  
ErrorHandler:  
    ' clean up  
    If Not rstTitles Is Nothing Then  
        If rstTitles.State = adStateOpen Then rstTitles.Close  
    End If  
    Set rstTitles = Nothing  
  
    If Not rstPublishers Is Nothing Then  
        If rstPublishers.State = adStateOpen Then rstPublishers.Close  
    End If  
    Set rstPublishers = Nothing  
  
    If Not rstTitlesPublishers Is Nothing Then  
        If rstTitlesPublishers.State = adStateOpen Then rstTitlesPublishers.Close  
    End If  
    Set rstTitlesPublishers = Nothing  
  
    If Not Cnxn Is Nothing Then  
        If Cnxn.State = adStateOpen Then Cnxn.Close  
    End If  
    Set Cnxn = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
End Sub  
'EndSourceVB  
```  
  
## <a name="see-also"></a>参照  
 [レコード セット オブジェクト (ADO)](../../../ado/reference/ado-api/recordset-object-ado.md)   
 [Source プロパティ (ADO Recordset)](../../../ado/reference/ado-api/source-property-ado-recordset.md)
