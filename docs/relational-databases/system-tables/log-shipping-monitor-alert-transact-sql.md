---
title: log_shipping_monitor_alert (TRANSACT-SQL) |Microsoft ドキュメント
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- log_shipping_monitor_alert
- log_shipping_monitor_alert_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- log_shipping_monitor_alert system table
ms.assetid: 1c775e48-9898-4149-b9d1-04d465f23438
caps.latest.revision: 20
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: f6ffc93c6ef960880d7143cc03b72e55c570bac4
ms.sourcegitcommit: f1caaa156db2b16e817e0a3884394e7b30fb642f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2018
ms.locfileid: "33253652"
---
# <a name="logshippingmonitoralert-transact-sql"></a>log_shipping_monitor_alert (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  ログ配布に関する警告ジョブ ID を格納します。 次の表は、 **msdb**データベース。   
  
|列名|データ型|Description|  
|-----------------|---------------|-----------------|  
|**alert_job_id**|**uniqueidentifier**|[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]エージェント ジョブのログ配布警告ジョブ ID。|  
  
## <a name="see-also"></a>参照  
 [ログ配布 & #40; についてSQL Server & #41;](../../database-engine/log-shipping/about-log-shipping-sql-server.md)   
 [sp_add_log_shipping_alert_job &#40;TRANSACT-SQL&#41;](../../relational-databases/system-stored-procedures/sp-add-log-shipping-alert-job-transact-sql.md)   
 [sp_delete_log_shipping_alert_job &#40;TRANSACT-SQL&#41;](../../relational-databases/system-stored-procedures/sp-delete-log-shipping-alert-job-transact-sql.md)   
 [sp_help_log_shipping_alert_job &#40;TRANSACT-SQL&#41;](../../relational-databases/system-stored-procedures/sp-help-log-shipping-alert-job-transact-sql.md)   
 [システム テーブル &#40;TRANSACT-SQL&#41;](../../relational-databases/system-tables/system-tables-transact-sql.md)  
  
  
