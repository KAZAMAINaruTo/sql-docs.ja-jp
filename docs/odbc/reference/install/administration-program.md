---
title: プログラムの管理 |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- administration program [ODBC]
- ODBC administrator [ODBC]
ms.assetid: a6c8248a-7a01-42e7-aaed-99dc94d50028
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 740a09d9a6bceb9d3f290faa71444df0d1e7c6c7
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47792320"
---
# <a name="administration-program"></a>管理プログラム
> [!NOTE]  
>  ODBC は Windows XP および Windows Server 2003 以降、Windows オペレーティング システムに含まれます。 Windows の以前のバージョンで ODBC を明示的にのみインストールしてください。  
  
 管理プログラム、ODBC アドミニストレーターは、Windows SDK/MDAC SDK に含まれています。 このプログラムし、SDK のユーザーによる再配布できます。 さらに、開発者は、独自の管理プログラムを作成できます。 一般に、開発者は、管理プログラムとして機能しているアプリケーションから直接データ ソースを構成するか、データ ソースの構成を完全に制御を維持する場合にのみ管理プログラムを記述します。 たとえば、スプレッドシート プログラムでは、ユーザーを追加して、実行時にデータ ソースを使用を許可できます。  
  
 管理プログラムは、まずインストーラー DLL を読み込みます。 インストーラーは、次のタスクを実行する DLL で関数を呼び出します。  
  
-   **追加、変更、または対話形式でデータ ソースを削除します。** 管理プログラムを呼び出すことができます**SQLManageDataSources**、 **SQLCreateDataSource**、または**SQLConfigDataSource**します。  
  
     **SQLManageDataSources**がユーザーを追加、変更、またはデータ ソースを削除するオプションを指定できますトレース; インストーラー DLL は、コントロール パネルから直接呼び出されたときに、この関数が呼び出されます ダイアログ ボックスを表示します。 **SQLCreateDataSource**をユーザーはのみのデータ ソースを追加 ダイアログ ボックスが表示されます。 **SQLConfigDataSource**ドライバーのセットアップ DLL への直接の呼び出しに渡します。  
  
     インストーラー DLL を呼び出す場合は、 **ConfigDSN**ドライバーの設定を実際には追加 DLL では、変更、またはデータ ソースを削除します。 ドライバーのセットアップ DLL を追加情報を求める場合があります。  
  
-   **追加、変更、またはサイレント モードでデータ ソースを削除します。** 管理プログラムの呼び出し**SQLConfigDataSource**インストーラー DLL とパスに null ウィンドウを処理を追加、変更、または削除するには、データ ソースの名前と、レジストリの値の一覧。 インストーラー DLL の呼び出し**ConfigDSN**ドライバーの設定を実際には追加 DLL では、変更、またはデータ ソースを削除します。  
  
-   **追加、変更、または既定のデータ ソースを削除します。** 既定のデータ ソースでは、その名前が既定値が他のデータ ソースの場合と同じです。 追加、変更、または他のデータ ソースと同じ方法で削除されたことが。
