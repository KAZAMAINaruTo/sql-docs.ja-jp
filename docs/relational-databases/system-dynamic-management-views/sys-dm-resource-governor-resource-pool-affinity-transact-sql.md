---
title: sys.dm_resource_governor_resource_pool_affinity (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 08/09/2016
ms.prod: sql
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sys.dm_resource_governor_resource_pool_affinity_TSQL
- sys.dm_resource_governor_resource_pool_affinity
- dm_resource_governor_resource_pool_affinity
- dm_resource_governor_resource_pool_affinity_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- dm_resource_governor_resource_pool_affinity
- sys.dm_resource_governor_resource_pool_affinity
ms.assetid: a197ec19-a2ba-44f5-a4f2-3eee33ebd77d
caps.latest.revision: 9
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: b9142b5219a8f404ee81ebfb51460d451ff2096a
ms.sourcegitcommit: 7019ac41524bdf783ea2c129c17b54581951b515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/23/2018
---
# <a name="sysdmresourcegovernorresourcepoolaffinity-transact-sql"></a>sys.dm_resource_governor_resource_pool_affinity (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  リソース プール アフィニティを追跡します。  
  
 ![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)。  
  
|Colmn 名|データ型|Description|  
|----------------|---------------|-----------------|  
|Pool_id|**int**|リソース プールの ID。 NULL 値は許可されません。|  
|Processor_group|**smallint**|Windows の論理プロセッサ グループの ID。 NULL 値は許可されません。|  
|Scheduler_mask|**bigint**|このプールに関連付けられているスケジューラを表すバイナリ マスク。 NULL 値は許可されません。|  
  
## <a name="remarks"></a>解説  
 AUTO アフィニティで作成されたプールにはアフィニティがないので、このビューには表示されません。 詳細については、次を参照してください。、 [CREATE RESOURCE POOL &#40;TRANSACT-SQL&#41; ](../../t-sql/statements/create-resource-pool-transact-sql.md)と[ALTER RESOURCE POOL &#40;TRANSACT-SQL&#41; ](../../t-sql/statements/alter-resource-pool-transact-sql.md)ステートメントです。  
  
## <a name="see-also"></a>参照  
 [sys.dm_resource_governor_external_resource_pool_affinity &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-resource-governor-external-resource-pool-affinity-transact-sql.md)  
  
  
