---
title: "SQLSetScrollOptions (デスクトップ データベース ドライバー) |Microsoft ドキュメント"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: microsoft
ms.reviewer: 
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- SQLSetScrollOptions function [ODBC], Desktop Database Drivers
ms.assetid: 51d643ed-015b-4639-969a-9491d9875aca
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: bd83d7ce68d0a7bc1045aee76c28b9b5c39c9faf
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="sqlsetscrolloptions-desktop-database-drivers"></a>SQLSetScrollOptions (デスクトップ データベース ドライバー)
SQL_CONCUR_READ_ONLY では、順方向カーソルと静的カーソルはサポートされます。  
  
 キーセット ドリブン カーソルのみがサポートされている、 *fConcurrency* SQL_CONCUR_LOCK の引数。  
  
 *FConcurrency* SQL_CONCUR_ROWVER の引数はサポートされていません。  
  
 動的カーソルやカーソルの混合はサポートされていません。

