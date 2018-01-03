---
title: "トランザクション (ADO) を制御する |Microsoft ドキュメント"
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
helpviewer_keywords: transactions [ADO]
ms.assetid: 189240e8-3ffa-4024-81a9-c6cb5d17eee0
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 4770d802ea309f449d01bd2f83912b248c950c05
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2017
---
# <a name="controlling-transactions-ado"></a>トランザクション (ADO) を制御します。
ADO のヘルプへの接続内のトランザクション処理をサポートする、 **BeginTrans**、 **CommitTrans**、および**RollbackTrans**のメソッド、 **接続**オブジェクト。 次の単純なコード スニペットは、ADO のトランザクション処理を実装する一般的なという概念を示しています。  
  
```  
Const DS = "MySqlServer"  
Const DB = "Northwind"  
Const DP = "SQLOLEDB"  
  
Dim oConn As ADODB.Connection  
Dim oRs As ADODB.Recordset  
Dim sConn As String  
  
sConn = "Provider=" & DP & _  
          ";Data Source=" & DS & _  
          ";Initial Catalog=" & DB & _  
          ";Integrated Security=SSPI;"  
  
sSQL = "SELECT ProductID, ProductName FROM Products"  
  
Set oConn = New ADODB.Connection  
oConn.Open sConn  
  
' Create and Open the Recordset object.  
Set oRs = New ADODB.Recordset  
oRs.Open sSQL, oConn, adOpenStatic, adLockOptimistic, adCmdText  
  
If oRs.RecordCount > 1 Then  
  
    oRs.MoveFirst  
    Id1 = oRs("ProductID")  
    Name1 = oRs("ProductName")  
    oRs.MoveNext  
    Id2 = oRs("ProductID")  
    Name2 = oRs("ProductName")  
  
    q = "Switch ID's of " & Name1 & " and " & Name2 & "?"  
    If MsgBox(q, vbYesNo) = vbYes Then  
        oRs.MoveFirst  
        oRs("ProductName") = Name2  
        oRs.Update  
  
        oRs.MoveNext  
        oRs("ProductName") = Name1  
        oRs.Update  
  
        If MsgBox("Save changes?", vbYesNo) = vbYes Then  
  
        Else  
  
        End If  
    End If  
  
End If  
  
oRs.Close  
oConn.Close  
```  
  
 ここでトランザクション処理は、ことを確認して、操作の 1 つの単位として 2 つのレコードが更新に交換またはまったく変更されていない 2 つの製品名であることに使用されます。  
  
 トランザクション処理の詳細な説明を参照してください[更新およびデータの永続化](../../../ado/guide/data/updating-and-persisting-data.md)です。
