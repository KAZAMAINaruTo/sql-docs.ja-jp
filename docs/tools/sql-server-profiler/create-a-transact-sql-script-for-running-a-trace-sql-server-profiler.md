---
title: "トレース (SQL Server Profiler) を実行するための TRANSACT-SQL スクリプトを作成 |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: sql-non-specified
ms.service: 
ms.component: sql-server-profiler
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- traces [SQL Server], running
- scripts [SQL Server], traces
ms.assetid: 6b0e2519-998d-40d5-b8ba-5e6a773f91a6
caps.latest.revision: "25"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 312b81b1ac9dd733d81259972b8dd443861923c1
ms.sourcegitcommit: b2d8a2d95ffbb6f2f98692d7760cc5523151f99d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2017
---
# <a name="create-a-transact-sql-script-for-running-a-trace-sql-server-profiler"></a>トレースを実行するための Transact-SQL スクリプトの作成 (SQL Server Profiler)
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]このトピックを使用して、既存のトレース ファイルまたはテーブルから TRANSACT-SQL スクリプトを作成する方法について説明[!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)]です。  
  
### <a name="to-create-a-transact-sql-script-to-run-a-trace"></a>トレースを実行するための Transact-SQL スクリプトを作成するには  
  
1.  トレース ファイルまたはトレース テーブルを開きます。 詳細については、「[トレース ファイルを開く &#40;SQL Server Profiler&#41;](../../tools/sql-server-profiler/open-a-trace-file-sql-server-profiler.md)」または「[トレース テーブルを開く &#40;SQL Server Profiler&#41;](../../tools/sql-server-profiler/open-a-trace-table-sql-server-profiler.md)」を参照してください。  
  
2.  **[ファイル]** メニューで **[エクスポート]**、**[トレース定義のスクリプト]** の順にポイントし、トレースするサーバーに対応するバージョンをクリックします。  
  
3.  **[名前を付けて保存]** ダイアログ ボックスで、スクリプト ファイルの名前を入力し、 **[保存]**をクリックします。  
  
## <a name="see-also"></a>参照  
 [SQL Server プロファイラーのテンプレートと権限](../../tools/sql-server-profiler/sql-server-profiler-templates-and-permissions.md)   
 [SQL Server Profiler](../../tools/sql-server-profiler/sql-server-profiler.md)  
  
  
