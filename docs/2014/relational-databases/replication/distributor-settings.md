---
title: ディストリビューターの設定 | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- replication
ms.topic: conceptual
f1_keywords:
- sql12.rep.monitor.DistributorSettings.f1
helpviewer_keywords:
- Distributor Settings dialog box
ms.assetid: 8276a521-bdd1-4783-bdb6-7ab43499c0ca
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: 3986ed6cd2b3fbe3bb6db22a68e62304d8dae318
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48131892"
---
# <a name="distributor-settings"></a>ディストリビューターの設定
  **[ディストリビューターの設定]** ダイアログ ボックスを使用すると、レプリケーション モニターの左ペインに追加されているディストリビューターの設定を変更できます。  
  
## <a name="options"></a>および  
 **[レプリケーション モニターが起動したときに自動的に接続する]**  
 レプリケーション モニターでディストリビューターに接続して状態情報を取得する場合に選択します。  
  
 **[接続]**  
 クリックすると、 **[サーバーへの接続]** ダイアログ ボックスが表示されます。 このダイアログ ボックスでは、レプリケーション モニターがディストリビューターに接続するときに使用する接続プロパティおよび資格情報を表示および変更できます。  
  
 **[このディストリビューターとパブリケーションのステータスを自動的に更新する]**  
 レプリケーション モニターでディストリビューターのステータスを自動的に更新する場合に選択します。 このオプションがオンの場合、レプリケーション モニターは、 **[更新頻度]** オプションにより設定されたポーリング間隔に基づき、状態情報についてディストリビューターをポーリングします。 レプリケーション モニターでの更新については、「 [Caching, Refresh, and Replication Monitor Performance](monitor/caching-refresh-and-replication-monitor-performance.md)」を参照してください。  
  
 **[更新頻度]**  
 レプリケーション モニターが状態についてディストリビューターをポーリングする間隔 (秒数) を入力します。 入力する値が小さいほど、ポーリングの発生頻度が高くなります。 多数のパブリッシャーを監視している場合は、ディストリビューターのパフォーマンスに影響する可能性があります。 システムをテストしながら適切な値を見つけてください。 **[更新頻度]** 設定は、レプリケーション モニターのいずれかの詳細ウィンドウで **[自動更新]** を選択している場合にも使用されます。  
  
 **[このディストリビューターのすべてのパブリッシャーを次のグループに表示する]**  
 一覧からパブリッシャー グループを選択します。 パブリッシャーは、左ペインでこのグループの下に表示されます。 グループはパブリッシャーを整理するもので、レプリケーションの動作には影響を与えません。  
  
 **[新しいグループ]**  
 クリックすると、新しいパブリッシャー グループを作成できます。 パブリッシャー グループを利用すると、レプリケーション モニター内でパブリッシャーを容易に整理できます。 グループは、データのレプリケーションや、レプリケーション トポロジ内のサーバー間のリレーションシップには影響を与えません。  
  
## <a name="see-also"></a>参照  
 [レプリケーション モニターの開始](monitor/start-the-replication-monitor.md)   
 [レプリケーションの監視](monitoring-replication.md)  
  
  
