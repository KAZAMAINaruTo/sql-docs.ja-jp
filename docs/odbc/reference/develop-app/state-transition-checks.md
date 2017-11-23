---
title: "状態の移行チェック |Microsoft ドキュメント"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: reference
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- diagnostic information [ODBC], driver manager error checking
- state transition checks [ODBC]
- driver manager [ODBC], error checking
ms.assetid: 0706db7d-e125-4845-a13a-7fe4308f7360
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 0d6c33118d108c4a4c9e541db311710202cabdb3
ms.sourcegitcommit: 7f8aebc72e7d0c8cff3990865c9f1316996a67d5
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="state-transition-checks"></a>状態遷移のチェック
ドライバー マネージャーは、環境、接続、またはステートメントの状態が呼び出される関数に適していることを確認します。 たとえば、接続が、割り当て済みにあります。 状態に**SQLConnect**が呼び出されます。 ステートメントが準備済みである必要があります状態に**SQLExecute**と呼びます。 ドライバー マネージャーは、状態遷移のエラーの SQL_ERROR を返します。
