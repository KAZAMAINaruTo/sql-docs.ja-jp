---
title: sysmail_delete_profileaccount_sp (TRANSACT-SQL) |Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sysmail_delete_profileaccount_sp
- sysmail_delete_profileaccount_sp_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysmail_delete_profileaccount_sp
ms.assetid: b58d06f2-d6c9-4c8e-95bd-027c50f4621a
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: de13b3b3ff39ac9aacdbcd7beb996a353593f609
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47677160"
---
# <a name="sysmaildeleteprofileaccountsp-transact-sql"></a>sysmail_delete_profileaccount_sp (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  データベース メール プロファイルからアカウントを削除します。  
  
 ![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>構文  
  
```  
  
sysmail_delete_profileaccount_sp  {   [ @profile_id = ] profile_id | [ @profile_name = ] 'profile_name' } ,  
    {   [ @account_id = ] account_id | [ @account_name = ] 'account_name' }  
```  
  
## <a name="arguments"></a>引数  
 [ **@profile_id** = ] *profile_id*  
 削除するプロファイルのプロファイル ID です。 *profile_id*は**int**、既定値は NULL です。 いずれか、 *profile_id*または*profile_name*指定することがあります。  
  
 [ **@profile_name** =] **'***profile_name***'**  
 削除するプロファイルのプロファイル名を指定します。 *profile_name*は**sysname**、既定値は NULL です。 いずれか、 *profile_id*または*profile_name*指定することがあります。  
  
 [ **@account_id** =] *account_id*  
 削除するアカウント ID を指定します。 *account_id*は**int**、既定値は NULL です。 いずれか、 *account_id*または*account_name*指定することがあります。  
  
 [ **@account_name** =] **'***account_name***'**  
 削除するアカウントの名前を指定します。 *account_name*は**sysname**、既定値は NULL です。 いずれか、 *account_id*または*account_name*指定することがあります。  
  
## <a name="return-code-values"></a>リターン コードの値  
 **0** (成功) または**1** (失敗)  
  
## <a name="result-sets"></a>結果セット  
 なし  
  
## <a name="remarks"></a>コメント  
 指定したアカウントと指定したプロファイルが関連付けられていない場合は、エラーが返されます。  
  
 アカウントを指定し、プロファイルを指定しなかった場合、このストアド プロシージャでは指定したアカウントがすべてのプロファイルから削除されます。 たとえば、既存の SMTP サーバーをシャットダウンする前に、その SMTP サーバーを使用しているアカウントを各プロファイルから個別に削除するのではなく、すべてのプロファイルからまとめて削除できます。  
  
 プロファイルを指定し、アカウントを指定しなかった場合、このストアド プロシージャでは指定したプロファイルからすべてのアカウントが削除されます。 たとえば、プロファイルが使用している SMTP サーバーを変更する場合は、そのプロファイルからすべてのアカウントを削除してから必要に応じて新しいアカウントを追加するほうが便利な場合があります。  
  
 ストアド プロシージャ**sysmail_delete_profileaccount_sp**では、 **msdb**が所有するデータベースにあり、 **dbo**スキーマ。 現在のデータベースがない場合、3 つの部分の名前を持つプロシージャを実行する必要があります**msdb**します。  
  
## <a name="permissions"></a>アクセス許可  
 このプロシージャの既定のメンバーへのアクセス許可を実行、 **sysadmin**固定サーバー ロール。  
  
## <a name="examples"></a>使用例  
 次の例では、プロファイルの `Audit Account` からアカウントの `AdventureWorks Administrator` を削除します。  
  
```  
EXECUTE msdb.dbo.sysmail_delete_profileaccount_sp  
    @profile_name = 'AdventureWorks Administrator',  
    @account_name = 'Audit Account' ;  
```  
  
## <a name="see-also"></a>参照  
 [データベース メール](../../relational-databases/database-mail/database-mail.md)   
 [データベース メール アカウントを作成します。](../../relational-databases/database-mail/create-a-database-mail-account.md)   
 [データベース メール構成オブジェクト](../../relational-databases/database-mail/database-mail-configuration-objects.md)   
 [データベース メール ストアド プロシージャ&#40;TRANSACT-SQL&#41;](../../relational-databases/system-stored-procedures/database-mail-stored-procedures-transact-sql.md)  
  
  
