---
title: CovarianceN (MDX) |Microsoft ドキュメント
ms.date: 06/04/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: mdx
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 054acaaca417ca7d3fa5303fb31b5ea027bfcd72
ms.sourcegitcommit: 97bef3f248abce57422f15530c1685f91392b494
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2018
ms.locfileid: "34740181"
---
# <a name="covariancen-mdx"></a>CovarianceN (MDX)


  バイアスをかけない母集団の公式 (X と Y のペアの数で除算) を使用して、セットに対して評価された値の X と Y のペアのサンプル共分散を返します。  
  
## <a name="syntax"></a>構文  
  
```  
  
CovarianceN(Set_Expression, Numeric_Expression_y [ ,Numeric_Expression_x ] )  
```  
  
## <a name="arguments"></a>引数  
 *Set_Expression*  
 セットを返す有効な多次元式 (MDX) です。  
  
 *Numeric_Expression_y*  
 有効な数値式です。通常は、Y 軸の値を表す数値を返すセル座標の多次元式 (MDX) 式です。  
  
 *Numeric_Expression_x*  
 有効な数値式です。通常は、X 軸の値を表す数値を返すセル座標の多次元式 (MDX) 式です。  
  
## <a name="remarks"></a>コメント  
 **CovarianceN**関数は、y 軸の値を取得する、最初の数値式に対して指定されたセットを評価します。 次に、2 番目の数値式が指定されている場合は、指定されているセットをその式に対して評価し、X 軸の値のセットを取得します。 2 番目の数値式が指定されていない場合は、指定されたセット内のセルの現在のコンテキストを X 軸の値として使用します。  
  
 **CovarianceN**関数は、バイアスをかけない母集団の公式を使用します。 これは、対照的に、[共変性](../mdx/covariance-mdx.md)バイアスをかけた母集団の公式 (x と y のペアの数で除算) を使用する関数。  
  
> [!NOTE]  
>  **CovarianceN**関数は空のセルまたはテキストや論理値を含むセルを無視します。 ただし、0 の値を持つセルは対象になります。  
  
## <a name="see-also"></a>参照  
 [MDX 関数リファレンス&#40;MDX&#41;](../mdx/mdx-function-reference-mdx.md)  
  
  
