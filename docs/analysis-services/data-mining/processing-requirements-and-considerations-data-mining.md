---
title: 処理の要件および考慮事項 (データ マイニング) |Microsoft ドキュメント
ms.date: 05/08/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: data-mining
ms.topic: conceptual
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: d4228f5ae90f7fdd2510787b6fca6ad10f7302e4
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2018
ms.locfileid: "34016149"
---
# <a name="processing-requirements-and-considerations-data-mining"></a>処理の要件および注意事項 (データ マイニング)
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  このトピックでは、データ マイニング オブジェクトを処理するときに注意するいくつかの技術的な考慮事項について説明します。 処理について、および処理がデータ マイニングに適用される方法に関する一般情報については、「 [データ マイニング オブジェクトの処理](../../analysis-services/data-mining/processing-data-mining-objects.md)」を参照してください。  
  
 [リレーショナル ストアに対するクエリ](#bkmk_QueryReqs)  
  
 [マイニング構造の処理](#bkmk_ProcessStructures)  
  
 [マイニング モデルの処理](#bkmk_ProcessModels)  
  
##  <a name="bkmk_QueryReqs"></a> 処理中のリレーショナル ストアに対するクエリ  
 データ マイニングでの処理には、ソース データのクエリ、生の統計情報の特定、およびモデル定義とアルゴリズムを使用したマイニング モデルのトレーニングの 3 つの段階があります。  
  
 [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] サーバーは、生データを提供するデータベースに対してクエリを実行します。 そのデータベースは、 [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] 以前のバージョンの SQL Server データベース エンジンのインスタンスである場合もあります。 データ マイニング構造の処理時には、ソース内のデータがマイニング構造に転送され、圧縮形式でディスク上に新たに保存されます。 データ ソース内のすべての列が処理されるとは限りません。バインドの定義に従って、マイニング構造に含まれる列だけが処理されます。  
  
 [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] はそのデータを使用して、すべてのデータおよび離散化列のインデックスと、連続列のための別のインデックスを作成します。 入れ子になったテーブルごとに、インデックスを作成するためのクエリが実行され、入れ子になったテーブルとケース テーブルの各ペアの関係を処理するための追加のクエリが生成されます。 このように複数のクエリが作成されるのは、特殊な内部多次元データ ストアを処理するためです。 [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] によってリレーショナル ストアに送信されるクエリの数を制限するには、サーバー プロパティの **DatabaseConnectionPoolMax**を設定します。 詳細については、「 [OLAP のプロパティ](../../analysis-services/server-properties/olap-properties.md)」を参照してください。  
  
 モデルの処理時に、モデルは、データ ソースからデータを再度読み取るのではなく、マイニング構造からデータの概要を取得します。 サーバーは、作成されたキューブと、キャッシュされたインデックス データとケース データを使用して、モデルのトレーニングを行うための独立したスレッドを作成します。  
  
 各エディションの詳細については[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]並列モデル処理をサポートするを参照してください[SQL Server 2012 の各エディションでサポートされる機能](http://go.microsoft.com/fwlink/?linkid=232473)(http://go.microsoft.com/fwlink/?linkid=232473)です。  
  
##  <a name="bkmk_ProcessStructures"></a> マイニング構造の処理  
 マイニング構造は、すべての依存モデルと一緒に処理することも、個別に処理することもできます。 処理に時間がかかると予想されるモデルがあり、その操作を保留する場合、モデルとは別にマイニング構造を処理すると便利です。  
  
 詳細については、「 [マイニング構造の処理](../../analysis-services/data-mining/process-a-mining-structure.md)」を参照してください。  
  
 [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] ではマイニング構造キャッシュがローカルに保持されるので、ハード ディスク領域を節約する場合は注意してください。 つまり、すべてのトレーニング データがローカル ハード ディスクに書き込まれます。 データをキャッシュしない場合は、マイニング構造の <xref:Microsoft.AnalysisServices.MiningStructureCacheMode> プロパティを **ClearAfterProcessing**」を参照してください。 これにより、モデルを処理した後にキャッシュが破棄されます。また、マイニング構造のドリルスルーも無効になります。 詳細については、「[ドリルスルー クエリ &#40;データ マイニング&#41;](../../analysis-services/data-mining/drillthrough-queries-data-mining.md)」を参照してください。  
  
 また、キャッシュを消去すると、提示されたテスト セット (定義している場合) を使用できなくなり、テスト セット パーティションの定義も失われます。 提示されたテスト セットの詳細については、「 [トレーニング データ セットとテスト データ セット](../../analysis-services/data-mining/training-and-testing-data-sets.md)」を参照してください。  
  
##  <a name="bkmk_ProcessModels"></a> マイニング モデルの処理  
 関連付けられているマイニング構造とは別にマイニング モデルを処理することも、マイニング構造に基づくすべてのモデルをマイニング構造と共に処理することもできます。  
  
 詳細については、「 [マイニング モデルの処理](../../analysis-services/data-mining/process-a-mining-model.md)」を参照してください。  
  
 ただし、 [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] および [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)]では、マイニング構造と共に処理するマイニング モデルを複数選択することができません。 処理するモデルを制御する必要がある場合は、モデルを個別に選択するか、XMLA または DMX を使用してモデルを順番に処理する必要があります。  
  
## <a name="when-reprocessing-is-required"></a>再処理が必要な場合  
 モデルの操作を開始する前に、定義する [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] モデルを処理する必要があります。 また、マイニング モデル構造の変更、トレーニング データの更新、既存のマイニング モデルの変更、または構造への新しいマイニング モデルの追加を行った場合は、必ずマイニング モデルを再処理する必要があります。  
  
 マイニング モデルは、以下のシナリオでも処理されます。  
  
 **プロジェクトの配置**: 通常は、プロジェクトの設定と現在の状態に応じて、プロジェクトの配置時にそのプロジェクトのマイニング モデルが完全処理されます。  
  
 配置を開始すると、以前に処理されたバージョンが [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] サーバーに存在して構造的に変更されていない場合を除き、処理が自動的に開始されます。 プロジェクトを配置するには、ドロップダウン リストから **[ソリューションの配置]** を選択するか、または F5 キーを押します。 次の操作を実行できます。  
  
 マイニング モデルの配置方法を制御する [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] の配置プロパティの設定方法の詳細については、「 [データ マイニング ソリューションの配置](../../analysis-services/data-mining/deployment-of-data-mining-solutions.md)」を参照してください。  
  
 **マイニング モデルの移動**: EXPORT コマンドを使用してマイニング モデルを移動する場合、モデルの定義だけがエクスポートされます。この定義には、モデルにデータを提供する予定のマイニング構造の名前が含まれます。  
  
 EXPORT コマンドと IMPORT コマンドを使用するシナリオとその再処理の要件を次に示します。  
  
-   移動先のインスタンスにマイニング構造が存在し、そのマイニング構造が未処理の状態にある場合。  
  
     構造とモデルの両方を再処理する必要があります。  
  
-   移動先のインスタンスにマイニング構造が存在し、そのマイニング構造が処理済みで、 マイニング モデルのみがエクスポートされた場合。  
  
     モデルは処理せずに使用できます。  
  
-   WITH DEENDENCIES キーワードを使用してマイニング構造の定義もエクスポートされた場合。  
  
     構造とモデルの両方を再処理する必要があります。  
  
 詳細については、「 [データ マイニング オブジェクトのエクスポートおよびインポート](../../analysis-services/data-mining/export-and-import-data-mining-objects.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [マイニング構造と #40 です。Analysis Services - データ マイニング & #41;](../../analysis-services/data-mining/mining-structures-analysis-services-data-mining.md)   
 [マイニング構造と #40 です。Analysis Services - データ マイニング & #41;](../../analysis-services/data-mining/mining-structures-analysis-services-data-mining.md)   
 [多次元モデルの処理 &#40;Analysis Services&#41;](../../analysis-services/multidimensional-models/processing-a-multidimensional-model-analysis-services.md)  
  
  
