---
title: 更新 (DMX) |Microsoft ドキュメント
ms.custom: ''
ms.date: 03/02/2016
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: ''
ms.component: data-mining
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- UPDATE
dev_langs:
- DMX
helpviewer_keywords:
- NODE_CAPTION column
- mining models [Analysis Services], content changes
- modifying mining model content
- UPDATE statement [SQL Server], DMX
ms.assetid: 8a2b0942-c490-410c-b1cf-ff2e0fd8e24b
caps.latest.revision: 36
author: Minewiskan
ms.author: owend
manager: erikre
ms.openlocfilehash: c8b479dc74fe63a9eff4245be64a9eef5429101c
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
---
# <a name="update-dmx"></a>UPDATE (DMX)
[!INCLUDE[ssas-appliesto-sqlas](../includes/ssas-appliesto-sqlas.md)]

  変更、 **NODE_CAPTION**データ マイニング モデル内の列です。  
  
## <a name="syntax"></a>構文  
  
```  
  
UPDATE <model>.CONTENT  
SET NODE_CAPTION='new caption'  
[WHERE <condition expression>]  
```  
  
## <a name="arguments"></a>引数  
 *model*  
 モデル識別子です。  
  
 *新しいキャプション*  
 新しい名前を表す文字列、 **NODE_CAPTION**列です。  
  
 *条件式*  
 省略可。 列のリストから返される値を制限する条件です。  
  
## <a name="examples"></a>使用例  
 次の例で、**更新**ステートメントは、既定の名前を変更`Cluster 1`、クラスターの`001`、わかりやすい名前に`Likely Customers`です。  
  
```  
UPDATE [TM Clustering].CONTENT  
SET NODE_CAPTION= 'Likely Customers'  
WHERE NODE_UNIQUE_NAME = '001'  
```  
  
## <a name="see-also"></a>参照  
 [データ マイニング拡張機能&#40;DMX&#41;データ定義ステートメント](../dmx/dmx-statements-data-definition.md)   
 [データ マイニング拡張機能&#40;DMX&#41;データ操作ステートメント](../dmx/dmx-statements-data-manipulation.md)   
 [データ マイニング拡張機能 (&) #40";"DMX"&"#41;ステートメント リファレンス](../dmx/data-mining-extensions-dmx-statements.md)  
  
  
