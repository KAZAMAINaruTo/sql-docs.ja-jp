---
title: "getPacketSize メソッド (SQLServerDataSource) |Microsoft ドキュメント"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- SQLServerDataSource.getPacketSize
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: b2e9f01a-2e51-47e5-90bf-43c62d1be74d
caps.latest.revision: 14
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 9788a804580b88d9f65f9df8e176d883863aa1a0
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="getpacketsize-method-sqlserverdatasource"></a>getPacketSize メソッド (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  通信するために使用される現在のネットワーク パケット サイズを返します[!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)]、バイト単位で指定します。  
  
## <a name="syntax"></a>構文  
  
```  
  
public int getPacketSize()  
```  
  
## <a name="return-value"></a>戻り値  
 **Int**現在のネットワーク パケット サイズを含む値です。  
  
## <a name="remarks"></a>解説  
 PacketSize プロパティが設定されていない場合、getPacketSize メソッドは、既定値の 8000 を返します。  
  
## <a name="see-also"></a>参照  
 [SQLServerDataSource のメンバー](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource クラス](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  

