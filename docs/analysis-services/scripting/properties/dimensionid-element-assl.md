---
title: "DimensionID 要素 (ASSL) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/06/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology:
- analysis-services
- docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
apiname: DimensionID Element
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords: DimensionID
helpviewer_keywords: DimensionID element
ms.assetid: 00262781-4216-4a19-8bdc-d46647f42165
caps.latest.revision: "34"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 3154856186051f14331361266e05e57619ffae61
ms.sourcegitcommit: f1a6944f95dd015d3774a25c14a919421b09151b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2017
---
# <a name="dimensionid-element-assl"></a>DimensionID 要素 (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]ディメンションの識別子 (ID) が含まれています。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<CubeDimension> <!-- or DimensionBinding, DimensionAttributeBinding -- >  
   ...  
   <DimensionID>...</DimensionID>  
      ...  
</CubeDimension>  
```  
  
## <a name="element-characteristics"></a>要素の特性  
  
|特性|説明|  
|--------------------|-----------------|  
|データ型と長さ|文字列|  
|既定値|なし|  
|Cardinality|1-1 : 必須要素で、1 回だけ出現します|  
  
## <a name="element-relationships"></a>要素の関係  
  
|リレーションシップ|要素|  
|------------------|-------------|  
|親要素|[CubeDimension](../../../analysis-services/scripting/data-type/cubedimension-data-type-assl.md)、 [DimensionBinding](../../../analysis-services/scripting/data-type/dimensionbinding-data-type-assl.md)、 [DimensionAttributeBinding](../../../analysis-services/scripting/data-type/dimensionattributebinding-data-type-out-of-line-assl.md)|  
|子要素|なし|  
  
## <a name="remarks"></a>解説  
 親に対応する要素**DimensionID**分析管理オブジェクト (AMO) オブジェクト モデルには<xref:Microsoft.AnalysisServices.CubeDimension>と<xref:Microsoft.AnalysisServices.DimensionBinding>です。  
  
## <a name="see-also"></a>参照  
 [プロパティ &#40;です。ASSL &#41;](../../../analysis-services/scripting/properties/properties-assl.md)  
  
  
