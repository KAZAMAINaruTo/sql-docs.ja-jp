---
title: STIsSimple (geometry データ型) | Microsoft Docs
ms.custom: ''
ms.date: 08/03/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- STIsSimple_TSQL
- STIsSimple (geometry Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- STIsSimple (geometry Data Type)
ms.assetid: da8f45d4-4f9c-405d-b883-760eb5344a71
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: e974d8cda1a6c21e7b3d568f242d36c96d81b5f7
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47718300"
---
# <a name="stissimple-geometry-data-type"></a>STIsSimple (geometry データ型)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

**geometry** インスタンスが Open Geospatial Consortium (OGC) で定義されているとおりの単純なものであれば 1 を返します。 **geometry** インスタンスが単純なものでない場合、0 を返します。
  
## <a name="syntax"></a>構文  
  
```  
  
.STIsSimple ( )  
```  
  
## <a name="return-types"></a>戻り値の型  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 戻り値の型: **bit**  
  
 CLR の戻り値の型: **SqlBoolean**  
  
## <a name="remarks"></a>Remarks  
 単純であると見なされるには、**geometry** インスタンスが次の要件をすべて満たしている必要があります。  
  
-   インスタンスの各図形が終点以外で自己交差していてはいけない。  
  
-   インスタンスの 2 つの図形が、両方の図形の境界外部の点で互いに交差していてはいけない。  
  
## <a name="examples"></a>使用例  
 次は、それ自体と交差する単純ではない `LineString` インスタンスを作成し、`STIsSimple()` を使用して `LineString` が単純かどうかをテストする例です。  
  
```  
DECLARE @g geometry;  
SET @g = geometry::STGeomFromText('LINESTRING(0 0, 2 2, 0 2, 2 0)', 0);  
SELECT @g.STIsSimple();  
```  
  
## <a name="see-also"></a>参照  
 [Geometry インスタンスの OGC メソッド](../../t-sql/spatial-geometry/ogc-methods-on-geometry-instances.md)  
  
  

