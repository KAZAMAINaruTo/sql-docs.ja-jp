---
title: MSSQLSERVER_9692 | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- database-engine
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- 9692 (Database Engine error)
ms.assetid: 02399d6e-ab5e-4f30-8a3e-2bb1e8c135b5
caps.latest.revision: 16
author: craigg-msft
ms.author: craigg
manager: jhubbard
ms.openlocfilehash: 396f1ae8e711157bc8f6b911997557f68e397c47
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36085220"
---
# <a name="mssqlserver9692"></a>MSSQLSERVER_9692
    
## <a name="details"></a>詳細  
  
|||  
|-|-|  
|製品名|SQL Server|  
|イベント ID|9692|  
|イベント ソース|MSSQLSERVER|  
|コンポーネント|SQLEngine|  
|シンボル名|SB2_CANT_LISTEN_PORT_IN_USE|  
|メッセージ テキスト|ポート %d は他のプロセスで使用中なので、%S_MSG プロトコルのトランスポートではそのポートでリッスンできません。|  
  
## <a name="explanation"></a>説明  
 指定された TCP ポートが、コンピューター上の別のプログラムで使用されています。  
  
## <a name="user-action"></a>ユーザーの操作  
 実行`netstat -aon`をどのようなプログラムがポートを使用して決定します。 そのアプリケーションを無効にするか、Service Broker に対して別のポートを指定します。  
  
  