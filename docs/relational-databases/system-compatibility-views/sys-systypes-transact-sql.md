---
title: sys.systypes (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.systypes_TSQL
- systypes_TSQL
- sys.systypes
- systypes
dev_langs:
- TSQL
helpviewer_keywords:
- sys.systypes compatibility view
- systypes system table
ms.assetid: 1b0b1d0c-5f7b-470b-bd52-8bfa922d7889
author: rothja
ms.author: jroth
manager: craigg
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 4acf3466615548e9c88b7743c48e39d3915f9c8d
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47602691"
---
# <a name="syssystypes-transact-sql"></a>sys.systypes (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  データベースで定義されている、システムから提供されているデータ型およびユーザー定義データ型ごとに 1 行のデータを返します。  
  
> [!IMPORTANT]  
>  [!INCLUDE[ssnoteCompView](../../includes/ssnotecompview-md.md)]  
  
|列名|データ型|説明|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|データ型の名前です。|  
|**xtype**|**tinyint**|物理記憶型です。|  
|**status**|**tinyint**|[!INCLUDE[ssInternalOnly](../../includes/ssinternalonly-md.md)]|  
|**xusertype**|**smallint**|拡張ユーザー タイプです。 データ型の数が 32,767 を超える場合は、オーバーフローが発生するか NULL が返されます。|  
|**length**|**smallint**|データ型の物理的な長さです。|  
|**xprec**|**tinyint**|サーバーが使用する内部の有効桁数です。 クエリでは使用されません。|  
|**xscale**|**tinyint**|サーバーが使用する内部の小数点以下桁数です。 クエリでは使用されません。|  
|**tdefault**|**int**|このデータ型の整合性チェックを行うストアド プロシージャの ID です。|  
|**domain**|**int**|このデータ型の整合性チェックを行うストアド プロシージャの ID です。|  
|**uid**|**smallint**|型の所有者のスキーマ ID です。<br /><br /> [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] の前のバージョンからアップグレードしたデータベースの場合、スキーマ ID は所有者のユーザー ID と同じです。<br /><br /> **\*\* 重要な\* \*** 場合は、次のいずれかを使用する[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]、DDL ステートメントを使用する必要がある、 [sys.types](../../relational-databases/system-catalog-views/sys-types-transact-sql.md)カタログ ビューの代わりに**sys.systypes**します。<br /><br /> ALTER AUTHORIZATION ON TYPE<br /><br /> CREATE TYPE<br /><br /> ユーザーとロールの数が 32,767 を超える場合は、オーバーフローが発生するか NULL が返されます。|  
|**reserved**|**smallint**|[!INCLUDE[ssInternalOnly](../../includes/ssinternalonly-md.md)]|  
|**collationid**|**int**|文字が基づいている場合**collationid**現在のデータベースの照合順序の id は、それ以外の場合は NULL。|  
|**usertype**|**smallint**|ユーザー型の ID です。 データ型の数が 32,767 を超える場合は、オーバーフローが発生するか NULL が返されます。|  
|**variable**|**bit**|可変長データ型です。<br /><br /> 1 = True<br /><br /> 0 = False|  
|**allownulls**|**bit**|既定で NULL 値を許容するかどうかを示します。 使用して null 値許容属性が指定されている場合この既定値がオーバーライドされる[CREATE TABLE](../../t-sql/statements/create-table-transact-sql.md)または[ALTER TABLE](../../t-sql/statements/alter-table-transact-sql.md)します。|  
|**type**|**tinyint**|物理記憶データ型です。|  
|**printfmt**|**varchar(255)**|[!INCLUDE[ssInternalOnly](../../includes/ssinternalonly-md.md)]|  
|**prec**|**smallint**|このデータ型の有効桁数です。<br /><br /> -1 = **xml**または大きな値の型。|  
|**scale**|**tinyint**|このデータ型の有効桁数に基づく小数点以下桁数です。<br /><br /> NULL = データ型は数値型以外です。|  
|**collation**|**sysname**|文字が基づいている場合は**照合順序**現在のデータベースの照合順序は、それ以外の場合は NULL です。|  
  
## <a name="see-also"></a>参照  
 [互換性ビュー &#40;TRANSACT-SQL&#41;](~/relational-databases/system-compatibility-views/system-compatibility-views-transact-sql.md)   
 [システム ビューへのシステム テーブルのマッピング&#40;TRANSACT-SQL&#41;](../../relational-databases/system-tables/mapping-system-tables-to-system-views-transact-sql.md)  
  
  
