---
title: sysdbmaintplan_databases (TRANSACT-SQL) |Microsoft ドキュメント
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.service: ''
ms.component: system-tables
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- sysdbmaintplan_databases
- sysdbmaintplan_databases_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysdbmaintplan_databases system table
ms.assetid: f8413a44-8fcc-4899-84f2-b4afe0f8ec08
caps.latest.revision: 21
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: b17f3d35b300c6da4e28ac3f23980d6d390422e2
ms.sourcegitcommit: 7a6df3fd5bea9282ecdeffa94d13ea1da6def80a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="sysdbmaintplandatabases-transact-sql"></a>sysdbmaintplan_databases (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  このテーブルはからアップグレードされたインスタンスの既存の情報を保持するために以前のバージョンの[!INCLUDE[msCoName](../../includes/msconame-md.md)][!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]です。 [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] およびそれ以降のバージョンでは、このテーブルの内容は変更しないでください。 次の表は、 **msdb**データベース。  
  
 [!INCLUDE[ssNoteDepNextAvoid](../../includes/ssnotedepnextavoid-md.md)]  
  
|列名|データ型|Description|  
|-----------------|---------------|-----------------|  
|**plan_id**|**一意識別子**|メンテナンス プランの ID|  
|**database_name**|**sysname**|このデータベース メンテナンス プランが関連付けられているデータベースの名前|  
  
  
