---
title: DQSInstaller.exe を使用した DQS ナレッジ ベースのエクスポートとインポート | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: data-quality-services
ms.reviewer: ''
ms.technology: data-quality-services
ms.topic: conceptual
ms.assetid: 8234c63b-a018-4e55-8184-9a6bdf03274d
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 2b76eca15b4c435230c2449d79dd892fd9bd736a
ms.sourcegitcommit: c19696d3d67161ce78aaa5340964da3256bf602d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "52617452"
---
# <a name="export-and-import-dqs-knowledge-bases-using-dqsinstallerexe"></a>DQSInstaller.exe を使用した DQS ナレッジ ベースのエクスポートとインポート

[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly](../../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]

  DQS の既存のインストールでは、コマンド プロンプトで DQSInstaller.exe ファイルを実行して、 [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] のすべてのナレッジ ベースを DQS バックアップ ファイル (.dqsb) へ一度にエクスポートし、その後で .dqsb ファイルを使用してすべてのナレッジ ベースを別の [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] へ一度にインポートできます。 コマンド プロンプトからの DQSInstaller.exe の実行の詳細については、「 [コマンド プロンプトから DQSInstaller.exe を実行する](../../data-quality-services/install-windows/run-dqsinstaller-exe-to-complete-data-quality-server-installation.md#CommandPrompt) 」の「 [Data Quality Server のインストールを完了するための DQSInstaller.exe の実行](../../data-quality-services/install-windows/run-dqsinstaller-exe-to-complete-data-quality-server-installation.md)」を参照してください。  
  
 この機能を使用すると、 *を使用して各ナレッジ ベースを .dqs ファイルへ個別にエクスポートすることなく、* の [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] すべての [!INCLUDE[ssDQSClient](../../includes/ssdqsclient-md.md)]ナレッジ ベースを一度にバックアップできます。 同様に、 *を使用して .dqs ファイルから各ナレッジ ベースを個別にインポートすることなく、* すべての [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] ナレッジ ベースをバックアップ ファイルから別の [!INCLUDE[ssDQSClient](../../includes/ssdqsclient-md.md)]へ一度にインポートできます。 これは、コンピューターの [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] をアンインストールして別のコンピューターに再インストールするときにナレッジ ベースをバックアップして復元する場合に特に便利です。 既存の [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] インストールのすべてのナレッジ ベースを DQS バックアップ ファイル (.dqsb) へエクスポートし、別のコンピューターに [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] をインストールした後にすべてのナレッジ ベースをバックアップ ファイルからインポートすることが簡単にできます。  
  
##  <a name="export"></a> .dqsb ファイルへのナレッジ ベースのエクスポート  
 既存の [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] のすべてのナレッジ ベースをいつでもエクスポートできます。また、 [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)]のアンインストール中にエクスポートすることもできます。  
  
-   [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] のすべてのナレッジ ベースを DQS バックアップ ファイル (.dqsb) へエクスポートするには、コマンド プロンプトで `exportkbs` パラメーターとナレッジ ベースのエクスポート先の完全パスおよびファイル名を指定して DQSInstaller.exe を実行します。 たとえば、すべてのナレッジ ベースを C: ドライブの DQSBackup.dqsb ファイルへエクスポートするには、次のように入力します。  
  
    ```  
    dqsinstaller.exe -exportkbs c:\DQSBackup.dqsb  
    ```  
  
    > [!NOTE]  
    >  指定したファイル名が指定した場所に既に存在する場合は、ファイルを上書きするかどうかを確認するメッセージが表示されます。  
  
-   [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)]のアンインストール中にすべてのナレッジ ベースを DQS バックアップ ファイルへエクスポートするには、コマンド プロンプトで `uninstall` パラメーターとナレッジ ベースのエクスポート先の完全パスおよびファイル名を指定して DQSInstaller.exe を実行します。 たとえば、すべてのナレッジ ベースを C: ドライブの DQSBackup.dqsb ファイルへエクスポートしてから [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)]をアンインストールするには、次のように入力します。  
  
    ```  
    dqsinstaller.exe -uninstall c:\DQSBackup.dqsb  
    ```  
  
    > [!NOTE]  
    >  [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] パラメーターを使用してコマンド プロンプトから `uninstall` をアンインストールするときに DQS バックアップ ファイルの完全パスとファイル名を指定しなかった場合は、すべてのナレッジ ベースが削除されることを示すメッセージが表示され、アンインストール プロセスを続行するかどうかを選択できます。  
  
##  <a name="import"></a> .dqsb ファイルからのナレッジ ベースのインポート  
 [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] のインストールが完了した後にすべてのナレッジ ベースを DQS バックアップ ファイル (.dqsb) からインポートできます。 ナレッジベースをインポートするには、有効な DQS バックアップ ファイル (.dqsb) が必要です。  
  
 コマンド プロンプトで `importkbs` パラメーターとナレッジ ベースのインポート元の完全パスおよびファイル名を指定して DQSInstaller.exe ファイルを実行します。 たとえば、すべてのナレッジ ベースを C: ドライブの DQSBackup.dqsb ファイルからインポートするには、次のように入力します。  
  
```  
dqsinstaller.exe -importkbs c:\DQSBackup.dqsb  
```  
  
 インポートしているナレッジ ベースと同じ名前のナレッジ ベースが [!INCLUDE[ssDQSServer](../../includes/ssdqsserver-md.md)] に既に存在する場合は、インポートされたナレッジ ベースの名前の後にアンダースコア (_) と 1 から始まる整数値が付加されます。 たとえば、"CompanyName" ドメインが重複する場合、インポートされたドメイン名は "CompanyName_1" になります。  
  
## <a name="see-also"></a>参照  
 [Data Quality Server のインストールを完了するための DQSInstaller.exe の実行](../../data-quality-services/install-windows/run-dqsinstaller-exe-to-complete-data-quality-server-installation.md)   
 [Data Quality Services のインストール](../../data-quality-services/install-windows/install-data-quality-services.md)   
 [.dqs ファイルへのナレッジ ベースのエクスポート](../../data-quality-services/export-a-knowledge-base-to-a-dqs-file.md)   
 [.dqs ファイルからのナレッジ ベースのインポート](../../data-quality-services/import-a-knowledge-base-from-a-dqs-file.md)  
  
  
