---
title: SQL Server テーブルを削除する |Microsoft ドキュメント
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
- docset-sql-devref
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- tables [OLE DB]
- deleting tables
- SQL Server Native Client OLE DB provider, tables
- removing tables
- dropping tables
ms.assetid: b6d6c4de-43c6-473e-92aa-34ffddd58cbe
caps.latest.revision: 29
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: dd18658df32c8106432b3a791c1eda2b7edaabf7
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36176161"
---
# <a name="dropping-a-sql-server-table"></a>SQL Server テーブルの削除
  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client OLE DB プロバイダーを公開、 **itabledefinition::droptable**関数。 これにより、削除するコンシューマー、 [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]データベースからテーブル。  
  
 コンシューマーでは、テーブル名を指定の Unicode 文字の文字列として、 *pwszName*のメンバー、 *uName*共用体の*pTableID*パラメーター。 *EKind*のメンバー *pTableID* dbkind_name にする必要があります。  
  
## <a name="see-also"></a>参照  
 [テーブルとインデックス](tables-and-indexes.md)  
  
  