---
title: recover メソッド (SQLServerXAResource) |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
apiname:
- SQLServerXAResource.recover
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 840ecfcf-0dd3-4b7b-976f-dc9a96cd1464
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 8ec96cd3f56b1710268ae951e39e98866fe1bd54
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MTE75
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47826820"
---
# <a name="recover-method-sqlserverxaresource"></a>recover メソッド (SQLServerXAResource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  準備されたトランザクション ブランチの一覧を、リソース マネージャーから取得します。  
  
## <a name="syntax"></a>構文  
  
```  
  
public javax.transaction.xa.Xid[] recover(int flags)  
```  
  
#### <a name="parameters"></a>パラメーター  
 *flags*  
  
 **Int**値は次のいずれかを取る値: XAResource.TMSTARTRSCAN または XAResource.TMENDRSCAN または XAResource.TMNOFLAGS XAResource.TMSTARTTRSCAN |XAResource.TMENDRSCAN します。  
  
## <a name="return-value"></a>戻り値  
 Xid オブジェクト。  
  
## <a name="exceptions"></a>例外  
 javax.transaction.xa.XAException  
  
## <a name="remarks"></a>Remarks  
 この recover メソッドは、javax.transaction.xa.XAResource インターフェイスの recover メソッドで規定されています。  
  
 場合、パラメーター**フラグ**XAResource.TMSTARTRSCAN または XAResource.TMSTARTRSCAN ではありません |XAResource.TMENDRSCAN、リカバリ スキャンは、進行状況でなければなりません。  
  
## <a name="see-also"></a>参照  
 [SQLServerXAResource のメソッド](../../../connect/jdbc/reference/sqlserverxaresource-methods.md)   
 [SQLServerXAResource のメンバー](../../../connect/jdbc/reference/sqlserverxaresource-members.md)   
 [SQLServerXAResource クラス](../../../connect/jdbc/reference/sqlserverxaresource-class.md)  
  
  
