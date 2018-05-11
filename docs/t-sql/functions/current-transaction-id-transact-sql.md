---
title: CURRENT_TRANSACTION_ID (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 07/24/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.component: t-sql|functions
ms.reviewer: ''
ms.suite: sql
ms.technology: t-sql
ms.tgt_pltfrm: ''
ms.topic: language-reference
f1_keywords:
- CURRENT_TRANSACTION_ID
- CURRENT_TRANSACTION_ID_TSQL
- sys.CURRENT_TRANSACTION_ID
- sys.CURRENT_TRANSACTION_ID_TSQL
helpviewer_keywords:
- CURRENT_TRANSACTION_ID function
ms.assetid: 82cd9f92-d935-45a0-a433-620d6e15b467
caps.latest.revision: 6
author: edmacauley
ms.author: edmaca
manager: craigg
ms.openlocfilehash: b5170c6a3b96710ea42d1acdb88256c33be0eb6d
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
---
# <a name="currenttransactionid-transact-sql"></a>CURRENT_TRANSACTION_ID (TRANSACT-SQL)
[!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]

現在のセッションでは、現在のトランザクションのトランザクションの ID を返します。
  
![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>構文  
  
```sql
CURRENT_TRANSACTION_ID( )  
  
```  
  
## <a name="return-types"></a>戻り値の型
**bigint**
  
## <a name="return-value"></a>戻り値  
* *から取得した現在のセッションで、現在のトランザクションのトランザクション ID [sys.dm_tran_current_transaction (&) #40 です。TRANSACT-SQL と #41;.**](../../relational-databases/system-dynamic-management-views/sys-dm-tran-current-transaction-transact-sql.md)
  
## <a name="permissions"></a>アクセス許可  
すべてのユーザーには、現在のセッションのトランザクション ID を返すことができます。
  
## <a name="examples"></a>使用例  
次の例では、現在のセッションのトランザクション ID が返されます。
  
```sql
SELECT CURRENT_TRANSACTION_ID();  
```  
  
## <a name="see-also"></a>参照
[sp_set_session_context &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-set-session-context-transact-sql.md)  
[SESSION_CONTEXT &#40;Transact-SQL&#41;](../../t-sql/functions/session-context-transact-sql.md)  
[行レベルのセキュリティ](../../relational-databases/security/row-level-security.md)  
[CONTEXT_INFO &#40;Transact-SQL&#41;](../../t-sql/functions/context-info-transact-sql.md)  
[SET CONTEXT_INFO &#40;Transact-SQL&#41;](../../t-sql/statements/set-context-info-transact-sql.md)
  
  
