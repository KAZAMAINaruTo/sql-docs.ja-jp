---
title: getClientInfo () メソッド |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: b06a5ced-b760-4c78-b17e-854ce95a1a5c
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: a89f2afa50b0ee1b83e72c05bf675d49dac662ca
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47757770"
---
# <a name="getclientinfo-method-"></a>getClientInfo () メソッド
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  JDBC ドライバーでサポートされている、各クライアント情報のプロパティの名前と現在の値を含む一覧を取得します。  
  
## <a name="syntax"></a>構文  
  
```  
  
public java.util.Properties getClientInfo()  
```  
  
## <a name="return-value"></a>戻り値  
 ドライバーでサポートされている、各クライアント情報のプロパティの名前と現在の値を含む Properties オブジェクトです。  
  
## <a name="exceptions"></a>例外  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Remarks  
 この getClientInfo メソッドは、java.sql.Connection インターフェイスの getClientInfo メソッドによって指定されます。  
  
 [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] ではクライアント情報のプロパティをサポートしていません。 その結果、このメソッドは、空のプロパティ オブジェクトを返します。  
  
 同様に、アプリケーションは、[SQLServerDatabaseMetaData](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md) クラスの [getClientInfoProperties](../../../connect/jdbc/reference/getclientinfoproperties-method-sqlserverdatabasemetadata.md) メソッドを使用して、ドライバーがサポートするクライアント情報プロパティの一覧を取得できます。 [getClientInfoProperties](../../../connect/jdbc/reference/getclientinfoproperties-method-sqlserverdatabasemetadata.md) メソッドでは、空の結果セットが返されます。  
  
## <a name="see-also"></a>参照  
 [getClientInfo メソッド &#40;SQLServerConnection&#41;](../../../connect/jdbc/reference/getclientinfo-method-sqlserverconnection.md)   
 [SQLServerConnection のメンバー](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection クラス](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
