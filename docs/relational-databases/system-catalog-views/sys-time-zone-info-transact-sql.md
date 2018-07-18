---
title: sys.time_zone_info (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/27/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.component: system-catalog-views
ms.reviewer: ''
ms.suite: sql
ms.technology: system-objects
ms.tgt_pltfrm: ''
ms.topic: language-reference
applies_to:
- Azure SQL Database
- SQL Data Warehouse
- SQL Server (starting with 2016)
f1_keywords:
- sys.time_zone_info
- sys.time_zone_info_TSQL
- time_zone_info
- time_zone_info_TSQL
helpviewer_keywords:
- sys.time_zone_info system table
ms.assetid: 3f51a9a4-75f8-4a11-9552-8bf6118b68da
caps.latest.revision: 7
author: edmacauley
ms.author: edmaca
manager: craigg
monikerRange: = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions
ms.openlocfilehash: 252def1ce861b926a6c8a990a3cbf10b22eb83f6
ms.sourcegitcommit: e77197ec6935e15e2260a7a44587e8054745d5c2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "37984924"
---
# <a name="systimezoneinfo-transact-sql"></a>sys.time_zone_info (TRANSACT-SQL)
[!INCLUDE[tsql-appliesto-ss2014-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md)]

  サポートされているタイム ゾーンに関する情報を返します。 コンピューターにインストールされているすべてのタイム ゾーンは、次のレジストリ ハイブに格納されます。  
`KEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Time Zones`。  
  
|列名|データ型|説明|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|Windows 標準の形式でタイム ゾーンの名前です。 たとえば、 **cen です。オーストラリア標準時**または**中央ヨーロピアン標準時**します。|  
|**current_utc_offset**|**nvarchar(12)**|現在の utc オフセットです。 たとえば、 **+01: 00**または **-07:00**します。|  
|**is_currently_dst**|**bit**|夏時間が現在監視している場合は true。|  
  
## <a name="see-also"></a>参照  
 [GETUTCDATE &#40;TRANSACT-SQL&#41;](../../t-sql/functions/getutcdate-transact-sql.md)   
 [AT TIME ZONE &#40;Transact-SQL&#41;](../../t-sql/queries/at-time-zone-transact-sql.md)   
 [日付と時刻のデータ型および関数 (Transact-SQL)](../../t-sql/functions/date-and-time-data-types-and-functions-transact-sql.md)   
 [サーバー全体の構成に関するカタログ ビュー &#40;TRANSACT-SQL&#41;](../../relational-databases/system-catalog-views/server-wide-configuration-catalog-views-transact-sql.md)  
