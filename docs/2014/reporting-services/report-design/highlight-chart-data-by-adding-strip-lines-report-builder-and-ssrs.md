---
title: ストリップ ラインの追加によるグラフのデータの強調表示 (レポート ビルダーおよび SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- reporting-services-native
ms.topic: conceptual
ms.assetid: addd6137-4b6e-4e88-a7e8-9600fcd1ccce
author: maggiesMSFT
ms.author: maggies
manager: craigg
ms.openlocfilehash: 6a0318d041a43e96246931015ef35edaf7fd74a2
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48162872"
---
# <a name="highlight-chart-data-by-adding-strip-lines-report-builder-and-ssrs"></a>ストリップ ラインの追加によるグラフのデータの強調表示 (レポート ビルダーおよび SSRS)
  ストリップ ライン (ストリップ) は、一定の間隔またはカスタムの間隔でグラフの背景を網掛け表示にする、横方向または縦方向の帯です。 ストリップ ラインを使用すると、次のことが可能になります。  
  
-   グラフ上の個々の値を調べるために見やすくする。 一定の間隔でストリップ ラインを指定すると、グラフを読む際にデータ ポイントを区別しやすくなります。  
  
-   一定の間隔の日付を強調する。 たとえば、売上レポートでは、ストリップ ラインを使用して週末のデータ ポイントを識別することができます。  
  
-   特定のキー範囲を強調する。 上記の例を使用すると、1 本のストリップ ラインを使用して、売上高が最も高い範囲 (80 ～ 100 ドル) を強調できます。  
  
 ストリップ ラインは、図形グラフや極座標グラフには適用できません。  
  
> [!NOTE]  
>  [!INCLUDE[ssRBRDDup](../../includes/ssrbrddup-md.md)]  
  
### <a name="to-display-interlaced-strip-lines-at-regular-intervals-on-a-chart"></a>インターレース ストリップ ラインを一定間隔でグラフに表示するには  
  
1.  横方向のストリップ ラインを表示するには、グラフの縦軸を右クリックし、 **[縦軸のプロパティ]** をクリックします。  
  
     縦方向のストリップ ラインを表示するには、グラフの横軸を右クリックし、 **[横軸のプロパティ]** をクリックします。  
  
2.  **[インターレースを使用する]** チェック ボックスをオンにします。 グラフにグレーのストリップ ラインが表示されます。  
  
3.  (省略可) 隣接する **[色]** ボックスの一覧を使用して、ストリップ ラインの色を指定します。  
  
### <a name="to-display-interlaced-strip-lines-at-custom-intervals-on-a-chart"></a>インターレース ストリップ ラインをカスタムの間隔でグラフに表示するには  
  
1.  横方向のストリップ ラインを表示するには、グラフの縦軸を右クリックし、 **[縦軸のプロパティ]** をクリックします。  
  
     縦方向のストリップ ラインを表示するには、グラフの横軸を右クリックし、 **[横軸のプロパティ]** をクリックします。  
  
     軸のプロパティが [プロパティ] ウィンドウに表示されます。  
  
2.  [プロパティ] ウィンドウの **[外観]** セクションで、StripLines プロパティのコレクションの編集ボタン ([...]) をクリックし、 **ChartStripLine コレクション エディター**を開きます。  
  
3.  **[追加]** をクリックし、新しいストリップ ラインをコレクションに追加します。  
  
4.  StripWidth をクリックして、レポート上のストリップ ラインの幅 (インチ単位) を指定します。 日付や時刻を強調する場合は、StripWidthType をクリックし、期間を選択します。  
  
5.  Interval を表す値または式を入力し、ストリップ ラインが繰り返される間隔を指定します。  たとえば、間隔に 10 を指定し、ストリップ ラインの幅が 5 である場合、ストリップ ラインは、値が 0 ～ 5、15 ～ 20、30 ～ 35 などの場所に表示されます。  
  
> [!NOTE]  
>  既定では、Interval は Auto に設定されます。つまり、グラフでは、カスタム ストリップ ラインの間隔が計算されません。 グラフでは、間隔値が設定されている場合のみ、ストリップ ラインの間隔が計算されます。  
  
## <a name="see-also"></a>関連項目  
 [グラフの軸ラベルの書式設定 (レポート ビルダーおよび SSRS)](formatting-axis-labels-on-a-chart-report-builder-and-ssrs.md)   
 [グラフの書式設定 (レポート ビルダーおよび SSRS)](formatting-a-chart-report-builder-and-ssrs.md)   
 [移動平均をグラフに追加&#40;レポート ビルダーおよび SSRS&#41;](add-a-moving-average-to-a-chart-report-builder-and-ssrs.md)  
  
  
