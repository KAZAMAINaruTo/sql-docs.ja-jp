---
title: MSpeer_request (TRANSACT-SQL) |Microsoft ドキュメント
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: ''
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- MSpeer_request
- MSpeer_request_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSpeer_request system table
ms.assetid: ed048c46-7a2f-4ad0-bc7c-c2d65e83b4fb
caps.latest.revision: 21
author: edmacauley
ms.author: edmaca
manager: craigg
ms.openlocfilehash: 00873769699c217a3efc2b20458e3e8b594f68af
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
ms.locfileid: "33005729"
---
# <a name="mspeerrequest-transact-sql"></a>MSpeer_request (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  MSpeer_request テーブルはピア ツー ピア レプリケーションで使用され、任意のパブリケーションに対する状態要求を記録します。 このテーブルは、パブリケーション データベース内に保存されます。  
  
|列名|データ型|Description|  
|-----------------|---------------|-----------------|  
|id|**int**|要求を識別する値|  
|パブリケーション (publication)|**sysname**|状態要求が開始されたパブリケーションの名前|  
|sent_date|**datetime**|状態要求が開始された日付と時刻|  
|description|**nvarchar (4000)**|個々の状態要求の識別に使用できるユーザー定義情報|  
  
## <a name="see-also"></a>参照  
 [レプリケーション テーブル &#40; です。TRANSACT-SQL と &#41; です。](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [レプリケーション ビュー &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
