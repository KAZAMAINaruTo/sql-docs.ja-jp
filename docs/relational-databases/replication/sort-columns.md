---
title: '[列の並べ替え] | Microsoft Docs'
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: conceptual
f1_keywords:
- sql13.rep.monitor.sortcolumns.f1
ms.assetid: 66b44b6c-10a5-4e3f-a97b-7568609c88ac
author: MashaMSFT
ms.author: mathoma
manager: craigg
ms.openlocfilehash: ce595fc0032ef8c1f498993f0953aa90117d73ce
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47737380"
---
# <a name="sort-columns"></a>[列の並べ替え]
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
  **[列の並べ替え]** ダイアログ ボックスでは、1 つ以上の列を基準にしてレプリケーション モニターのグリッドを並べ替えることができます (また、レプリケーション モニターのグリッドの列ヘッダーをクリックすることにより、1 つの列を基準にして並べ替えることもできます)。 たとえば、 **[すべてのサブスクリプション]** タブのサブスクリプションを、まず状態を基準にして並べ替え、次に接続の種類を基準にして並べ替えるには、次の手順を実行します。  
  
1.  グリッドの最初の行で、 **[列名]** 列から **[状態]** を選択し、 **[並べ替え順序]** 列から値を選択します。  
  
2.  グリッドの 2 番目の行で、 **[列名]** 列から **[接続の種類]** を選択し、 **[並べ替え順序]** 列から値を選択します。  
  
## <a name="options"></a>[変数]  
 **[状態]**  
 並べ替える列の名前です。 1 つ以上の列を基準にして並べ替えることができます。 **[パブリケーション]** タブの **[現在の平均パフォーマンス]** 列または **[現在の最低パフォーマンス]** 列を基準にして並べ替えることはできません。その理由は、これらの列の値の計算方法にあります。  
  
 **[並べ替え順序]**  
 **[昇順]** または **[降順]** を指定します。  
  
 **[すべてクリア]**  
 並べ替えグリッドからすべての行を削除します。 1 つの行を削除するには、行を選択して Del キーを押します。  
  
## <a name="see-also"></a>参照  
 [レプリケーションの監視](../../relational-databases/replication/monitor/monitoring-replication-overview.md)  
  
  
