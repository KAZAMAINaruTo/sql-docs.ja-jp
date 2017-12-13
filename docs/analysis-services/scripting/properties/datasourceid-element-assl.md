---
title: "DataSourceID 要素 (ASSL) |Microsoft ドキュメント"
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
apiname: DataSourceID Element
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords: DataSourceID
helpviewer_keywords: DataSourceID element
ms.assetid: 2d71ba53-1684-4da0-8da4-fb75033c971b
caps.latest.revision: "35"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 38af766b80158eb4b2145ca7934efd0d4fbfb02b
ms.sourcegitcommit: f1a6944f95dd015d3774a25c14a919421b09151b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2017
---
# <a name="datasourceid-element-assl"></a>DataSourceID 要素 (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]識別、[データソース](../../../analysis-services/scripting/objects/datasource-element-assl.md)親要素に関連付けられている要素です。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<CubeBinding> <!-- or one of the elements listed below in the Element Relationships table -->  
   ...  
   <DataSourceID>...</DataSourceID>  
   ...  
</CubeBinding>  
```  
  
## <a name="element-characteristics"></a>要素の特性  
  
|特性|説明|  
|--------------------|-----------------|  
|データ型と長さ|なし|  
|既定値|なし|  
|Cardinality|コンテキストに応じる|  
  
## <a name="element-relationships"></a>要素の関係  
  
|リレーションシップ|要素|  
|------------------|-------------|  
|親要素|[CubeBinding](../../../analysis-services/scripting/data-type/cubebinding-data-type-out-of-line-assl.md)、 [CubeDimensionBinding](../../../analysis-services/scripting/data-type/cubedimensionbinding-data-type-assl.md)、 [DimensionBinding](../../../analysis-services/scripting/data-type/dimensionbinding-data-type-assl.md)、 [MeasureGroupBinding](../../../analysis-services/scripting/data-type/measuregroupbinding-data-type-assl.md)、 [QueryBinding](../../../analysis-services/scripting/data-type/querybinding-data-type-assl.md)、 [DataSourceView](../../../analysis-services/scripting/objects/datasourceview-element-assl.md)、 [TableBinding](../../../analysis-services/scripting/data-type/tablebinding-data-type-assl.md)|  
|子要素|なし|  
  
## <a name="remarks"></a>解説  
 親に対応する要素**DataSourceID**分析管理オブジェクト (AMO) オブジェクト モデルには<xref:Microsoft.AnalysisServices.CubeDimensionBinding>、 <xref:Microsoft.AnalysisServices.DimensionBinding>、 <xref:Microsoft.AnalysisServices.MeasureGroupBinding>、 <xref:Microsoft.AnalysisServices.QueryBinding>、 <xref:Microsoft.AnalysisServices.DataSourceView>、および<xref:Microsoft.AnalysisServices.TableBinding>.  
  
## <a name="see-also"></a>参照  
 [ID 要素 &#40;です。ASSL &#41;](../../../analysis-services/scripting/properties/id-element-assl.md)   
 [プロパティ &#40;です。ASSL &#41;](../../../analysis-services/scripting/properties/properties-assl.md)  
  
  
