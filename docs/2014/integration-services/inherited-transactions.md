---
title: トランザクションの継承 |Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- integration-services
ms.topic: conceptual
helpviewer_keywords:
- transactions [Integration Services], inherited
- child packages
- inherited transactions [Integration Services]
ms.assetid: 90db5564-d41e-4cfe-8c9e-4e68d41eff1c
author: douglaslms
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 3f3555125032b5409f53b802990df0e5da04954f
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48058442"
---
# <a name="inherited-transactions"></a>トランザクションの継承
  パッケージでパッケージ実行タスクを使用して、別のパッケージを実行できます。 パッケージ実行タスクで実行される子パッケージでは、独自のパッケージ トランザクションを作成する場合もあれば、親パッケージのトランザクションを継承する場合もあります。  
  
 次の 2 つの条件に該当する場合、パッケージは親パッケージのトランザクションを継承します。  
  
-   パッケージがパッケージ実行タスクによって呼び出される。  
  
-   パッケージを呼び出すパッケージ実行タスクも、親パッケージのトランザクションに参加している。  
  
 子パッケージ自身がトランザクションに参加していなければ、子パッケージのコンテナーやタスクは親パッケージのトランザクションに参加できません。  
  
## <a name="illustration-of-package-transactions"></a>パッケージ トランザクションの図  
 次の図には、3 個のパッケージがあり、すべてトランザクションを使用します。 各パッケージには、複数のタスクが含まれています。 トランザクションの動作がわかりやすいように、パッケージ実行タスクは 1 つだけ示されています。 パッケージ A がパッケージ B および C を実行します。次に、パッケージ B がパッケージ D および E を実行し、パッケージ C がパッケージ F を実行します。  
  
 パッケージとタスクのトランザクション属性は次のとおりです。  
  
-   パッケージ A および C の**TransactionOption** は **Required** に設定されています。  
  
-   パッケージ B と D、およびパッケージ実行タスク B、パッケージ実行タスク D、パッケージ実行タスク F の**TransactionOption** は **Supported** に設定されています。  
  
-   パッケージ E、およびパッケージ実行タスク C、パッケージ実行タスク E の**TransactionOption** は **NotSupported** に設定されています。  
  
 ![トランザクションの継承のフロー](media/mw-dts-executepack.gif "トランザクションの継承のフロー")  
  
 パッケージ B、D、および F のみが親パッケージのトランザクションを継承できます。  
  
 パッケージ B および D は、パッケージ A が開始したトランザクションを継承します。  
  
 パッケージ F はパッケージ C が開始したトランザクションを継承します。  
  
 パッケージ A および C は独自のトランザクションを制御します。  
  
 パッケージ E はトランザクションを使用しません。  
  
## <a name="related-tasks"></a>Related Tasks  
 [トランザクションを使用するようにパッケージを構成する](../relational-databases/native-client-ole-db-transactions/transactions.md)  
  
  
