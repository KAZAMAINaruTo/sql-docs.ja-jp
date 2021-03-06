---
title: データ マイニング デザイナー |Microsoft ドキュメント
ms.date: 05/01/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: data-mining
ms.topic: conceptual
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 25eea114d105ec445e91b5bebbbe74e1d0f846f3
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2018
ms.locfileid: "34014359"
---
# <a name="data-mining-designer"></a>データ マイニング デザイナー
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  データ マイニング デザイナーは、[!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] のマイニング モデルを操作するための主要な環境です。 データ マイニング デザイナーにアクセスするには、既存のマイニング構造を選択するか、またはデータ マイニング ウィザードを使用して新しいマイニング構造とマイニング モデルを作成します。 データ マイニング デザイナーを使用すると、次の作業を実行できます。  
  
-   最初にデータ マイニング ウィザードで作成したマイニング構造とマイニング モデルを変更する。  
  
-   既存のマイニング構造に基づいて新しいモデルを作成する。  
  
-   マイニング モデルをトレーニングして参照する。  
  
-   精度チャートを使用してモデルを比較する。  
  
-   マイニング モデルに基づいて予測クエリを作成する。  
  
## <a name="mining-structure-tab"></a>[マイニング構造] タブ  
 **[マイニング構造]** タブを使用すると、列を追加したり、既存のマイニング構造のプロパティを変更したりできます。 次のタスクおよびトピックでは、マイニング構造の操作の詳細について説明します。  
  
 [マイニング構造 &#40;Analysis Services - データ マイニング&#41;](../../analysis-services/data-mining/mining-structures-analysis-services-data-mining.md)  
  
 [マイニング構造のタスクと操作方法](../../analysis-services/data-mining/mining-structure-tasks-and-how-tos.md)  
  
## <a name="mining-models-tab"></a>[マイニング モデル] タブ  
 **[マイニング モデル]** タブを使用すると、既存のマイニング モデルを管理したり、新しいモデルを作成したりできます。 マイニング モデルは、常に既存のマイニング構造に基づきます。  
  
 **[マイニング モデル]** タブでは、アルゴリズムの種類の変更、モデル構造に関連付けられている列の追加または削除、アルゴリズム固有の列プロパティの調整、マイニング モデル列の使用法の指定、およびマイニング モデルに関連付けられているアルゴリズム パラメーターの調整を行うことができます。 また、マイニング構造は、選択したモデルまたは関連付けられているすべてのモデルと共に処理することもできます。  
  
 マイニング モデルの操作の詳細については、次のトピックを参照してください。  
  
 [マイニング モデルと #40 です。Analysis Services - データ マイニング & #41;](../../analysis-services/data-mining/mining-models-analysis-services-data-mining.md)  
  
 [マイニング モデル タスクと操作方法](../../analysis-services/data-mining/mining-model-tasks-and-how-tos.md)  
  
## <a name="mining-model-viewer-tab"></a>[マイニング モデル ビューアー] タブ  
 **[マイニング モデル ビューアー]** タブは、マイニング モデルを視覚的に調べるときに使用します。 各マイニング モデルは、そのモデルに固有のコンテンツを表示するカスタム ビューアーに関連付けられています。 また、コンテンツ ビューアーを使用して、マイニング モデル コンテンツを表示することもできます。  
  
 データ マイニング ビューアーを使用したマイニング モデルの調査の詳細については、次のトピックを参照してください。  
  
 [データ マイニング モデル ビューアー](../../analysis-services/data-mining/data-mining-model-viewers.md)  
  
 [マイニング モデル ビューアーのタスクと操作方法](../../analysis-services/data-mining/mining-model-viewer-tasks-and-how-tos.md)  
  
## <a name="mining-accuracy-chart-tab"></a>[マイニング精度チャート] タブ  
 **[マイニング精度チャート]** タブは、1 つのマイニング モデルの予測精度をテストしたり、マイニング構造内に含まれている複数のマイニング モデルの効果を比較したりするときに使用します。 このタブには、データのフィルター選択、マイニング モデルの選択、およびリフト チャート、利益チャート、または分類マトリックスへの結果の表示を行うためのツールがあります。  
  
 マイニング モデルのテストおよび検証の詳細については、次のトピックを参照してください。  
  
 [テストおよび検証 &#40;データ マイニング&#41;](../../analysis-services/data-mining/testing-and-validation-data-mining.md)  
  
 [テストおよび検証タスクと操作方法 &#40;データ マイニング&#41;](../../analysis-services/data-mining/testing-and-validation-tasks-and-how-tos-data-mining.md)  
  
## <a name="mining-model-prediction-tab"></a>[マイニング モデル予測] タブ  
 **[マイニング モデル予測]** タブには予測クエリ ビルダーがあり、これを使用してデータ マイニング拡張機能 (DMX) の予測クエリを作成できます。 このタブには、マイニング モデルと入力テーブルの指定、入力テーブル内の列へのマイニング モデル内の列のマッピング、クエリへの機能の追加、および各列の条件の指定を行うためのツールがあります。  
  
 クエリをデザインした後、タブのさまざまなビューを使用して、クエリの結果を表示したり、クエリを手動で変更したりできます。 また、クエリの結果をデータベースのテーブルに保存することもできます。  
  
 データ マイニング クエリの作成の詳細については、次のトピックを参照してください。  
  
 [データ マイニング クエリ](../../analysis-services/data-mining/data-mining-queries.md)  
  
 [データ マイニング クエリ タスクと操作方法](../../analysis-services/data-mining/data-mining-query-tasks-and-how-tos.md)  
  
## <a name="see-also"></a>参照  
 [データ マイニング ソリューション](../../analysis-services/data-mining/data-mining-solutions.md)  
  
  
