---
title: "メンバー関数の使用 |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/02/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- kbMDX
helpviewer_keywords:
- member functions [MDX]
ms.assetid: 094c443f-0daa-4af7-801c-d2e1d686d755
caps.latest.revision: 24
author: Minewiskan
ms.author: owend
manager: erikre
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 9354c2e6a83918742f1c2de1dea943be4b21e844
ms.contentlocale: ja-jp
ms.lasthandoff: 08/02/2017

---
# <a name="using-member-functions"></a>メンバー関数の使用
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  メンバー関数は、メンバーを返す多次元式 (MDX) 関数です。 メンバー関数は、組関数や集合関数と同様に、[!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] で使用される多次元構造を操作するために不可欠です。  
  
 MDX の多くのメンバー関数の最も重要なは、 **CurrentMember**関数、階層の現在のメンバーを判別するために使用します。 次のクエリは、と共に使用する方法を示しています、**親**、**先祖**、および**Prevmember**関数。  
  
 `WITH`  
  
 `//Returns the name of the currentmember on the Calendar hierarchy`  
  
 `MEMBER MEASURES.[CurrentMemberDemo] AS [Date].[Calendar].CurrentMember.Name`  
  
 `//Returns the name of the parent of the currentmember on the Calendar hierarchy`  
  
 `MEMBER MEASURES.[ParentDemo] AS [Date].[Calendar].CurrentMember.Parent.Name`  
  
 `//Returns the name of the ancestor of the currentmember on the Calendar hierarchy at the Year level`  
  
 `MEMBER MEASURES.[AncestorDemo] AS ANCESTOR([Date].[Calendar].CurrentMember, [Date].[Calendar].[Calendar Year]).Name`  
  
 `//Returns the name of the member before the currentmember on the Calendar hierarchy`  
  
 `MEMBER MEASURES.[PrevMemberDemo] AS [Date].[Calendar].CurrentMember.Prevmember.Name`  
  
 `SELECT{MEASURES.[CurrentMemberDemo],MEASURES.[ParentDemo],MEASURES.[AncestorDemo],MEASURES.[PrevMemberDemo] } ON 0,`  
  
 `[Date].[Calendar].MEMBERS ON 1`  
  
 `FROM [Adventure Works]`  
  
## <a name="see-also"></a>参照  
 [関数と #40 です。MDX 構文 &#41;](../mdx/functions-mdx-syntax.md)   
 [組関数の使用](../mdx/using-tuple-functions.md)   
 [集合関数の使用](../mdx/using-set-functions.md)  
  
  

