---
title: SQL Server の適用 | Microsoft Docs
ms.custom: ''
ms.date: 07/27/2017
ms.prod: sql
ms.prod_service: sql-tools
ms.component: sqlcmd
ms.reviewer: ''
ms.suite: sql
ms.technology:
- database-engine
caps.latest.revision: 155
author: MashaMSFT
ms.author: mathoma
manager: craigg
monikerRange: '>= aps-pdw-2016 || = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: d9246a20a51a729bcc9427ccde239e30087b59a8
ms.sourcegitcommit: 90a9a051fe625d7374e76cf6be5b031004336f5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2018
ms.locfileid: "39228663"
---
# <a name="sql-applies-to-and-includes"></a>SQL の "Applies to" と "Includes"
ドキュメント内の参照は、Markdown で "Includes" を使用することにより、個々のアーティクルの実際のテキストを変更することなく簡単に変更できます。 SQL のコンテンツには、3 種類のインクルードがあります。SQL のバージョン、applies-to、および参照のテキストです。 SQL のバージョンは、扱っている SQL のバージョンを示すために使用されます (SQL 2016 と 2017 など)。applies-to では、ドキュメントが適用される SQL Server のバージョンが示されます (SQL Server on Linux と Azure SQL Database)。 参照のテキストとは、他の 2 つのカテゴリに該当しないインクルードです。たとえば Get Help インクルード (顧客が SQL でのヘルプを参照するために使用できるリンクの一覧) などです。 

この記事は、最初の 2 種類のインクルードに対する基準点を提供することのみが目的です。 

## <a name="sql-server-version-includes"></a>SQL Server のバージョンのインクルード

SQL のコンテンツの作成者は、製品名や SQL Server のバージョンを含める必要があることが頻繁にあります。 この方法では、名前に変更があると、各アーティクルごとに値を手動で更新する代わりに、インクルードが更新されます。 これらのインクルードは製品名のプレースホルダーとして使用されますが、すべての SQL ドキュメントで一貫して使用されているわけではありません。 SQL Server vNext は、まだバージョン番号を持っておらず、これに対する例外となる SQL の将来のリリースを指します。  

|SQL バージョン| [ファイル名]| Markdown の例 |Text|
| :------------  | :-------------| :----------| :-------------------|
|   SQL 2012    |   sssql11-md.md   |   `[!INCLUDE[ssSQL11](../includes/sssql11-md.md)]`    |   SQL Server 2012 (11.x)  |
|   SQL 2012 SP1    |   sssql11sp1-md.md    |   `[!INCLUDE[ssSQL11SP1](../includes/sssql11sp1-md.md)]`  |   SQL Server 2012 SP1 (11.0.3x)   |
|   SQL 2014    |   sssql14-md.md   |   `[!INCLUDE[ssSQL14](../includes/sssql14-md.md)]`    |   SQL Server 2014 (12.x)  |
|   SQL 2016    |   sssql15-md.md   |   `[!INCLUDE[sssql15-md](../includes/sssql15-md.md)]` |   SQL Server 2016 (13.x)  |
|   SQL 2017    |   sssql17-md.md   |   `[!INCLUDE[sssql17-md](../includes/sssql17-md.md)]` |   SQL Server 2017 (14.x)  |
|   SQL 2017    |   sssqlv14-md.md  |   `[!INCLUDE[sssqlv14](../includes/sssqlv14-md.md)]`  |   SQL Server 2017 (14.x)  |
|   SQL vNext   |   sssqlv15-md.md  |   `[!INCLUDE[sssqlv15-md](../includes/sssqlv14-md.md)]` ? |   SQL Server vNext    |
| &nbsp; | &nbsp; | &nbsp; | &nbsp; |  




## <a name="sql-server-non-version-specific-applies-to"></a>SQL Server バージョン固有ではない applies-to

| [ファイル名]| Markdown の例 |image|
| :-------------| :----------| :-------------------|
| appliesto-ss-asdb-asdw-xxx-md.md  |   `[!INCLUDE[appliesto-ss-asdb-asdw-xxx-md.md](../includes/appliesto-ss-asdb-asdw-xxx-md.md)]`    | [!INCLUDE[appliesto-ss-asdb-asdw-xxx-md.md](../includes/appliesto-ss-asdb-asdw-xxx-md.md)]    |
|   appliesto-ss-asdb-asdw-pdw-md.md    |   `[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md.md](../includes/appliesto-ss-asdb-asdw-pdw-md.md)]`    | [!INCLUDE[appliesto-ss-asdb-asdw-pdw-md.md](../includes/appliesto-ss-asdb-asdw-pdw-md.md)]    |
|   appliesto-ss-asdb-xxxx-pdw-md.md    |   `[!INCLUDE[appliesto-ss-asdb-xxxx-pdw-md.md](../includes/appliesto-ss-asdb-xxxx-pdw-md.md)]`    | [!INCLUDE[appliesto-ss-asdb-xxxx-pdw-md.md](../includes/appliesto-ss-asdb-xxxx-pdw-md.md)]    |
|   appliesto-ss-asdb-xxxx-xxx-md.md    |   `[!INCLUDE[appliesto-ss-asdb-xxxx-xxx-md.md](../includes/appliesto-ss-asdb-xxxx-xxx-md.md)]`    | [!INCLUDE[appliesto-ss-asdb-xxxx-xxx-md.md](../includes/appliesto-ss-asdb-xxxx-xxx-md.md)]    |
|   appliesto-ss-asdbmi-xxxx-xxx-md.md  |   `[!INCLUDE[appliesto-ss-asdbmi-xxxx-xxx-md.md](../includes/appliesto-ss-asdbmi-xxxx-xxx-md.md)]`    | [!INCLUDE[appliesto-ss-asdbmi-xxxx-xxx-md.md](../includes/appliesto-ss-asdbmi-xxxx-xxx-md.md)]    |
|   appliesto-ss-xxxx-asdw-pdw-md.md    |   `[!INCLUDE[appliesto-ss-xxxx-asdw-pdw-md.md](../includes/appliesto-ss-xxxx-asdw-pdw-md.md)]`    | [!INCLUDE[appliesto-ss-xxxx-asdw-pdw-md.md](../includes/appliesto-ss-xxxx-asdw-pdw-md.md)]    |
|   appliesto-ss-xxxx-xxxx-pdw-md.md    |   `[!INCLUDE[appliesto-ss-xxxx-xxxx-pdw-md.md](../includes/appliesto-ss-xxxx-xxxx-pdw-md.md)]`    | [!INCLUDE[appliesto-ss-xxxx-xxxx-pdw-md.md](../includes/appliesto-ss-xxxx-xxxx-pdw-md.md)]    |
|   appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md  |   `[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md)]`    | [!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md)]    |
|   appliesto-ss-xxxx-xxxx-xxx-md-winonly.md    |   `[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]`    | [!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]    |
|   appliesto-ss-xxxx-xxxx-xxx-md.md    |   `[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]`    | [!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md.md](../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]    |
|   appliesto-xx-asdb-asdw-xxx-md.md    |   `[!INCLUDE[appliesto-xx-asdb-asdw-xxx-md.md](../includes/appliesto-xx-asdb-asdw-xxx-md.md)]`    | [!INCLUDE[appliesto-xx-asdb-asdw-xxx-md.md](../includes/appliesto-xx-asdb-asdw-xxx-md.md)]    |
|   appliesto-xx-asdb-xxxx-xxx-md.md    |   `[!INCLUDE[appliesto-xx-asdb-xxxx-xxx-md.md](../includes/appliesto-xx-asdb-xxxx-xxx-md.md)]`    | [!INCLUDE[appliesto-xx-asdb-xxxx-xxx-md.md](../includes/appliesto-xx-asdb-xxxx-xxx-md.md)]    |
|   appliesto-xx-xxxx-asdw-pdw-md.md    |   `[!INCLUDE[appliesto-xx-xxxx-asdw-pdw-md.md](../includes/appliesto-xx-xxxx-asdw-pdw-md.md)]`    | [!INCLUDE[appliesto-xx-xxxx-asdw-pdw-md.md](../includes/appliesto-xx-xxxx-asdw-pdw-md.md)]    |
|   appliesto-xx-xxxx-asdw-xxx-md.md    |   `[!INCLUDE[appliesto-xx-xxxx-asdw-xxx-md.md](../includes/appliesto-xx-xxxx-asdw-xxx-md.md)]`    | [!INCLUDE[appliesto-xx-xxxx-asdw-xxx-md.md](../includes/appliesto-xx-xxxx-asdw-xxx-md.md)]    |
|&nbsp; | &nbsp; | &nbsp; |  
 
## <a name="sql-server-version-specific-applies-to"></a>SQL Server バージョン固有の applies-to
これらの applies-to では、ドキュメントを適用する SQL のバージョンが指定されます。 

 [ファイル名]| Markdown の例 |image|
| :-------------| :----------| :-------------------|
|   tsql-appliesto-2014sp2-asdb-xxxx-xxx-md.md  |   `[!INCLUDE[tsql-appliesto-2014sp2-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-2014sp2-asdb-xxxx-xxx-md.md)]`    | [!INCLUDE[tsql-appliesto-2014sp2-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-2014sp2-asdb-xxxx-xxx-md.md)]    |
|   tsql-appliesto-2016sp2-asdb-xxxx-xxx-md.md  |   `[!INCLUDE[tsql-appliesto-2016sp2-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-2016sp2-asdb-xxxx-xxx-md.md)]`    | [!INCLUDE[tsql-appliesto-2016sp2-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-2016sp2-asdb-xxxx-xxx-md.md)]    |
|   tsql-appliesto-ss2008-all-md.md |   `[!INCLUDE[tsql-appliesto-ss2008-all-md.md](../includes/tsql-appliesto-ss2008-all-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-all-md.md](../includes/tsql-appliesto-ss2008-all-md.md)]  |
|   tsql-appliesto-ss2008-asdb-asdw-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-asdb-asdw-pdw-md.md](../includes/tsql-appliesto-ss2008-asdb-asdw-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-asdb-asdw-pdw-md.md](../includes/tsql-appliesto-ss2008-asdb-asdw-pdw-md.md)]  |
|   tsql-appliesto-ss2008-asdb-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2008-asdb-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2008-asdb-asdw-xxx-md.md)]  |
|   tsql-appliesto-ss2008-asdbmi-xxxx-xxx-md.md |   `[!INCLUDE[tsql-appliesto-ss2008-asdbmi-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-asdbmi-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-asdbmi-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-asdbmi-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2008-asdb-xxxx-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2008-asdb-xxxx-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2008-asdb-xxxx-pdw-md.md)]  |
|   tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-ss2008-xxxx-asdw-pdw-md.md)]  |
|   tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md)]  |
|   tsql-appliesto-ss2008-xxxx-xxxx-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-pdw-md.md)]  |
|   tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2012-all-md.md |   `[!INCLUDE[tsql-appliesto-ss2012-all-md.md](tsql-appliesto-ss2012-all-md.md)]`  | [!INCLUDE[../includes/tsql-appliesto-ss2012-all-md.md](../includes/tsql-appliesto-ss2012-all-md.md)]  |
|   tsql-appliesto-ss2012-asdb-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2012-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2012-asdb-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2012-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2012-asdb-asdw-xxx-md.md)]  |
|   tsql-appliesto-ss2012-asdbmi-xxxx-xxx-md.md |   `[!INCLUDE[tsql-appliesto-ss2012-asdbmi-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-asdbmi-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2012-asdbmi-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-asdbmi-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2012-xxxx-xxxx-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-pdw-md.md)]  |
|   tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2014-asdb-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2016-all-md.md |   `[!INCLUDE[tsql-appliesto-ss2016-all-md.md](tsql-appliesto-ss2016-all-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-all-md.md](../includes/tsql-appliesto-ss2016-all-md.md)]  |
|   tsql-appliesto-ss2016-asdb-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2016-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2016-asdb-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-ss2016-asdb-asdw-xxx-md.md)]  |
|   tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2016-asdb-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2016-xxxx-asdw-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-ss2016-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-ss2016-xxxx-asdw-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-ss2016-xxxx-asdw-pdw-md.md)]  |
|   tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-ss2016-xxxx-asdw-xxx-md.md)]  |
|   tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2016-xxxx-xxxx-xxx-md-winonly.md   |   `[!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md-winonly.md](../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md-winonly.md)]`  | [!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md-winonly.md](../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md-winonly.md)]  |
|   tsql-appliesto-ss2017-xxxx-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2017-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2017-xxxx-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2017-xxxx-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2017-xxxx-xxxx-xxx-md.md)]  |
|   tsql-appliesto-ss2017-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-ss2017-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2017-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-ss2017-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-ss2017-asdb-xxxx-xxx-md.md)]  |
|   t-sql-appliesto-ss-asdbmi-xxxx-pwd-md.md    |   `[!INCLUDE[t-sql-appliesto-ss-asdbmi-xxxx-pwd-md.md](../includes/t-sql-appliesto-ss-asdbmi-xxxx-pwd-md.md)]`    | [!INCLUDE[t-sql-appliesto-ss-asdbmi-xxxx-pwd-md.md](../includes/t-sql-appliesto-ss-asdbmi-xxxx-pwd-md.md)]    |
|   tsql-appliesto-xxxxxx-asdb-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-xxxxxx-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-xxxxxx-asdb-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-xxxxxx-asdb-asdw-xxx-md.md](../includes/tsql-appliesto-xxxxxx-asdb-asdw-xxx-md.md)]  |
|   tsql-appliesto-xxxxxx-asdb-xxxx-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-xxxxxx-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-xxxxxx-asdb-xxxx-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-xxxxxx-asdb-xxxx-xxx-md.md](../includes/tsql-appliesto-xxxxxx-asdb-xxxx-xxx-md.md)]  |
|   tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-asdw-pdw-md.md)]  |
|   tsql-appliesto-xxxxxx-xxxx-asdw-xxx-md.md   |   `[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-asdw-xxx-md.md)]`  | [!INCLUDE[tsql-appliesto-xxxxxx-xxxx-asdw-xxx-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-asdw-xxx-md.md)]  |
|   tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md   |   `[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md)]`  | [!INCLUDE[tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md](../includes/tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md)]  |
|&nbsp; | &nbsp; | &nbsp; |  

## <a name="analysis-services-applies-to"></a>Analysis Services の applies-to

| [ファイル名]| Markdown の例 |image|
| :-------------| :----------| :-------------------|
|   ssas-appliesto-sql2016.md   |   `[!INCLUDE[ssas-appliesto-sql2016.md](../includes/ssas-appliesto-sql2016.md)]`  | [!INCLUDE[ssas-appliesto-sql2016.md](../includes/ssas-appliesto-sql2016.md)]  |
|   ssas-appliesto-sql2016-later.md |   `[!INCLUDE[ssas-appliesto-sql2016-later.md](../includes/ssas-appliesto-sql2016-later.md)]`  | [!INCLUDE[ssas-appliesto-sql2016-later.md](../includes/ssas-appliesto-sql2016-later.md)]  |
|   ssas-appliesto-sql2016-later-aas.md |   `[!INCLUDE[ssas-appliesto-sql2016-later-aas.md](../includes/ssas-appliesto-sql2016-later-aas.md)]`  | [!INCLUDE[ssas-appliesto-sql2016-later-aas.md](../includes/ssas-appliesto-sql2016-later-aas.md)]  |
|   ssas-appliesto-sql2017.md   |   `[!INCLUDE[ssas-appliesto-sql2017.md](../includes/ssas-appliesto-sql2017.md)]`  | [!INCLUDE[ssas-appliesto-sql2017.md](../includes/ssas-appliesto-sql2017.md)]  |
|   ssas-appliesto-sql2017-later-aas.md |   `[!INCLUDE[ssas-appliesto-sql2017-later-aas.md](../includes/ssas-appliesto-sql2017-later-aas.md)]`  | [!INCLUDE[ssas-appliesto-sql2017-later-aas.md](../includes/ssas-appliesto-sql2017-later-aas.md)]  |
|   ssas-appliesto-sqlas.md |   `[!INCLUDE[ssas-appliesto-sqlas.md](../includes/ssas-appliesto-sqlas.md)]`  | [!INCLUDE[ssas-appliesto-sqlas.md](../includes/ssas-appliesto-sqlas.md)]  |
|   ssas-appliesto-sqlas-aas.md |   `[!INCLUDE[ssas-appliesto-sqlas-aas.md](../includes/ssas-appliesto-sqlas-aas.md)]`  | [!INCLUDE[ssas-appliesto-sqlas-aas.md](../includes/ssas-appliesto-sqlas-aas.md)]  |
|   ssas-appliesto-sqlas-all.md |   `[!INCLUDE[ssas-appliesto-sqlas-all.md](../includes/ssas-appliesto-sqlas-all.md)]`  | [!INCLUDE[ssas-appliesto-sqlas-all.md](../includes/ssas-appliesto-sqlas-all.md)]  |
|   ssas-appliesto-sqlas-all-aas.md |   `[!INCLUDE[ssas-appliesto-sqlas-all-aas.md](../includes/ssas-appliesto-sqlas-all-aas.md)]`  | [!INCLUDE[ssas-appliesto-sqlas-all-aas.md](../includes/ssas-appliesto-sqlas-all-aas.md)]  |
|&nbsp; | &nbsp; | &nbsp; |  

## <a name="reporting-services-applies-to"></a>Reporting Services の applies-to

| [ファイル名]| Markdown の例 |image|
| :-------------| :----------| :-------------------|
|   ssrs-appliesto-2017-and-later.md    |   `[!INCLUDE[ssrs-appliesto-2017-and-later.md](../includes/ssrs-appliesto-2017-and-later.md)]`    | [!INCLUDE[ssrs-appliesto-2017-and-later.md](../includes/ssrs-appliesto-2017-and-later.md)]    |
|   ssrs-appliesto-not-pbirs.md |   `[!INCLUDE[ssrs-appliesto-not-pbirs.md](../includes/ssrs-appliesto-not-pbirs.md)]`  | [!INCLUDE[ssrs-appliesto-not-pbirs.md](../includes/ssrs-appliesto-not-pbirs.md)]  |
|   ssrs-appliesto-pbirs.md |   `[!INCLUDE[ssrs-appliesto-pbirs.md](../includes/ssrs-appliesto-pbirs.md)]`  | [!INCLUDE[ssrs-appliesto-pbirs.md](../includes/ssrs-appliesto-pbirs.md)]  |
|   ssrs-appliesto-sharepoint-2013-2016.md  |   `[!INCLUDE[ssrs-appliesto-sharepoint-2013-2016.md](../includes/ssrs-appliesto-sharepoint-2013-2016.md)]`    | [!INCLUDE[ssrs-appliesto-sharepoint-2013-2016.md](../includes/ssrs-appliesto-sharepoint-2013-2016.md)]    |
|   ssrs-appliesto-sql2016-preview.md   |   `[!INCLUDE[ssrs-appliesto-sql2016-preview.md](../includes/ssrs-appliesto-sql2016-preview.md)]`  | [!INCLUDE[ssrs-appliesto-sql2016-preview.md](../includes/ssrs-appliesto-sql2016-preview.md)]  |
|&nbsp; | &nbsp; | &nbsp; |  