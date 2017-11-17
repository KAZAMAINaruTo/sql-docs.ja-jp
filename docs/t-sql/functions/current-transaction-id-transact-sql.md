---
title: "CURRENT_TRANSACTION_ID (TRANSACT-SQL) |Microsoft ドキュメント"
ms.custom: 
ms.date: 07/24/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
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
manager: cguyer
ms.workload: Inactive
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 6716663ea2e54fdeb372b2a1ce2aa3e206f785ac
ms.contentlocale: ja-jp
ms.lasthandoff: 09/01/2017

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
取得した現在のセッションで現在のトランザクションのトランザクション ID [sys.dm_tran_current_transaction & #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-dynamic-management-views/sys-dm-tran-current-transaction-transact-sql.md).
  
## <a name="permissions"></a>Permissions  
すべてのユーザーには、現在のセッションのトランザクション ID を返すことができます。
  
## <a name="examples"></a>使用例  
次の例では、現在のセッションのトランザクション ID が返されます。
  
```sql
SELECT CURRENT_TRANSACTION_ID();  
```  
  
## <a name="see-also"></a>参照
[sp_set_session_context & #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-stored-procedures/sp-set-session-context-transact-sql.md)  
[SESSION_CONTEXT & #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/session-context-transact-sql.md)  
[行レベルのセキュリティ](../../relational-databases/security/row-level-security.md)  
[CONTEXT_INFO & #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/context-info-transact-sql.md)  
[SET CONTEXT_INFO & #40 です。TRANSACT-SQL と #41 です。](../../t-sql/statements/set-context-info-transact-sql.md)
  
  

