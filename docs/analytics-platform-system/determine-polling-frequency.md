---
title: ポーリング間隔 - Analytics Platform System の決定 |Microsoft Docs
description: この記事では、Analytics Platform System appliance のアラートのポーリング頻度を決定する方法について説明します。
author: mzaman1
manager: craigg
ms.prod: sql
ms.technology: data-warehouse
ms.topic: conceptual
ms.date: 04/17/2018
ms.author: murshedz
ms.reviewer: martinle
ms.openlocfilehash: 6b838766e7a6d6bfb9a68bb832cd7a8feb3c9960
ms.sourcegitcommit: 50b60ea99551b688caf0aa2d897029b95e5c01f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2018
ms.locfileid: "51696620"
---
# <a name="determine-polling-frequency"></a>ポーリング間隔を決定します。
この記事では、Analytics Platform System appliance のアラートのポーリング頻度を決定する方法について説明します。  
  
## <a name="to-determine-the-polling-frequency"></a>ポーリングの頻度を決定するには  
PDW は現在サポートしていないためプロアクティブな通知アラートが発生したときに、監視ソリューションを継続的に、アプライアンスの Dll をポーリングする必要があります。  内部的には、PDW では、さまざまな間隔で、コンポーネントをポーリングします。  
  
-   クラスター-60 秒  
  
-   ハートビート-60 秒  
  
-   他のすべてコンポーネント – 5 分  
  
-   3 秒のパフォーマンス カウンター  
  
System Center によっても使用される一般的なアラートをポーリングする間隔は**15 分ごと**します。  当然ながら、多くの場合より小さいかを照会することが 6 時間未満ごとにポーリングをお勧めできません。  
  
頻繁にポーリングすることが許容されるが、煩雑になります。 ポーリング頻度が高すぎる、 [sys.dm_pdw_nodes_exec_requests](https://msdn.microsoft.com/library/ms177648(v=sql11).aspx) DMV。  ポーリング頻度が高すぎることが困難なユーザー クエリのパフォーマンスを診断する際に問題が非表示をすばやくロールします。  
  
## <a name="see-also"></a>参照  
<!-- MISSING LINKS [Common Metadata Query Examples &#40;SQL Server PDW&#41;](../sqlpdw/common-metadata-query-examples-sql-server-pdw.md)  -->  
[アプライアンスの監視&#40;Analytics Platform System&#41;](appliance-monitoring.md)  
  
