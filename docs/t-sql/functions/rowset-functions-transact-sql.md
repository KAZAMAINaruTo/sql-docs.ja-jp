---
title: "行セット関数 (TRANSACT-SQL) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/15/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- functions [SQL Server], rowsets
- rowsets [SQL Server], functions
- rowsets [SQL Server]
ms.assetid: ac24d700-3144-4ab5-9fa8-8c014001cc71
caps.latest.revision: 24
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 16f842ec37ddb777c1f3ea801c922f52791d5e91
ms.contentlocale: ja-jp
ms.lasthandoff: 09/01/2017

---
# <a name="rowset-functions-transact-sql"></a>行セット関数 (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx_md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  次の行セット関数は、[!INCLUDE[tsql](../../includes/tsql-md.md)] ステートメントの中でテーブル参照の代わりに使用できるオブジェクトを返します。  
  
|||  
|-|-|  
|[OPENDATASOURCE](../../t-sql/functions/opendatasource-transact-sql.md)|[OPENJSON](../../t-sql/functions/openjson-transact-sql.md)|  
|[OPENROWSET](../../t-sql/functions/openrowset-transact-sql.md)|[OPENQUERY](../../t-sql/functions/openquery-transact-sql.md)|  
|[OPENXML](../../t-sql/functions/openxml-transact-sql.md)||  
  
 すべての行セット関数は非決定的です。 つまり、これらの関数は、同じ一連の入力値を使用しても、呼び出されるたびに常に同じ結果を返すわけではありません。 関数の決定性の詳細については、次を参照してください。[決定的関数と非決定的関数](../../relational-databases/user-defined-functions/deterministic-and-nondeterministic-functions.md)です。  
  
## <a name="see-also"></a>参照  
 [組み込み関数 &#40;Transact-SQL&#41;](~/t-sql/functions/functions.md)  
  
  

