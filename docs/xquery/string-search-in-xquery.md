---
title: "XQuery での検索文字列 |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/04/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
applies_to:
- SQL Server
dev_langs:
- XML
helpviewer_keywords:
- strings [SQL Server], search
- XML [SQL Server], searching text
- searches [SQL Server], XML documents
- XQuery, string search
ms.assetid: edc62024-4c4c-4970-b5fa-2e54a5aca631
caps.latest.revision: 23
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: d76942bb93b751d8a4747cceab357616330f096e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/01/2017

---
# <a name="string-search-in-xquery"></a>XQuery での文字列検索
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  このトピックには、XML ドキュメント内のテキストを検索する方法を示すサンプル クエリを掲載しています。  
  
## <a name="examples"></a>使用例  
  
### <a name="a-find-feature-descriptions-that-contain-the-word-maintenance-in-the-product-catalog"></a>A. 製品カタログから "maintenance" という語を含む機能説明を検索する  
  
```  
SELECT CatalogDescription.query('  
     declare namespace p1="http://schemas.microsoft.com/sqlserver/2004/07/adventure-works/ProductModelDescription";  
    for $f in /p1:ProductDescription/p1:Features/*  
     where contains(string($f), "maintenance")  
     return  
           $f ') as Result  
FROM Production.ProductModel  
WHERE ProductModelID=19  
```  
  
 前のクエリで、`where`の結果をフィルター処理、FLOWR 式、`for`式とを満たす要素のみを返します、 **contains()**条件。  
  
 結果を次に示します。  
  
```  
<p1:Maintenance     
      xmlns:p1="http://schemas.microsoft.com/sqlserver/2004/07/adventure-works/ProductModelWarrAndMain">  
 <p1:NoOfYears>10</p1:NoOfYears>  
 <p1:Description>maintenance contact available through your   
               dealer or any AdventureWorks retail store.</p1:Description>  
</p1:Maintenance>  
```  
  
## <a name="see-also"></a>参照  
 [XML データ &#40;SQL Server&#41;](../relational-databases/xml/xml-data-sql-server.md)   
 [XQuery 言語リファレンス &#40;SQL Server&#41;](../xquery/xquery-language-reference-sql-server.md)  
  
  
