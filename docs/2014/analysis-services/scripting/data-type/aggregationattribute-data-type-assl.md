---
title: AggregationAttribute データ型 (ASSL) |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.topic: reference
api_name:
- AggregationAttribute Data Type
api_location:
- http://schemas.microsoft.com/analysisservices/2003/engine
topic_type:
- apiref
f1_keywords:
- AggregationAttribute
helpviewer_keywords:
- AggregationAttribute data type
ms.assetid: 636827c7-938d-4b7d-9827-46da3bc60d9a
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: 05b0f2f1bc4ed517c289cb4e68810265118d9ea7
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48078672"
---
# <a name="aggregationattribute-data-type-assl"></a>AggregationAttribute データ型 (ASSL)
  間の関連付けを表すプリミティブ データ型を定義、[集計](../objects/aggregation-element-assl.md)要素と属性。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<AggregationAttribute>  
   <AttributeID>...</AttributeID>  
      <Annotations>...</Annotations>  
</AggregationAttribute>  
```  
  
## <a name="data-type-characteristics"></a>データ型の特性  
  
|特性|説明|  
|--------------------|-----------------|  
|基本データ型|なし|  
|派生データ型|なし|  
  
## <a name="data-type-relationships"></a>データ型のリレーションシップ  
  
|リレーションシップ|要素|  
|------------------|-------------|  
|親要素|なし|  
|子要素|[AttributeID](../properties/id-element-assl.md)、[注釈](../collections/annotations-element-assl.md)|  
|派生要素|[属性](../objects/attribute-element-assl.md)([属性](../collections/attributes-element-assl.md)のコレクション[AggregationDimension](dimension-data-type-assl.md))|  
  
## <a name="remarks"></a>コメント  
 分析管理オブジェクト (AMO) オブジェクト モデルで対応するクラスは <xref:Microsoft.AnalysisServices.AggregationAttribute> です。  
  
## <a name="see-also"></a>参照  
 [Aggregation 要素&#40;ASSL&#41;](../objects/aggregation-element-assl.md)   
 [Analysis Services スクリプト言語の XML データ型&#40;ASSL&#41;](analysis-services-scripting-language-xml-data-types-assl.md)  
  
  
