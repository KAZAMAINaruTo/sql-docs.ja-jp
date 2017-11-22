---
title: "Enabled プロパティ (ServerNetworkProtocolIpAddress クラス) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: wmi
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: reference
apiname: Enabled Property (ServerNetworkProtocolIpAddress Class)
apilocation: sqlmgmproviderxpsp2up.mof
apitype: MOFDef
helpviewer_keywords: Enabled property
ms.assetid: 870fd4d0-6c77-462a-b480-d42eb044b2e7
caps.latest.revision: "14"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 755178e6e89d380bc1ad6d38b755a9d6194cbfe5
ms.sourcegitcommit: 66bef6981f613b454db465e190b489031c4fb8d3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2017
---
# <a name="enabled-property-servernetworkprotocolipaddress-class"></a>Enabled プロパティ (ServerNetworkProtocolIpAddress クラス)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]IP アドレスが有効になっているかどうかを示すブール型プロパティを取得します。  
  
## <a name="syntax"></a>構文  
  
```  
  
object.Enabled [= value]  
```  
  
## <a name="parts"></a>要素  
 *オブジェクト*  
 A [ServerNetworkProtocolIPAdress クラス](../../../relational-databases/wmi-provider-configuration-classes/servernetworkprotocolipaddress-class/servernetworkprotocolipaddress-class.md)のインスタンス上のネットワーク プロトコルの IP アドレスを表すオブジェクト[!INCLUDE[msCoName](../../../includes/msconame-md.md)][!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)]です。  
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値  
 IP アドレスが有効になっているかどうかを指定するブール値: **true** IP アドレスが有効になっている場合または**false** IP アドレスが無効になっている場合。  
  
## <a name="see-also"></a>参照  
 [サーバー ネットワーク プロトコルとネットワーク ライブラリの構成](http://msdn.microsoft.com/library/ms177485\(v=sql.100\).aspx)  
  
  
