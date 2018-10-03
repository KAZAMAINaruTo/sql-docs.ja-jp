---
title: RelationshipEndVisualizationProperties データ型 (ASSL) |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- analysis-services
- docset-sql-devref
ms.topic: reference
ms.assetid: 11f9a10f-d36c-4faf-b595-3fe969d1935e
author: minewiskan
ms.author: owend
manager: craigg
ms.openlocfilehash: fb59b92c7b0942ce8d8e1c4fd719a8591e6a35cb
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48104102"
---
# <a name="relationshipendvisualizationproperties-data-type-assl"></a>RelationshipEndVisualizationProperties データ型 (ASSL)
  リレーションシップのリレーションシップ End を表すプリミティブ データ型を定義します。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<RelationshipEnd>  
   <FolderPosition>...</FolderPosition>  
   <ContextualNameRule>...</ContextualNameRule>  
   <DefaultDetailsPosition>...</DefaultDetailsPosition>  
   <DisplayKeyPosition>...</DisplayKeyPosition>  
   <CommonIdentifierPosition>...</CommonIdentifierPosition>  
   <IsDefaultMeasure>...</IsDefaultMeasure>  
   <IsDefaultImage>...</IsDefaultImage>  
   <SortPropertiesPosition>...</SortPropertiesPosition>  
</RelationshipEnd>  
```  
  
## <a name="data-type-characteristics"></a>データ型の特性  
  
|特性|説明|  
|--------------------|-----------------|  
|基本データ型|なし|  
|派生データ型|なし|  
  
## <a name="data-type-relationships"></a>データ型のリレーションシップ  
  
|リレーションシップ|要素|  
|------------------|-------------|  
|親要素|[RelationshipEnd](relationshipend-data-type-assl.md)|  
|子要素|[FolderPosition](../../xmla/xml-elements-properties/folderposition-element-xml.md)、 [ContextualNameRule](../../xmla/xml-elements-properties/contextualnamerule-element-xml.md)、 [DefaultDetailsPosition](../../xmla/xml-elements-properties/defaultdetailsposition-element-xml.md)、 [DisplayKeyPosition](../../xmla/xml-elements-properties/displaykeyposition-element-xml.md)、 [CommonIdentifierPosition](../../xmla/xml-elements-properties/commonidentifierposition-element-xml.md)、 [IsDefaultMeasure](../../xmla/xml-elements-properties/isdefaultmeasure-element-xml.md)、 [IsDefaultImage](../../xmla/xml-elements-properties/isdefaultimage-element-xml.md)、 [SortPropertiesPosition](../../xmla/xml-elements-properties/sortpropertiesposition-element-xml.md)|  
|派生要素||  
  
## <a name="remarks"></a>コメント  
 分析管理オブジェクト (AMO) オブジェクト モデルで対応する要素は<xref:Microsoft.AnalysisServices.RelationshipEnd>します。  
  
  
