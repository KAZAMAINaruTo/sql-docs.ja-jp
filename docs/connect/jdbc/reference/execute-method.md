---
title: execute メソッド () |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerPreparedStatement.execute ()
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: fa96d0f8-101b-422f-a767-405be9a5f74f
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 76b495fc9d583ea93b32d6625a836fcd84faca47
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47731190"
---
# <a name="execute-method-"></a>execute () メソッド
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  [SQLServerPreparedStatement](../../../connect/jdbc/reference/sqlserverpreparedstatement-class.md) オブジェクトの SQL ステートメントを実行します。すべての種類の SQL ステートメントを実行することができます。  
  
## <a name="syntax"></a>構文  
  
```  
  
public boolean execute()  
```  
  
## <a name="return-value"></a>戻り値  
 **true**ステートメントは結果セットを返す場合。 **false**場合は、更新数またはない結果が返されます。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Remarks  
 この execute メソッドは、java.sql.PreparedStatement インターフェイスの execute メソッドで規定されています。  
  
## <a name="see-also"></a>参照  
 [execute メソッド &#40;SQLServerPreparedStatement&#41;](../../../connect/jdbc/reference/execute-method-sqlserverpreparedstatement.md)   
 [SQLServerPreparedStatement のメンバー](../../../connect/jdbc/reference/sqlserverpreparedstatement-members.md)   
 [SQLServerPreparedStatement クラス](../../../connect/jdbc/reference/sqlserverpreparedstatement-class.md)  
  
  
