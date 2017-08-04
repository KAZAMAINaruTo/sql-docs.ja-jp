---
title: "SQL Server - Azure SQL DB への Access データベースの移行 |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- sql-ssma
ms.tgt_pltfrm: 
ms.topic: article
applies_to:
- Azure SQL Database
- SQL Server
helpviewer_keywords:
- instructions, migration
- migrating databases, overview
- overview, migration process
- procedure, migration
- recommended migration process
ms.assetid: 76a3abcf-2998-4712-9490-fe8d872c89ca
caps.latest.revision: 23
author: sabotta
ms.author: carlasab
manager: lonnyb
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 6d3c44ed3c73edae1b2b8d9cd244a2530c5748cf
ms.contentlocale: ja-jp
ms.lasthandoff: 08/02/2017

---
# <a name="migrating-access-databases-to-sql-server---azure-sql-db-accesstosql"></a>SQL Server - Azure SQL DB (AccessToSQL) へのアクセス データベースの移行
[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]Migration Assistant (SSMA) は、包括的な環境に Access データベースを簡単に移行するのに役立つ[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure です。 SSMA を使用すると、アクセスを確認することができ、[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure データベース オブジェクト、Access データベースの移行の評価、データベース オブジェクトに変換、読み込みに[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure、し、データを移行します。  
  
## <a name="recommended-migration-process"></a>移行プロセスを推奨  
正常に移行するオブジェクトとデータへのアクセスを[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure、次のプロセスを使用します。  
  
1.  [新しい SSMA プロジェクトを作成](http://msdn.microsoft.com/en-us/f2d1f0b0-5394-4adb-b3f3-abd71eb68ca7)です。 プロジェクトを作成することができます[プロジェクト オプションを設定](http://msdn.microsoft.com/en-us/0a7304df-2f35-4453-96ef-7ac83dea1167)です。 変換オプション、移行オプション、およびデータ型のマッピングが含まれます。  
  
2.  [Access データベース ファイルを追加](http://msdn.microsoft.com/en-us/e944c740-4c8a-4bc1-b0ed-be57bc06dced)をプロジェクトにします。  
  
    個々 のファイルを追加することができますか、コンピューターまたはネットワーク上にあるファイルを追加することができます。  
  
3.  [SQL Server のターゲット インスタンスに接続する](http://msdn.microsoft.com/en-us/f84cf007-ddf1-4396-a07c-3e0729abc769)または[SQL Azure のターゲット インスタンスに接続する](http://msdn.microsoft.com/en-us/1ba0d113-dc05-4431-8689-e14a8821bafd)です。  
  
    SQL Server または SQL Azure に接続することができますか。  
  
4.  1 つまたは複数の Access データベースの間のマッピングをカスタマイズして[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure スキーマ[マップ ソースとターゲット データベース](http://msdn.microsoft.com/en-us/69bee937-7b2c-49ee-8866-7518c683fad4)です。  
  
5.  ことができます必要に応じて、[評価レポートを作成する](http://msdn.microsoft.com/en-us/8b9e23d6-da62-437a-8c05-8ad2628b9441)に Access データベース オブジェクトを正常に変換するかどうかを決定する[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure です。  
  
6.  [データベース オブジェクトを変換](http://msdn.microsoft.com/en-us/e0ef67bf-80a6-4e6c-a82d-5d46e0623c6c)に[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure オブジェクトの定義。  
  
7.  [SQL Server に変換後のデータベース オブジェクトを読み込む](http://msdn.microsoft.com/en-us/4e854eee-b10c-4f0b-9d9e-d92416e6f2ba)します。  
  
    データベース オブジェクトを負荷することができます[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]SSMA、またはを使用して SQL Azure に保存したり[!INCLUDE[tsql](../../includes/tsql_md.md)]スクリプト。  
  
8.  [SQL Server にデータへのアクセスを移行](http://msdn.microsoft.com/en-us/f3b18af7-1af0-499d-a00d-a0af94895625)です。  
  
    > [!NOTE]  
    > 変換し、読み込むには、スキーマと 1 つの手順でデータを移行できます。 1 回のクリックの移行を実行する をクリックして、**変換、読み込み、および移行**ボタンをクリックします。  
  
9. ユーザー アクセス アプリケーション内のデータを使用するかどうか[!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)]または SQL Azure を使用して[SQL Server テーブルにアクセス テーブルをリンク](http://msdn.microsoft.com/en-us/82374ad2-7737-4164-a489-13261ba393d4)です。  
  
またにこのプロセスを指示するのに、移行ウィザードを使用することができます。 詳細については、次を参照してください。[移行ウィザード](http://msdn.microsoft.com/en-us/5bab5914-b2ae-4795-8cf5-83e42d64bef2)です。  
  
## <a name="see-also"></a>参照  
[SQL Server Migration Assistant for Access の概要](http://msdn.microsoft.com/en-us/462a731f-08f1-44e1-9eeb-4deac6d2f6c5)  
[Access データベースの移行の準備](http://msdn.microsoft.com/en-us/9b80a9e0-08e7-4b4d-b5ec-cc998d3f5114)  
  

