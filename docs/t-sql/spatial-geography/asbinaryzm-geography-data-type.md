---
title: "AsBinaryZM (geography データ型) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|spatial-geography
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- AsBinaryZM
- AsBinaryZM_TSQL
dev_langs: TSQL
helpviewer_keywords:
- AsBinaryZM, geography
- AsBinaryZM
ms.assetid: 37246adb-814d-4113-9983-4d336de8182c
caps.latest.revision: "7"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 99981d95095b97dd599787578f891a39e60098ac
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2018
---
# <a name="asbinaryzm-geography-data-type"></a>AsBinaryZM (geography データ型)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

  Open Geospatial Consortium (OGC) Well-Known Binary (WKB) 表現を返します、 **geometry**インスタンスは、いずれかで補完された**Z** (標高) と**M** (メジャー)インスタンスの値。  
  
## <a name="syntax"></a>構文  
  
```  
  
.AsBinaryZM()  
```  
  
## <a name="return-types"></a>戻り値の型  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] return type: **varbinary(max)**  
  
 CLR の戻り値の型: **SqlBytes**  
  
## <a name="remarks"></a>解説  
  
## <a name="examples"></a>使用例  
  
```sql  
DECLARE @g1 GEOGRAPHY = 'Point(1 1 2 3)';  
  
SELECT @g1.STAsBinary();  
-- Returns: 0x0101000000000000000000F03F000000000000F03F  
  
SELECT @g1.AsBinaryZM();  
--Returns: 0x01B90B0000000000000000F03F000000000000F03F00000000000000400000000000000840  
```  
  
## <a name="see-also"></a>参照  
 [Geography インスタンスの拡張メソッド](../../t-sql/spatial-geography/extended-methods-on-geography-instances.md)   
 [M &#40;geography データ型&#41;](../../t-sql/spatial-geography/m-geography-data-type.md)   
 [Z &#40;geography データ型&#41;](../../t-sql/spatial-geography/z-geography-data-type.md)  
  
  
