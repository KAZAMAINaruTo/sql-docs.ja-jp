---
title: "XSINIL パラメーターを使用した NULL 値に対する要素の生成 | Microsoft Docs"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: xml
ms.reviewer: 
ms.suite: sql
ms.technology: dbe-xml
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- FOR XML clause, null values
- null values [SQL Server], XML
- ELEMENTS directive
- XSINIL parameter
ms.assetid: 2dbc4e48-1cae-4d83-b371-3265da9687cc
caps.latest.revision: "21"
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 7b1bf02ea398cd8310dce5fb3afabee3ec681232
ms.sourcegitcommit: 66bef6981f613b454db465e190b489031c4fb8d3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2017
---
# <a name="generate-elements-for-null-values-with-the-xsinil-parameter"></a>XSINIL パラメーターを使用した NULL 値に対する要素の生成
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)] **ELEMENTS** ディレクティブにより構成される XML では、各列の値が XML の要素にマップされます。 列の値が NULL の場合、要素は追加されません。 ELEMENTS ディレクティブでオプションの **XSINIL** パラメーターを指定すると、NULL 値に対しても要素を作成するように要求できます。 この場合、値が NULL の各列に対して、TRUE に設定された **xsi:nil** 属性を持つ要素が返されます。  
  
## <a name="see-also"></a>参照  
 [FOR XML での RAW モードの使用](../../relational-databases/xml/use-raw-mode-with-for-xml.md)  
  
  
