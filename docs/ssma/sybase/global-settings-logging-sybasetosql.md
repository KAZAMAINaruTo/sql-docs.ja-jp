---
title: グローバル設定 (ログ) (SybaseToSQL) |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
ms.assetid: 4cb4da20-3b99-4aae-8c80-329ee23e796e
author: Shamikg
ms.author: Shamikg
manager: craigg
ms.openlocfilehash: 1c4b128dc548780350d76c758543a852895118e2
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47851720"
---
# <a name="global-settings-logging-sybasetosql"></a>グローバル設定 (ログ) (SybaseToSQL)
使用して、**グローバル設定**SSMA のログ記録設定を指定 ダイアログ ボックス。 通常、製品サポートを使用する場合にのみ、これらの設定を変更するは。  
  
このダイアログ ボックスにアクセスする、**ツール**メニューの **グローバル設定**順にクリックします、**ログ**左側のウィンドウの下部にあるボタン。  
  
## <a name="options"></a>および  
**メッセージ レベル**  
次のオプションが **メッセージ レベル**:  
  
|オプション|説明|  
|----------|---------------|  
|**[すべてのカテゴリ]**|次のオプションのすべてのログ記録レベルを設定するために使用します。|  
|**コレクター**|送信元スキーマに関するメタデータを収集し、プロジェクトに保存します。|  
|**コンバーター**|テーブルおよびストアド プロシージャなどのソース データベース オブジェクトの構造体に対応する変換[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]構造体。|  
|**データの移行**|ソース データベースからデータを移行[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]します。|  
|**フォーマッタ**|用のスクリプトを生成するコンバーターのサブコンポーネント、[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]スキーマ。|  
|**グラフィカル ユーザー インターフェイス**|SSMA ツールを使用するときに表示されるメッセージ。|  
|**リンカー**|SQL 識別子を解決し、他のコンポーネントに情報を提供します。|  
|**その他**|その他のカテゴリにないすべてのメッセージ。|  
|**パーサー**|送信元スキーマを解析します。|  
|**シンクロナイザー**|ソースにデータベース オブジェクトの読み込み[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]します。|  
|**TreeConverter**|ソースのメタデータ内のオブジェクトに変換します[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]メタデータ。|  
  
各オプションの下の**メッセージ レベル**SSMA の次のログ記録レベルのいずれかを構成します。  
  
|||  
|-|-|  
|**致命的なエラー**|致命的なエラー メッセージのみをログに書き込みます。|  
|**Error**|エラーと致命的なエラー メッセージをログに書き込みます。|  
|**警告**|警告、エラー、および致命的なエラー メッセージをログに書き込みます。|  
|**情報**|情報、警告、エラー、および致命的なエラー メッセージをログに書き込みます。|  
|**デバッグ**|デバッグ ログにメッセージを含む、すべてのメッセージを記述します。|  
  
**ログ ファイルのパス**  
ファイルのパスと SSMA のログ ファイルの名前。 別の名前を指定する、現在のパス をクリックし、クリックし、参照 (**.**) ボタンをクリックします。  
  
**ログ ファイルのサイズ**  
サポート技術情報のログ ファイルの最大サイズ。 最小のサイズは 10 KB です。 既定のサイズは 10240 KB です。  
  
**ログ ファイルの合計数**  
1 つのログがいっぱいになる、SSMA は、ログ ファイルの名前を変更し、新しいを開始します。 この設定を使用すると、保持するログ ファイルの最大数を指定します。 最小値は、2 です。  
  
