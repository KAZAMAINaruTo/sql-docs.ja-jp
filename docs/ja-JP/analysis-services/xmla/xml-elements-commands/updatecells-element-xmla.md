---
title: UpdateCells 要素 (XMLA) |Microsoft ドキュメント
ms.custom: ''
ms.date: 03/03/2017
ms.prod: analysis-services
ms.prod_service: analysis-services, azure-analysis-services
ms.service: ''
ms.component: ''
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- UpdateCells Element
apilocation:
- http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to:
- SQL Server 2016 Preview
f1_keywords:
- microsoft.xml.analysis.updatecells
- urn:schemas-microsoft-com:xml-analysis#UpdateCells
- http://schemas.microsoft.com/analysisservices/2003/engine#UpdateCells
helpviewer_keywords:
- UpdateCells command
ms.assetid: 18336a35-8a46-4532-9ee7-71828b2982af
caps.latest.revision: 12
author: Minewiskan
ms.author: owend
manager: kfile
ms.openlocfilehash: cd1c56f458d067ff5984ac42c371dfa5a43c5025
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
---
# <a name="updatecells-element-xmla"></a>UpdateCells 要素 (XMLA)
[!INCLUDE[ssas-appliesto-sqlas-aas](../../../includes/ssas-appliesto-sqlas-aas.md)]
  書き込み許可キューブ内のセルを更新します。  
  
## <a name="syntax"></a>構文  
  
```xml  
  
<Command>  
   <UpdateCells>  
      <Cell>...</Cell>  
   </UpdateCells>  
</Command>  
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
|親要素|[Command](../../../analysis-services/xmla/xml-elements-properties/command-element-xmla.md)|  
|子要素|[セル](../../../analysis-services/xmla/xml-elements-properties/cell-element-xmla.md)|  
  
## <a name="remarks"></a>解説  
 **UpdateCells**コマンドは、セルの書き戻しをサポートするキューブのセルを更新します。  
  
 セルの更新の詳細については、「[セルの更新 &#40;XMLA&#41;](../../../analysis-services/multidimensional-models-scripting-language-assl-xmla/updating-cells-xmla.md)」を参照してください。  
  
## <a name="see-also"></a>参照  
 [Drop 要素 & #40 です。XMLA & #41;](../../../analysis-services/xmla/xml-elements-commands/drop-element-xmla.md)   
 [要素 & #40; を挿入します。XMLA & #41;](../../../analysis-services/xmla/xml-elements-commands/insert-element-xmla.md)   
 [Update 要素 & #40 です。XMLA & #41;](../../../analysis-services/xmla/xml-elements-commands/update-element-xmla.md)   
 [コマンドと #40 です。XMLA & #41;](../../../analysis-services/xmla/xml-elements-commands/xml-elements-commands.md)  
  
  
