---
title: getObjectInstance メソッド (SQLServerDataSourceObjectFactory) |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerDataSourceObjectFactory.getObjectInstance
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 0a1503e2-e991-4d70-a223-087fc63baf73
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: aab186f41d494e9bddf7885ddf7d9f7b3ff65972
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47849510"
---
# <a name="getobjectinstance-method-sqlserverdatasourceobjectfactory"></a>getObjectInstance メソッド (SQLServerDataSourceObjectFactory)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  指定したデータ ソース オブジェクトのインスタンスを取得します。  
  
## <a name="syntax"></a>構文  
  
```  
  
public java.lang.Object getObjectInstance(java.lang.Object ref,  
                                          javax.naming.Name name,  
                                          javax.naming.Context c,  
                                          java.util.Hashtable h)  
```  
  
#### <a name="parameters"></a>パラメーター  
 *ref*  
  
 **Object** 値。  
  
 *name*  
  
 オブジェクトの名前。  
  
 *c*  
  
 指定した名前に関連するコンテキストです。  
  
 *h*  
  
 オブジェクトの作成に使用する環境です。  
  
## <a name="return-value"></a>戻り値  
 **Object** 値。  
  
## <a name="exceptions"></a>例外  
 java.sql.SQLException  
  
## <a name="remarks"></a>Remarks  
 この getObjectInstance メソッドは、javax.naming.spi.ObjectFactory インターフェイスで getObjectInstance メソッドによって指定されます。  
  
## <a name="see-also"></a>参照  
 [SQLServerDataSourceObjectFactory のメソッド](../../../connect/jdbc/reference/sqlserverdatasourceobjectfactory-methods.md)   
 [SQLServerDataSourceObjectFactory のメンバー](../../../connect/jdbc/reference/sqlserverdatasourceobjectfactory-members.md)   
 [SQLServerDataSourceObjectFactory クラス](../../../connect/jdbc/reference/sqlserverdatasourceobjectfactory-class.md)  
  
  
