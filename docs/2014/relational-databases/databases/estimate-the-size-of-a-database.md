---
title: データベース サイズの見積もり | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- database-engine
ms.topic: conceptual
helpviewer_keywords:
- space allocation [SQL Server], database size
- calculating database size
- increasing database size
- database size [SQL Server], estimating
- predicting database size
- size [SQL Server], databases
- estimating database size
- designing databases [SQL Server], estimating size
ms.assetid: 5b240161-eba4-44b0-946c-61a8fc00fc8c
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 61f62b56e2eb825f933dc11a30039e9b18ca9228
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48125892"
---
# <a name="estimate-the-size-of-a-database"></a>データベース サイズの見積もり
  データベースをデザインするときは、データを格納したときにデータベースのサイズがどのくらい大きくなるかを見積もる必要性が生じる場合があります。 データベースのサイズを見積もると、次の目的に必要なハードウェア構成の決定に役立ちます。  
  
-   アプリケーションが必要とするパフォーマンスの実現。  
  
-   データとインデックスの格納に必要となる適切な量の物理ディスク領域の確保。  
  
 データベースのサイズを見積もると、データベースのデザインを改良する必要があるかどうかを判断する場合にも役立ちます。 たとえば、見積もったデータベースのサイズが大きすぎて組織内で実装できず、正規化の必要性があるとわかる場合があります。 逆に、見積もったサイズが予想より小さい場合もあります。 この場合は、データベースを非正規化してクエリのパフォーマンスを向上させることができます。  
  
 データベースのサイズを見積もるには、各テーブルのサイズを個別に見積もり、それぞれの値を合計します。 テーブルのサイズは、テーブルにインデックスが含まれているかどうかにより異なり、インデックスが含まれている場合はそのインデックスの種類によって異なります。  
  
## <a name="in-this-section"></a>このセクションの内容  
  
|トピック|説明|  
|-----------|-----------------|  
|[テーブル サイズの見積もり](estimate-the-size-of-a-table.md)|テーブルおよび関連付けられたインデックスにデータを格納するために必要な領域を見積もる手順や計算方法について説明します。|  
|[ヒープ サイズの見積もり](estimate-the-size-of-a-heap.md)|ヒープにデータを格納するために必要な領域を見積もる手順や計算方法について説明します。 ヒープとは、クラスター化インデックスを含まないテーブルのことです。|  
|[クラスター化インデックスのサイズの見積もり](estimate-the-size-of-a-clustered-index.md)|クラスター化インデックスにデータを格納するために必要な領域を見積もる手順や計算方法について説明します。|  
|[非クラスター化インデックスのサイズの算出](estimate-the-size-of-a-nonclustered-index.md)|非クラスター化インデックスにデータを格納するために必要な領域を見積もる手順や計算方法について説明します。|  
  
  
