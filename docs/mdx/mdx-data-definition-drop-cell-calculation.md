---
title: "DROP CELL CALCULATION ステートメント (MDX) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/02/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- Calculation
- DROP
- DROP_CELL_CALCULATION
- CELL CALCULATION
- DROP CELL
- cell
- DROP CELL CALCULATION
dev_langs:
- kbMDX
helpviewer_keywords:
- deleting calculations
- dropping calculations
- removing calculations
- DROP CELL CALCULATION statement
- calculations [SQL Server]
- cubes [Analysis Services], calculations
ms.assetid: 77caedf4-dd96-4eac-a5e4-fd82148a44a7
caps.latest.revision: 29
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 90e2502709f15620330c69231b590130e1d0cca1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/02/2017

---
# <a name="mdx-data-definition---drop-cell-calculation"></a>MDX データ定義の DROP CELL CALCULATION
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  指定されたセル計算を削除します。  
  
## <a name="syntax"></a>構文  
  
```  
  
DROP [ SESSION ] CELL CALCULATION CURRENTCUBE | Cube_Name.CellCalc_Name  
```  
  
## <a name="arguments"></a>引数  
 *Cube_Name*  
 キューブ式の名前を指定する有効な文字列式です。  
  
 *CellCalc_Name*  
 削除するセル計算の名前を指定する有効な文字列式です。  
  
## <a name="see-also"></a>参照  
 [CELL CALCULATION ステートメント &#40; を作成します。MDX と #41 です。](../mdx/mdx-data-definition-create-cell-calculation.md)   
 [MDX データ定義ステートメント & #40 です。MDX と #41 です。](../mdx/mdx-data-definition-statements-mdx.md)  
  
  

