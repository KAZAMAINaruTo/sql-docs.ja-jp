---
title: fn_syscollector_get_execution_stats (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- fn_syscollector_get_execution_stats
- fn_syscollector_get_execution_stats_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- fn_syscollector_get_execution_stats function
ms.assetid: 793ad72c-a992-4a8d-8584-bcb6b3b476f1
author: rothja
ms.author: jroth
manager: craigg
ms.openlocfilehash: 91227f3f5d1ef6238b18064b4c978d238f85e4b2
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47811210"
---
# <a name="fnsyscollectorgetexecutionstats-transact-sql"></a>fn_syscollector_get_execution_stats (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  コレクション セットまたはパッケージに関する詳細な統計 (パッケージのデータ フロー タスクによってログ記録されたエラー行の数を含む) を返します。 データ フロー タスクは、[!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)]データを処理するコンポーネントです。 このデータはリレーショナル形式のため、行で構成される入力データセットと出力データセットが含まれます。  
  
 統計は、syscollector_execution_stats ビューのエントリから計算されます。  
  
 ![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>構文  
  
```  
  
fn_syscollector_get_execution_stats ( log_id )  
```  
  
## <a name="arguments"></a>引数  
 *log_id*  
 実行ログの一意なローカル識別子を指定します。 *log_id*は**int**します。  
  
## <a name="table-returned"></a>返されるテーブル  
  
|列名|データ型|説明|  
|-----------------|---------------|-----------------|  
|avg_row_count_in|**int**|パッケージのデータ フロー タスクが開始された行の平均数です。<br /><br /> 注: データ フロー タスクは、[!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)]データを処理するコンポーネントです。 このデータはリレーショナル形式のため、行で構成される入力データセットが含まれます。 これはタスクに入力された行数です。 このデータは、変換されてから、行で構成される結果セットとして出力されます。 データ フロー タスクでは、データを変換して行で構成される結果セットを出力します。 この出力はタスクが終了した行数です。|  
|min_row_count_in|**int**|パッケージのデータ フロー タスクが開始された行の最小数です。|  
|max_row_count_in|**int**|パッケージのデータ フロー タスクが開始された行の最大数です。|  
|avg_row_count_out|**int**|パッケージのデータ フロー タスクが終了した行の平均数です。|  
|min_row_count_out|**int**|パッケージのデータ フロー タスクが終了した行の最小数です。|  
|max_row_count_out|**int**|パッケージのデータ フロー タスクが終了した行の最大数です。|  
|avg_duration|**int**|パッケージのデータ フロー コンポーネントに費やされた時間の平均値です (ミリ秒)。|  
|min_duration|**int**|パッケージのデータ フロー コンポーネントに費やされた時間の最小値です (ミリ秒)。|  
|max_duration|**int**|パッケージのデータ フロー コンポーネントに費やされた時間の最大値です (ミリ秒)。|  
  
## <a name="permissions"></a>アクセス許可  
 SELECT 権限が必要**dc_operator**します。  
  
## <a name="see-also"></a>参照  
 [syscollector_execution_stats &#40;TRANSACT-SQL&#41;](../../relational-databases/system-catalog-views/syscollector-execution-stats-transact-sql.md)   
 [[データ コレクション]](../../relational-databases/data-collection/data-collection.md)  
  
  
