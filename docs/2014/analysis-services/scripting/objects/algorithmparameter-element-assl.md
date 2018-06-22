---
title: AlgorithmParameter 要素 (ASSL) |Microsoft ドキュメント
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
api_name:
- AlgorithmParameter Element
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- AlgorithmParameter
helpviewer_keywords:
- AlgorithmParameter element
ms.assetid: 73211495-065c-43c6-a486-be6044617263
caps.latest.revision: 35
author: Minewiskan
ms.author: owend
manager: mblythe
ms.openlocfilehash: 70e9e3619eb5f96ff2e64c87855b2bd33063aaf0
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36084875"
---
# <a name="algorithmparameter-element-assl"></a>AlgorithmParameter 要素 (ASSL)
  使用されるアルゴリズムのパラメーターを定義、 [MiningModel](miningmodel-element-assl.md)要素。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<AlgorithmParameters>  
   <AlgorithmParameter>  
      <Name>...</Name>  
      <Value>...</Value>  
   </AlgorithmParameter>  
</AlgorithmParameters>  
```  
  
## <a name="element-characteristics"></a>要素の特性  
  
|特性|説明|  
|--------------------|-----------------|  
|データ型と長さ|なし|  
|既定値|なし|  
|Cardinality|0-n : 省略可能な要素で、出現する場合は複数回の出現が可能です|  
  
## <a name="element-relationships"></a>要素の関係  
  
|リレーションシップ|要素|  
|------------------|-------------|  
|親要素|[AlgorithmParameters](../collections/algorithmparameters-element-assl.md)|  
|子要素|[名前](../properties/name-element-assl.md)、[値](../properties/value-element-assl.md)|  
  
## <a name="remarks"></a>コメント  
 `AlgorithmParameter` はマイニング モデル アルゴリズムのパラメーターです。 `AlgorithmParameter` では名前と値のペアとしてこのパラメーターを表します。 `AlgorithmParameter` で表すことのできる適用可能なパラメーターのセットは、アルゴリズムによって異なります。 特定のアルゴリズムのアルゴリズム パラメーターの詳細については、そのアルゴリズムに関するドキュメントを参照してください。  
  
 検証や表示の情報を含む使用可能なアルゴリズム パラメーターから取得できる、 [DMSCHEMA_MINING_SERVICE_PARAMETERS](../../schema-rowsets/data-mining/dmschema-mining-service-parameters-rowset.md)スキーマ行セット。  
  
 分析管理オブジェクト (AMO) オブジェクト モデルで対応する要素は<xref:Microsoft.AnalysisServices.AlgorithmParameter>します。  
  
## <a name="see-also"></a>参照  
 [MiningModel 要素&#40;ASSL&#41;](miningmodel-element-assl.md)   
 [Algorithm 要素&#40;ASSL&#41;](../properties/algorithm-element-assl.md)   
 [オブジェクト&#40;ASSL&#41;](objects-assl.md)  
  
  