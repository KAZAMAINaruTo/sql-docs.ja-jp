---
title: "HasM (geometry データ型) |Microsoft ドキュメント"
ms.custom: 
ms.date: 05/05/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|spatial-geography
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- HasM geometry
ms.assetid: 15540837-c4bf-4d18-b380-13ae31f3226f
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: cb449a098a60e253204b4d37e5dc22fd05c8f50b
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2018
---
# <a name="hasm-geometry-datatype"></a>HasM (geometry データ型)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

  空間オブジェクトに少なくとも 1 つの M 値が含まれている場合は 1 (true)、それ以外の場合は 0 (false) を返します。  
  
## <a name="syntax"></a>構文  
  
```  
  
.HasM  
```  
  
## <a name="return-types"></a>戻り値の型  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]型を返す:**ビット**  
  
 CLR の戻り値の型:**ブール**  
  
## <a name="remarks"></a>解説  
  
## <a name="examples"></a>使用例  
  
```sql  
DECLARE @p GEOMETRY = 'Point(1 1 1 1)'  
SELECT @p.HasM   
--Returns: 1 (true)  
```  
  
## <a name="see-also"></a>参照  
 [Geometry インスタンスの拡張メソッド](../../t-sql/spatial-geometry/extended-methods-on-geometry-instances.md)   
 [M &#40;geometry データ型&#41;](../../t-sql/spatial-geometry/m-geometry-data-type.md)  
  
  
