---
title: 'プロパティ (Visual C++ 構文のインデックス #import) |Microsoft ドキュメント'
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.suite: sql
ms.tgt_pltfrm: ''
ms.topic: conceptual
apitype: COM
dev_langs:
- C++
helpviewer_keywords:
- 'Property collection [ADO], Visual C++ syntax index with #import'
ms.assetid: 80988ca7-f514-438d-bf6f-9390dfe93fc3
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 5f228cc91f07c850448b4edfd61bde2aa909778c
ms.sourcegitcommit: 62826c291db93c9017ae219f75c3cfeb8140bf06
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "35280752"
---
# <a name="property-visual-c-syntax-index-with-import"></a>プロパティ (Visual C++ 構文のインデックス #import)
## <a name="properties"></a>[プロパティ]  
  
```  
long GetAttributes( );  
void PutAttributes( long plAttributes );  
__declspec(property(get=GetAttributes,put=PutAttributes)) long  
    Attributes;  
  
_bstr_t GetName( );  
__declspec(property(get=GetName)) _bstr_t Name;  
  
enum DataTypeEnum GetType( );  
__declspec(property(get=GetType)) enum DataTypeEnum Type;  
  
_variant_t GetValue( );  
void PutValue( const _variant_t & pval );  
__declspec(property(get=GetValue,put=PutValue)) _variant_t Value;  
```  
  
## <a name="see-also"></a>参照  
 [Property オブジェクト (ADO)](../../../ado/reference/ado-api/property-object-ado.md)
