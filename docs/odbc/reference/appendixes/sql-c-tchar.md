---
title: SQL_C_TCHAR |Microsoft ドキュメント
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: drivers
ms.service: ''
ms.component: odbc
ms.reviewer: ''
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: ''
ms.topic: conceptual
helpviewer_keywords:
- sql_c_tchar [ODBC]
- pseudo-type identifiers [ODBC], SQL_C_TCHAR
- data types [ODBC], pseudo-type identifiers
ms.assetid: 9e27c8bd-ee15-4ce9-b70a-34cf1bf16f4c
caps.latest.revision: 6
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 7f2367dcae307e3152005c1bb47885a274c6cc0a
ms.sourcegitcommit: 2ddc0bfb3ce2f2b160e3638f1c2c237a898263f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
---
# <a name="sqlctchar"></a>SQL_C_TCHAR
SQL_C_TCHAR 型識別子が、データ型を実際には識別できません。これは、Unicode 変換用のヘッダー ファイル内に存在するマクロです。 UNICODE の設定に応じて SQL_C_CHAR または SQL_C_WCHAR によって置き換えられる **#define**です。 アプリケーションは、ANSI と Unicode のアプリケーションの両方としてコンパイルする文字データを転送するのに便利です。
