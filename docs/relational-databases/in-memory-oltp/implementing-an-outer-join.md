---
title: 外部結合の実装 | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: in-memory-oltp
ms.reviewer: ''
ms.suite: sql
ms.technology: in-memory-oltp
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 67084043-6b23-4975-b9db-6e49923d4bab
caps.latest.revision: 8
author: MightyPen
ms.author: genemi
manager: craigg
monikerRange: =azuresqldb-current||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: a1baa8026668e6b43991230dfbf5c417678b65f5
ms.sourcegitcommit: 4183dc18999ad243c40c907ce736f0b7b7f98235
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2018
ms.locfileid: "43094681"
---
# <a name="implementing-an-outer-join"></a>外部結合の実装
[!INCLUDE[appliesto-ss-asdb-xxxx-xxx-md](../../includes/appliesto-ss-asdb-xxxx-xxx-md.md)]

  LEFT OUTER JOIN と RIGHT OUTER JOIN は、 [!INCLUDE[ssSQL15](../../includes/sssql15-md.md)]以降のネイティブ コンパイル T-SQL モジュールでサポートされています。  
  
  
