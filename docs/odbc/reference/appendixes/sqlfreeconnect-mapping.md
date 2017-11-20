---
title: "SQLFreeConnect マッピング |Microsoft ドキュメント"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: reference
ms.reviewer: 
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- mapping deprecated functions [ODBC], SQLFreeConnect
- SQLFreeConnect function [ODBC], mapping
ms.assetid: 8a844538-93c0-4709-bab6-35c45e771d80
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: f83eaaf01bb828963f6ebe98b78f70461346b763
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="sqlfreeconnect-mapping"></a>SQLFreeConnect マッピング
アプリケーションを呼び出すと**SQLFreeConnect**から ODBC 3*.x*ドライバーへの呼び出し  
  
```  
SQLFreeConnect(hdbc)   
```  
  
 をマップされます。  
  
```  
SQLFreeHandle(SQL_HANDLE_DBC,Handle)  
```  
  
 *処理*引数の値に設定されて*hdbc*です。

