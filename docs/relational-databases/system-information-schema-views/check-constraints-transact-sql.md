---
title: CHECK_CONSTRAINTS (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- CHECK_CONSTRAINTS
- CHECK_CONSTRAINTS_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- CHECK_CONSTRAINTS view
- INFORMATION_SCHEMA.CHECK_CONSTRAINTS view
ms.assetid: e9577fd2-c349-4dff-874c-9e57d2e5a3ec
author: CarlRabeler
ms.author: carlrab
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 6f5a9cdb939f9d093350c5dcbac75c82653d56f3
ms.sourcegitcommit: 4183dc18999ad243c40c907ce736f0b7b7f98235
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "43082845"
---
# <a name="checkconstraints-transact-sql"></a>CHECK_CONSTRAINTS (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  現在のデータベース内の CHECK 制約ごとに 1 行のデータを返します。 この情報スキーマ ビューは、現在のユーザーが権限を所有しているオブジェクトについての情報を返します。  
  
 これらのビューから情報を取得するには、完全修飾名を指定 **INFORMATION_SCHEMA. * * * view_name*します。  
  
|列名|データ型|説明|  
|-----------------|---------------|-----------------|  
|**CONSTRAINT_CATALOG**|**nvarchar(** 128 **)**|制約修飾子|  
|**CONSTRAINT_SCHEMA**|**nvarchar(** 128 **)**|制約が属するスキーマの名前<br /><br /> **\*\* 重要な\* \*** オブジェクトのスキーマを決定 INFORMATION_SCHEMA ビューを使用しないでください。 オブジェクトのスキーマを調べる唯一の信頼性のある方法は、sys.objects カタログ ビューに対するクエリを実行する方法です。|  
|**CONSTRAINT_NAME**|**sysname**|制約名。|  
|**CHECK_CLAUSE**|**nvarchar (** 4000 **)**|[!INCLUDE[tsql](../../includes/tsql-md.md)] 定義ステートメントの実際のテキスト|  
  
## <a name="see-also"></a>参照  
 [システム ビュー &#40;TRANSACT-SQL&#41;](http://msdn.microsoft.com/library/35a6161d-7f43-4e00-bcd3-3091f2015e90)   
 [情報スキーマ ビュー &#40;TRANSACT-SQL&#41;](~/relational-databases/system-information-schema-views/system-information-schema-views-transact-sql.md)   
 [sys.check_constraints &#40;TRANSACT-SQL&#41;](../../relational-databases/system-catalog-views/sys-check-constraints-transact-sql.md)   
 [sys.objects &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md)  
  
  
