---
title: "列暗号化キー (TRANSACT-SQL) を作成 |Microsoft ドキュメント"
ms.custom:
- SQL2016_New_Updated
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- CREATE_COLUMN_ENCRYPTION_KEY_TSQL
- SQL13.SWB.NEWCOLUMNENCRYPTIONKEY.GENERAL.F1
- ENCRYPTION_KEY_TSQL
- CREATE COLUMN ENCRYPTION KEY
- ENCRYPTION KEY
- COLUMN ENCRYPTION KEY
- CREATE_COLUMN_ENCRYPTION_TSQL
- SQL13.SWB.COLUMNENCRYPTIONKEY.GENERAL.F1
- COLUMN_ENCRYPTION_KEY_TSQL
- CREATE COLUMN ENCRYPTION
dev_langs:
- TSQL
helpviewer_keywords:
- Always Encrypted, create column encryption key
- column encryption key, create
- column encryption key
- CREATE COLUMN ENCRYPTION KEY statement
ms.assetid: 517fe745-d79b-4aae-99a7-72be45ea6acb
caps.latest.revision: 20
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 6663d8c00c5f24f3f104643d78698c05b4df636a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/01/2017

---
# <a name="create-column-encryption-key-transact-sql"></a>CREATE COLUMN ENCRYPTION KEY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]

  指定した列のマスター_キーで暗号化された値の初期セットでは、列の暗号化キーを作成します。 これは、メタデータの操作です。 CEK には、列のマスター_キーの回転を可能にするまでに 2 つの値を持つことができます。 使用して、データベースの任意の列を暗号化する前に、CEK の作成が必要、 [Always Encrypted & #40";"データベース エンジン"&"#41;](../../relational-databases/security/encryption/always-encrypted-database-engine.md)機能します。 使用して CEK を作成することも[!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)]します。 CEK を作成する前にを使用して、CMK を定義する必要があります[!INCLUDE[ssManStudio](../../includes/ssmanstudio-md.md)]または[CREATE COLUMN MASTER KEY](../../t-sql/statements/create-column-master-key-transact-sql.md)ステートメントです。  
  
 ![トピック リンク アイコン](../../database-engine/configure-windows/media/topic-link.gif "トピック リンク アイコン") [Transact-SQL 構文表記規則](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>構文  
  
```  
CREATE COLUMN ENCRYPTION KEY key_name   
WITH VALUES  
  (  
    COLUMN_MASTER_KEY = column_master_key_name,   
    ALGORITHM = 'algorithm_name',   
    ENCRYPTED_VALUE = varbinary_literal  
  )   
[, (  
    COLUMN_MASTER_KEY = column_master_key_name,   
    ALGORITHM = 'algorithm_name',   
    ENCRYPTED_VALUE = varbinary_literal  
  ) ]   
[;]  
```  
  
## <a name="arguments"></a>引数  
 *key_name*  
 データベースで、列の暗号化キーを認識する名前です。  
  
 *column_master_key_name*  
 列の暗号化キー (CEK) を暗号化するために使用される列のカスタム マスター キー (CMK) の名前を指定します。  
  
 *アルゴリズム*  
 列の暗号化キーの値を暗号化するために使用する暗号化アルゴリズムの名前です。 システム プロバイダーのアルゴリズムである必要があります**RSA_OAEP**です。  
  
 *varbinary_literal*  
 暗号化のように CEK 値 BLOB です。  
  
> [!WARNING]  
>  ありませんプレーン テキスト CEK 値で渡す次のステートメント。 そうと、この機能のメリットを構成します。  
  
## <a name="remarks"></a>解説  
 列の暗号化キーの作成ステートメントでは、少なくとも 1 つの VALUES 句を含める必要があります、2 つまでことがあります。 提供されているだけの場合は、2 番目の値を後で追加するのに列の暗号化キーの ALTER ステートメントを使用できます。 VALUES 句を削除するのに列の暗号化キーの ALTER ステートメントを使用することもできます。  
  
 通常、1 つだけの暗号化された値は、列の暗号化キーが作成されます。 列のマスター_キーが必要な場合は、(現在列マスター_キーのニーズに新しい列のマスター_キーに置き換えられます) を回転する、列の暗号化キーの新しい値を追加する列の新しいマスター_キーで暗号化します。 これは、オプションを選択するクライアント アプリケーションは、新しい列マスター_キーはクライアント アプリケーションで使用できるに確立している間に、列の暗号化キーで暗号化されたデータにアクセスできることを確認することができます。 常に暗号化するには、新しいマスター_キーにアクセスできない、列の古いマスター_キーで暗号化された列の暗号化のキー値を使用して機密データにアクセスできるクライアント アプリケーションでのドライバーを有効になっています。  
  
 暗号化アルゴリズム、常に暗号化のサポートでは、256 ビットをプレーン テキストの値が必要です。  
  
 列のマスター キーを押しながらキー ストアをカプセル化するキー ストア プロバイダーを使用して、暗号化された値を生成する必要があります。 詳細については、次を参照してください。 [Always Encrypted & #40";"クライアント開発"&"#41;](../../relational-databases/security/encryption/always-encrypted-client-development.md)です。  
  
 使用して[sys.columns & #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-catalog-views/sys-columns-transact-sql.md)、 [sys.column_encryption_keys & #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-catalog-views/sys-column-encryption-keys-transact-sql.md)と[sys.column_encryption_key_values & #40 です。TRANSACT-SQL と #41 です。](../../relational-databases/system-catalog-views/sys-column-encryption-key-values-transact-sql.md)列暗号化キーに関する情報を表示します。  
  
## <a name="permissions"></a>Permissions  
 必要があります、 **ALTER ANY COLUMN ENCRYPTION KEY**権限です。  
  
## <a name="examples"></a>使用例  
  
### <a name="a-creating-a-column-encryption-key"></a>A. 列の暗号化キーを作成します。  
 次の例と呼ばれる列の暗号化キーを作成する`MyCEK`です。  
  
```  
CREATE COLUMN ENCRYPTION KEY MyCEK   
WITH VALUES  
(  
    COLUMN_MASTER_KEY = MyCMK,   
    ALGORITHM = 'RSA_OAEP',   
    ENCRYPTED_VALUE = 0x01700000016C006F00630061006C006D0061006300680069006E0065002F006D0079002F003200660061006600640038003100320031003400340034006500620031006100320065003000360039003300340038006100350064003400300032003300380065006600620063006300610031006300284FC4316518CF3328A6D9304F65DD2CE387B79D95D077B4156E9ED8683FC0E09FA848275C685373228762B02DF2522AFF6D661782607B4A2275F2F922A5324B392C9D498E4ECFC61B79F0553EE8FB2E5A8635C4DBC0224D5A7F1B136C182DCDE32A00451F1A7AC6B4492067FD0FAC7D3D6F4AB7FC0E86614455DBB2AB37013E0A5B8B5089B180CA36D8B06CDB15E95A7D06E25AACB645D42C85B0B7EA2962BD3080B9A7CDB805C6279FE7DD6941E7EA4C2139E0D4101D8D7891076E70D433A214E82D9030CF1F40C503103075DEEB3D64537D15D244F503C2750CF940B71967F51095BFA51A85D2F764C78704CAB6F015EA87753355367C5C9F66E465C0C66BADEDFDF76FB7E5C21A0D89A2FCCA8595471F8918B1387E055FA0B816E74201CD5C50129D29C015895CD073925B6EA87CAF4A4FAF018C06A3856F5DFB724F42807543F777D82B809232B465D983E6F19DFB572BEA7B61C50154605452A891190FB5A0C4E464862CF5EFAD5E7D91F7D65AA1A78F688E69A1EB098AB42E95C674E234173CD7E0925541AD5AE7CED9A3D12FDFE6EB8EA4F8AAD2629D4F5A18BA3DDCC9CF7F352A892D4BEBDC4A1303F9C683DACD51A237E34B045EBE579A381E26B40DCFBF49EFFA6F65D17F37C6DBA54AA99A65D5573D4EB5BA038E024910A4D36B79A1D4E3C70349DADFF08FD8B4DEE77FDB57F01CB276ED5E676F1EC973154F86  
);  
GO  
```  
  
### <a name="creating-a-column-encryption-key-with-2-values"></a>2 つの値を列の暗号化キーを作成します。  
 次の例と呼ばれる列の暗号化キーを作成する`TwoValueCEK`2 つの値。  
  
```  
  
CREATE COLUMN ENCRYPTION KEY TwoValueCEK   
WITH VALUES  
(  
    COLUMN_MASTER_KEY = CMK1,   
    ALGORITHM = 'RSA_OAEP',   
    ENCRYPTED_VALUE = 0x016E000001630075007200720065006E00740075007300650072002F006D0079002F0037006300380061003100310033003400320037003800620037003000630038003100390062003900630039003400360061006600340039006500610030003200650038006200650038003400340065006C33A82ECF04A7185824B4545457AC5244CD9C219E64067B9520C0081B8399B58C2863F7494ABE3694BD87D55FFD7576FFDC47C28F94ECC99577DF4FB8FA19AA95764FEF889CDE0F176DA5897B74382FBB22756CE2921050A09201A0EB6AF3D6091014C30146EA62635EE8CBF0A8074DEDFF125CEA80D1C0F5E8C58750A07D270E2A8BF824EE4C0C156366BF26D38CCE49EBDD5639A2DF029A7DBAE5A5D111F2F2FA3246DF8C2FA83C1E542C10570FADA98F6B29478DC58CE5CBDD407CCEFCDB97814525F6F32BECA266014AC346AC39C4F185C6C0F0A24FEC4DFA015649624692DE7865B9827BA22C3B574C9FD169F822B609F902288C5880EB25F14BD990D871B1BC4BA3A5B237AF76D26354773FA2A25CF4511AF58C911E601CFCB1905128C997844EED056C2AE7F0B48700AB41307E470FF9520997D0EB0D887DE11AFE574FFE845B7DC6C03FEEE8D467236368FC0CB2FDBD54DADC65B10B3DE6C80DF8B7B3F8F3CE5BE914713EE7B1FA5B7A578359592B8A5FDFDDE5FF9F392BC87C3CD02FBA94582AC063BBB9FFAC803FD489E16BEB28C4E3374A8478C737236A0B232F5A9DDE4D119573F1AEAE94B2192B81575AD6F57E670C1B2AB91045124DFDAEC2898F3F0112026DFC93BF9391D667D1AD7ED7D4E6BB119BBCEF1D1ADA589DD3E1082C3DAD13223BE438EB9574DA04E9D8A06320CAC6D3EC21D5D1C2A0AA484C7C  
),  
(  
    COLUMN_MASTER_KEY = CMK2,   
    ALGORITHM = 'RSA_OAEP',   
    ENCRYPTED_VALUE = 0x016E000001630075007200720065006E00740075007300650072002F006D0079002F0064006500650063006200660034006100340031003000380034006200350033003200360066003200630062006200350030003600380065003900620061003000320030003600610037003800310066001DDA6134C3B73A90D349C8905782DD819B428162CF5B051639BA46EC69A7C8C8F81591A92C395711493B25DCBCCC57836E5B9F17A0713E840721D098F3F8E023ABCDFE2F6D8CC4339FC8F88630ED9EBADA5CA8EEAFA84164C1095B12AE161EABC1DF778C07F07D413AF1ED900F578FC00894BEE705EAC60F4A5090BBE09885D2EFE1C915F7B4C581D9CE3FDAB78ACF4829F85752E9FC985DEB8773889EE4A1945BD554724803A6F5DC0A2CD5EFE001ABED8D61E8449E4FAA9E4DD392DA8D292ECC6EB149E843E395CDE0F98D04940A28C4B05F747149B34A0BAEC04FFF3E304C84AF1FF81225E615B5F94E334378A0A888EF88F4E79F66CB377E3C21964AACB5049C08435FE84EEEF39D20A665C17E04898914A85B3DE23D56575EBC682D154F4F15C37723E04974DB370180A9A579BC84F6BC9B5E7C223E5CBEE721E57EE07EFDCC0A3257BBEBF9ADFFB00DBF7EF682EC1C4C47451438F90B4CF8DA709940F72CFDC91C6EB4E37B4ED7E2385B1FF71B28A1D2669FBEB18EA89F9D391D2FDDEA0ED362E6A591AC64EF4AE31CA8766C259ECB77D01A7F5C36B8418F91C1BEADDD4491C80F0016B66421B4B788C55127135DA2FA625FB7FD195FB40D90A6C67328602ECAF3EC4F5894BFD84A99EB4753BE0D22E0D4DE6A0ADFEDC80EB1B556749B4A8AD00E73B329C95827AB91C0256347E85E3C5FD6726D0E1FE82C925D3DF4A9  
);  
GO  
```  
  
## <a name="see-also"></a>参照  
 [ALTER COLUMN ENCRYPTION KEY & #40 です。TRANSACT-SQL と #41 です。](../../t-sql/statements/alter-column-encryption-key-transact-sql.md)   
 [列暗号化キー &#40; を削除します。TRANSACT-SQL と #41 です。](../../t-sql/statements/drop-column-encryption-key-transact-sql.md)   
 [CREATE COLUMN MASTER KEY (Transact-SQL)](../../t-sql/statements/create-column-master-key-transact-sql.md)   
 [Always Encrypted &#40;データベース エンジン&#41;](../../relational-databases/security/encryption/always-encrypted-database-engine.md)   
 [sys.column_encryption_keys (Transact-SQL)](../../relational-databases/system-catalog-views/sys-column-encryption-keys-transact-sql.md)   
 [sys.column_encryption_key_values (Transact-SQL)](../../relational-databases/system-catalog-views/sys-column-encryption-key-values-transact-sql.md)   
 [sys.columns &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-columns-transact-sql.md)  
  
  

