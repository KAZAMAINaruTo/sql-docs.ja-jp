---
title: Master、tempdb、および model データベースでフルテキスト インデックスはサポートされていません |Microsoft ドキュメント
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- full-text indexes
ms.assetid: f7992965-42c1-4eb8-a7fb-afb38b67c740
caps.latest.revision: 21
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 1d334a3626c11050418df3fae483f5b9029adeb4
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36072264"
---
# <a name="full-text-indexes-on-master-tempdb-and-model-databases-are-not-supported"></a>master、tempdb、および model データベースに対するフルテキスト インデックスはサポートされない
  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] では、いずれのシステム データベースに対してもフルテキスト インデックスが許可されません。  
  
## <a name="description"></a>説明  
 [!INCLUDE[ssVersion2000](../../includes/ssversion2000-md.md)] では、フルテキスト インデックスが master、tempdb、および model の各データベースでサポートされていました。  
  
 Master、tempdb、および model データベースでも、フルテキスト カタログは、アップグレード中に削除されます。  
  
## <a name="see-also"></a>参照  
 [アップグレード アドバイザーの使用](../../../2014/sql-server/install/working-with-upgrade-advisor.md)  
  
  