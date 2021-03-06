---
title: メッセージを使用して |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- database-engine
- docset-sql-devref
ms.topic: reference
topic_type:
- apiref
helpviewer_keywords:
- messages [SMO]
ms.assetid: 4037a866-4826-4c1f-890c-e7e3658adf13
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: ba6be1ebca7ee70b3c2bfc31e30a4636942c8d09
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48113652"
---
# <a name="using-messages"></a>メッセージの使用
  SMO では、システム メッセージは、`Server` オブジェクトに属する <xref:Microsoft.SqlServer.Management.Smo.SystemMessageCollection> オブジェクトで表現します。 システム メッセージは変更することができないため、`SystemMessage` オブジェクト プロパティは読み込み専用となります。  
  
 SMO では、プログラム上では <xref:Microsoft.SqlServer.Management.Smo.UserDefinedMessageCollection> オブジェクトを使用してユーザー定義メッセージを表現します。 既存のユーザー定義メッセージは、コレクションを反復処理することで検索することができます。 新しいユーザー定義メッセージは、新しい `UserDefinedMessage` オブジェクトをインスタンス化し、適切なプロパティの設定を行うことによって作成することができます。  
  
## <a name="examples"></a>使用例  
 次のコード例では、アプリケーションを作成するプログラミング環境、プログラミング テンプレート、およびプログラミング言語を選択する必要があります。 詳細については、次を参照してください。 [Visual Studio .NET で Visual Basic SMO プロジェクトを作成](../../../database-engine/dev-guide/create-a-visual-basic-smo-project-in-visual-studio-net.md)と[Visual C の作成&#35;Visual Studio .NET での SMO プロジェクト](../how-to-create-a-visual-csharp-smo-project-in-visual-studio-net.md)します。  
  
## <a name="finding-a-particular-system-message-in-visual-basic"></a>Visual Basic での特定のシステム メッセージの検索  
 このコード例では、システム メッセージを ID 番号で識別してメッセージを表示する方法を示します。  
  
<!-- TODO: review snippet reference  [!CODE [SMO How to#SMO_VBMessages1](SMO How to#SMO_VBMessages1)]  -->  
  
## <a name="finding-a-particular-system-message-in-visual-c"></a>Visual C# での特定のシステム メッセージの検索  
 このコード例では、システム メッセージを ID 番号で識別してメッセージを表示する方法を示します。  
  
```  
{  
            //Connect to the local, default instance of SQL Server.   
            Server srv = new Server();  
            //Reference an existing system message using the   
            //ItemByIdAndLanguage method.   
            SystemMessage msg = default(SystemMessage);  
            msg = srv.SystemMessages.ItemByIdAndLanguage(14126, "us_english");  
            //Display the message ID and text.   
            Console.WriteLine(msg.ID.ToString() + " " + msg.Text);  
        }  
```  
  
## <a name="finding-a-particular-system-message-in-powershell"></a>PowerShell での特定のシステム メッセージの検索  
 このコード例では、システム メッセージを ID 番号で識別してメッセージを表示する方法を示します。  
  
```  
# Set the path context to the local, default instance of SQL Server.  
CD \sql\localhost\  
$srv = get-item default  
  
#Get the message 14126 in US English and display it  
$msg = $srv.SystemMessages.ItemByIdAndLanguage(14126, "us_english")  
$msg.ID.ToString() + " "+ $msg.Text  
```  
  
## <a name="adding-a-new-user-defined-message-in-visual-basic"></a>Visual Basic での新しいユーザー定義メッセージの追加  
 コード例では、50000 より大きい ID を使用してユーザー定義メッセージを作成する方法を示します。  
  
```  
Dim mysrv As Server  
mysrv = New Server  
Dim udm As UserDefinedMessage  
udm = New UserDefinedMessage(mysrv, 50003, "us_english", 16, "Test message")  
udm.Create()  
```  
  
## <a name="adding-a-new-user-defined-message-in-visual-c"></a>Visual C# での新しいユーザー定義メッセージの追加  
 コード例では、50000 より大きい ID を使用してユーザー定義メッセージを作成する方法を示します。  
  
```  
{  
  
            Server mysrv = new Server();  
  
            UserDefinedMessage udm = new UserDefinedMessage(mysrv, 50030, "us_english",16, "Test message");  
            udm.Create();  
             UserDefinedMessage  msg = mysrv.UserDefinedMessages.ItemByIdAndLanguage(50030, "us_english");  
            //Display the message ID and text.   
            Console.WriteLine(msg.ID.ToString() + " " + msg.Text);  
  
        }  
```  
  
## <a name="adding-a-new-user-defined-message-in-powershell"></a>PowerShell での新しいユーザー定義メッセージの追加  
 コード例では、50000 より大きい ID を使用してユーザー定義メッセージを作成する方法を示します。  
  
```  
#Get a server object which corresponds to the default instance  
$srv = New-Object -TypeName Microsoft.SqlServer.Management.SMO.Server  
  
#Create a new message  
  
$udm = New-Object -TypeName Microsoft.SqlServer.Management.SMO.UserDefinedMessage -argumentlist `  
$srv, 50030, "us_english", 16, "Test message"  
$udm.Create()  
$msg = $srv.UserDefinedMessages.ItemByIdAndLanguage(50030, "us_english");  
$msg  
```  
  
  
