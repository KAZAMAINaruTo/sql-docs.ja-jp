---
title: 'タスク 15: 構築と、SSIS プロジェクトを実行する |Microsoft Docs'
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- data-quality-services
- integration-services
- master-data-services
ms.topic: conceptual
ms.assetid: 13adf4e0-216a-4992-b13d-b7b1e1629e77
author: douglaslms
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 1b84614910a594c4496e1eba8b7c11cb2d5617d5
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48050403"
---
# <a name="task-15-building-and-running-the-ssis-project"></a>タスク 15: SSIS プロジェクトをビルドおよび実行する
  ここでは、SSIS プロジェクトをビルドおよび実行します。 値を設定する必要があります、コンピューターにインストールされている Excel 2010 の 64 ビット バージョンがあれば、 **Run64BitRuntime**に**False**作業する Excel ソースの。  
  
1.  **ソリューション エクスプ ローラー**ウィンドウで、をクリックして**プロジェクト** をクリックし、メニューで**CleanseAndCurateSuppliers Properties**します。  
  
2.  **プロパティ** ダイアログ ボックスで、展開**構成プロパティ**をクリックし、左側**デバッグ**します。  
  
3.  設定**Run64BitRuntime**に**False**します。  
  
     ![CleanseAndCurateSuppliers プロジェクトのプロパティ](../../2014/tutorials/media/et-buildingandrunningthessisproject-01.jpg "CleanseAndCurateSuppliers プロジェクトのプロパティ")  
  
4.  クリックして**OK**を閉じる、**プロパティ** ダイアログ ボックス。  
  
5.  クリックして**ビルド**をクリックし、メニュー バー **Build CleanseAndCurateSuppliers**します。 ビルド エラーがないことを確認します。  
  
6.  クリックして**デバッグ**をクリックし、メニュー バー**デバッグの開始**します。  
  
7.  メッセージを確認して、**進行状況**ウィンドウと、そのパッケージが実行され、正常に終了したことを確認します。  
  
     ![進行状況ウィンドウの結果](../../2014/tutorials/media/et-buildingandrunningthessisproject-02.jpg "進行状況ウィンドウの結果")  
  
     ![進行状況ウィンドウの最終状態](../../2014/tutorials/media/et-buildingandrunningthessisproject-03.jpg "進行状況ウィンドウの最終状態")  
  
8.  クリックして**デバッグ**をクリックし、メニュー バー**デバッグの停止**デバッグ セッションを停止します。 パッケージの実行に失敗した場合、データ ビューアーを有効にしてコンポーネント間のデータ フローを確認する必要があります。  
  
## <a name="next-step"></a>次の手順  
 [タスク 16: マスター データ マネージャーを確認する](../../2014/tutorials/task-16-verifying-with-master-data-manager.md)  
  
  
