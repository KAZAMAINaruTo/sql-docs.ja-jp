---
title: "sys.column_encryption_keys (TRANSACT-SQL) |Microsoft ドキュメント"
ms.custom: 
ms.date: 10/28/2015
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-data-warehouse
ms.service: 
ms.component: system-catalog-views
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
applies_to:
- Azure SQL Database
- SQL Server 2016 Preview
f1_keywords:
- sys.column_encryption_keys
- column_encryption_keys_TSQL
- sys.column_encryption_keys_TSQL
- column_encryption_keys
dev_langs: TSQL
helpviewer_keywords: sys.column_encryption_keys catalog view
ms.assetid: 43980dd8-b9b1-4869-a304-2c183ae8977d
caps.latest.revision: "9"
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 7d8514e22680c96e33e99c60318181b5d2daeba2
ms.sourcegitcommit: 9fbe5403e902eb996bab0b1285cdade281c1cb16
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/27/2017
---
# <a name="syscolumnencryptionkeys--transact-sql"></a>sys.column_encryption_keys (TRANSACT-SQL)
[!INCLUDE[tsql-appliesto-ss2016-xxxx-asdw-xxx-md](../../includes/tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md)]

  作成された列暗号化キー (CEKs) に関する情報を返します、 [CREATE COLUMN ENCRYPTION KEY](../../t-sql/statements/create-column-encryption-key-transact-sql.md)ステートメントです。 各行には、CEK を表します。  
  
|列名|データ型|Description|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|CMK の名前。|  
|**column_encryption_key_id**|**int**|CEK の ID です。|  
|**create_date**|**datetime**|CEK が作成された日付。|  
|**modify_date**|**datetime**|CEK の最終変更日。|  
  
## <a name="permissions"></a>Permissions  
 必要があります、 **VIEW ANY COLUMN ENCRYPTION KEY**権限です。  
  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] 詳細については、「 [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [CREATE COLUMN ENCRYPTION KEY (Transact-SQL)](../../t-sql/statements/create-column-encryption-key-transact-sql.md)   
 [ALTER COLUMN ENCRYPTION KEY &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/statements/alter-column-encryption-key-transact-sql.md)   
 [列暗号化キー &#40; を削除します。TRANSACT-SQL と #41 です。](../../t-sql/statements/drop-column-encryption-key-transact-sql.md)   
 [CREATE COLUMN MASTER KEY (Transact-SQL)](../../t-sql/statements/create-column-master-key-transact-sql.md)   
 [セキュリティ カタログ ビュー &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/security-catalog-views-transact-sql.md)   
 [Always Encrypted &#40;データベース エンジン&#41;](../../relational-databases/security/encryption/always-encrypted-database-engine.md)   
 [sys.column_encryption_key_values &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-column-encryption-key-values-transact-sql.md)  
  
  
