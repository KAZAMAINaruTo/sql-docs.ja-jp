---
title: SQLTables (Visual FoxPro ODBC ドライバー) |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLTables function [ODBC], Visual FoxPro ODBC Driver
ms.assetid: 69e2a038-5def-423f-91aa-8756e069dd2a
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: e134b2870c4506e725f2900b83d1118e42b55d15
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47829000"
---
# <a name="sqltables-visual-foxpro-odbc-driver"></a>SQLTables (Visual FoxPro ODBC ドライバー)
> [!NOTE]  
>  このトピックでには、Visual FoxPro ODBC ドライバー固有の情報が含まれています。 この関数の詳細については、該当するトピックを参照してください。 [ODBC API リファレンス](../../odbc/reference/syntax/odbc-api-reference.md)します。  
  
 サポート: 完全な  
  
 レベル 1 の ODBC API 準拠:  
  
 内のパラメーターで指定されたテーブル名の一覧を返します、 **SQLTables**ステートメント。 パラメーターが指定されていない場合は、現在のデータ ソースに格納されているテーブル名を返します。 ドライバーは、その結果、情報を設定を返します。  
  
 列挙型の呼び出しでは、リモート ビューまたはローカルのパラメーター化されたビューの結果セットのエントリは表示されません。 ただし、呼び出しを**SQLTables**一意テーブルの名前指定子が一致を見つけるようなビューの名前で存在する場合は、これにより、新しいテーブルを作成する前に、名前の競合の確認に使用する API。  
  
> [!NOTE]  
>  Visual FoxPro ODBC ドライバーが区別[データベース テーブル](../../odbc/microsoft/visual-foxpro-terminology.md)と[テーブルを無料](../../odbc/microsoft/visual-foxpro-terminology.md)テーブルの両方の種類は、システム上の同じディレクトリに格納されている場合でも、します。 場合は、データ ソースは、無料のテーブルのディレクトリは、Visual FoxPro ODBC ドライバーはないカタログまたはデータベースに関連付けられているすべてのテーブルの名前を取得します。  
  
 詳細については、次を参照してください。 [SQLTables](../../odbc/reference/syntax/sqltables-function.md)で、 *ODBC プログラマ リファレンス*します。
