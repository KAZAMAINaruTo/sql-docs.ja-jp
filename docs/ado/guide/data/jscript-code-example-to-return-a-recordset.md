---
title: "レコード セットを返す JScript コード例 |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- JScript
helpviewer_keywords:
- Recordset [ADO]
ms.assetid: 74aad8a6-06cc-4a2c-811a-d78f9b741d84
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 7c9c767413fefb4f35e2f3ac60ebcf52323efd2b
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/09/2018
---
# <a name="jscript-code-example-to-return-a-recordset"></a>JScript コード例をレコード セットを返す
## <a name="jscript-code-rsjs"></a>JScript コード (rs.js)  
  
```  
main();  
  
function main()  
{  
  DP = "SQLOLEDB";  
  DS = "MySQLServer";  
  DB = "NORTHWIND";  
  
  adOpenForwardOnly = 0;  
  adLockReadOnly = 1;  
  adCmdText = 1;  
  try   
  {  
    var objRs = new ActiveXObject("ADODB.Recordset");  
  }  
  catch (e)  
  {  
    alert("ADODB namespace not found.");  
    exit(0);  
  }  
  
  strConn =  "Provider="         +DP+  
            ";Initial Catalog="  +DB+  
            ";Data Source="      +DS+  
            ";Integrated Security=SSPI;"  
  strComm = "SELECT ProductID,ProductName,UnitPrice "+  
            "FROM Products " +   
            "WHERE CategoryID = 7"  // select Produce  
  
  objRs.open(strComm,   
             strConn,   
             adOpenForwardOnly,  
             adLockReadOnly,  
             adCmdText);  
  
  objRs.MoveFirst();  
  while (objRs.EOF != true)   
  {  
    alert(objRs("ProductID")+"\t"  
         +objRs("ProductName")+"\t"  
         +objRs("UnitPrice"));  
    objRs.MoveNext();  
  }  
  
  objRs.Close  
  objRs = null;  
}  
  
function alert(str)  
{  
  WScript.Echo(str);  
}  
```  
  
#### <a name="try-it"></a>試してみる  
  
1.  上記のコードをテキスト ファイルに保存します。 Rs.js としてファイルを保存します。  
  
2.  コマンド プロンプトを開き、JScript ファイル (rs.js) を保存したディレクトリに cd します。  
  
3.  型`CScript rs.js`コマンド プロンプトからです。
