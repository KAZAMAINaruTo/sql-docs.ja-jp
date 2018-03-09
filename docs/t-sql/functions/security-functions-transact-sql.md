---
title: "セキュリティ関数 (TRANSACT-SQL) |Microsoft ドキュメント"
ms.custom: 
ms.date: 03/15/2017
ms.prod: sql-non-specified
ms.prod_service: sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- functions [SQL Server], security
- security functions
- roles [SQL Server], functions
- users [SQL Server], security functions
- security [SQL Server], functions
ms.assetid: 7773a87d-2f1b-4951-a225-baf159a7291b
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: f7539b13d9f1c6a39aa2273ad75f5a25a78b5c2b
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="security-functions-transact-sql"></a>セキュリティ関数 (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  次の関数は、セキュリティの管理に役立つ情報を返します。 追加の関数については、「[暗号化関数 &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/cryptographic-functions-transact-sql.md).  
  
|||  
|-|-|  
|[CERTENCODED &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/certencoded-transact-sql.md)|[PWDCOMPARE と #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/pwdcompare-transact-sql.md)|  
|[CERTPRIVATEKEY &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/certprivatekey-transact-sql.md)|[PWDENCRYPT &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/pwdencrypt-transact-sql.md)|  
|[CURRENT_USER と #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/current-user-transact-sql.md)|[SCHEMA_ID &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/schema-id-transact-sql.md)|  
|[DATABASE_PRINCIPAL_ID &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/database-principal-id-transact-sql.md)|[SCHEMA_NAME &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/schema-name-transact-sql.md)|  
|[sys.fn_builtin_permissions &#40;です。TRANSACT-SQL と #41 です。](../../relational-databases/system-functions/sys-fn-builtin-permissions-transact-sql.md)|[SESSION_USER と #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/session-user-transact-sql.md)|  
|[sys.fn_get_audit_file &#40;Transact-SQL&#41;](../../relational-databases/system-functions/sys-fn-get-audit-file-transact-sql.md)|[SUSER_ID と #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/suser-id-transact-sql.md)|  
|[sys.fn_my_permissions &#40;です。TRANSACT-SQL と #41 です。](../../relational-databases/system-functions/sys-fn-my-permissions-transact-sql.md)|[SUSER_SID &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/suser-sid-transact-sql.md)|  
|[HAS_PERMS_BY_NAME &#40;Transact-SQL&#41;](../../t-sql/functions/has-perms-by-name-transact-sql.md)|[SUSER_SNAME &#40;Transact-SQL&#41;](../../t-sql/functions/suser-sname-transact-sql.md)|  
|[IS_MEMBER &#40;Transact-SQL&#41;](../../t-sql/functions/is-member-transact-sql.md)|[SYSTEM_USER &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/system-user-transact-sql.md)|  
|[IS_ROLEMEMBER &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/is-rolemember-transact-sql.md)|[SUSER_NAME &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/suser-name-transact-sql.md)|  
|[IS_SRVROLEMEMBER &#40;Transact-SQL&#41;](../../t-sql/functions/is-srvrolemember-transact-sql.md)|[USER_ID と #40 です。TRANSACT-SQL と #41 です。](../../t-sql/functions/user-id-transact-sql.md)|  
|[ORIGINAL_LOGIN &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/original-login-transact-sql.md)|[USER_NAME &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/user-name-transact-sql.md)|  
|[アクセス許可 &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/permissions-transact-sql.md)||  
  
 Windows グループのメンバーシップの詳細については、次を参照してください。 [xp_logininfo (& a) #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-stored-procedures/xp-logininfo-transact-sql.md)と[xp_enumgroups (& a) #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-stored-procedures/xp-enumgroups-transact-sql.md).  
  
## <a name="see-also"></a>参照  
 [セキュリティのストアド プロシージャと #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-stored-procedures/security-stored-procedures-transact-sql.md)   
 [暗号化関数 &#40;です。TRANSACT-SQL と #41 です。](../../t-sql/functions/cryptographic-functions-transact-sql.md)   
 [組み込み関数 &#40;Transact-SQL&#41;](~/t-sql/functions/functions.md)   
 [セキュリティ ステートメント](http://msdn.microsoft.com/library/aebe2ec7-31bc-4697-a493-dcfcd0903a7b)  
  
  
