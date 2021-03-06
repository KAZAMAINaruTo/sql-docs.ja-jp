---
title: 共有データ ソースを作成、変更、および削除する (SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 03/07/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- reporting-services-native
ms.topic: conceptual
helpviewer_keywords:
- modifying data source properties
- shared data sources [Reporting Services]
- removing shared data sources
- roles [Reporting Services], shared data sources
- data sources [Reporting Services], shared
- data sources [Reporting Services], modifying properties
- deleting shared data sources
ms.assetid: 1e58c1c2-5ecf-4ce6-9d04-0a8acfba17be
author: markingmyname
ms.author: maghan
manager: craigg
ms.openlocfilehash: 2757c13236b871eccc91066e064924c27cc19a93
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48056812"
---
# <a name="create-modify-and-delete-shared-data-sources-ssrs"></a>共有データ ソースを作成、変更、および削除する (SSRS)
  共有データ ソースは、 [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] レポート サーバーで実行される複数のレポート、モデル、およびデータ ドリブン サブスクリプションから参照できる一連のデータ ソース接続プロパティの集まりです。 共有データ ソースを使用することで、時間の経過に伴って変更されることの多いデータ ソースのプロパティを容易に管理できます。 ユーザーのアカウントまたはパスワードが変更された場合や、データベースを別のサーバーに移動した場合は、接続情報を 1 か所で更新できます。  
  
 共有データ ソースは、レポートおよびデータ ドリブン サブスクリプションでは省略可能ですが、レポート モデルでは必須です。 カスタム レポート用のレポート モデルを使用する予定がある場合は、そのモデルへの接続情報を提供する共有データ ソース アイテムを作成および管理する必要があります。  
  
 共有データ ソースは、次の要素で構成されます。  
  
|要素|説明|  
|----------|-----------------|  
|名前|レポート サーバーのフォルダー階層内にあるアイテムを識別する名前。|  
|説明|レポート マネージャーでフォルダーの内容を参照したときに、アイテムと共に表示される説明です。|  
|接続の種類|データ ソースで使用するデータ処理拡張機能です。 レポート サーバーに配置されているデータ処理拡張機能のみ使用できます。 [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] に含まれているデータ処理拡張機能については、「[Reporting Services でサポートされるデータ ソース &#40;SSRS&#41;](../create-deploy-and-manage-mobile-and-paginated-reports.md)」を参照してください。|  
|[接続文字列]|データベースの接続文字列です。 詳細については、および頻繁に使用されるデータ ソースへの接続文字列の例を表示するのには、「[データ接続、データ ソース、および Reporting Services の接続文字列](../data-connections-data-sources-and-connection-strings-in-reporting-services.md)します。|  
|資格情報の種類|接続に必要な資格情報をどのように取得するか、および、接続の確立後もそれらを使用するかどうかを指定します。 詳細については、次を参照してください。[資格情報の指定とレポート データ ソースに関する接続情報](../../integration-services/connection-manager/data-sources.md)します。|  
  
 共有データ ソースには、データの取得に使用するクエリ情報が含まれません。 クエリは、常にレポート定義内に保持されます。  
  
## <a name="creating-and-modifying-a-shared-data-source"></a>共有データ ソースの作成と変更  
 共有データ ソースの作成や、そのプロパティの変更を行うには、レポート サーバーにおける **データ ソースの管理** 権限が必要です。 レポート サーバーをネイティブ モードで実行している場合は、レポート マネージャーを使用して、共有データ ソースの作成と構成を行うことができます。 レポート サーバーを SharePoint 統合モードで実行している場合は、SharePoint サイトのアプリケーション ページを使用できます。 モードに関係なくどのレポート サーバーでも、レポート デザイナーで共有データ ソースを作成し、それをターゲット サーバーにパブリッシュできます。  
  
 共有データ ソースの作成の詳細については、次のトピックを参照してください。  
  
-   [埋め込みまたは共有データ ソースを作成&#40;SSRS&#41;](../create-an-embedded-or-shared-data-source-ssrs.md)  
  
-   [共有データ ソースを作成および管理する &#40;Reporting Services の SharePoint 統合モード&#41;](../create-manage-shared-data-sources-reporting-services-sharepoint-integrated-mode.md)  
  
 レポート サーバーに共有データ ソースを作成した後は、その共有データ ソースに対するアクセスを制御するためのロール割り当てを作成できるほか、共有データ ソースを別の場所に移動したり、名前を変更したりできます。また、外部データ ソースでメンテナンス操作を実行しているときに、共有データ ソースをオフラインにして、レポート処理が行われないようにすることもできます。 共有データ ソース アイテムの名前を変更したり、レポート サーバーのフォルダー階層内の別の場所に共有データ ソース アイテムを移動すると、共有データ ソースを参照するすべてのレポートまたはサブスクリプションのパス情報が適宜更新されます。 共有データ ソースをオフラインにした場合、再度データ ソースを有効にするまで、レポート、モデル、およびサブスクリプションはすべて実行されなくなります。  
  
 レポート サーバーのフォルダー階層で共有データ ソースへのアクセスを制御する方法の詳細については、「 [共有データ ソース アイテムをセキュリティで保護する](../security/secure-shared-data-source-items.md)」を参照してください。  
  
## <a name="deleting-a-shared-data-source"></a>共有データ ソースを削除します。  
 共有データ ソースは、レポート サーバーからアイテムを削除するときと同じ方法で削除できます。 レポート マネージャーでフォルダーを開き、詳細ビューで、項目を選択 をクリックして**削除**します。 SharePoint サイトでアプリケーション ページでは、開いて、SharePoint ライブラリ、アイテムを選択する をクリックして**削除**します。  
  
 共有データ ソースを削除すると、それを使用しているレポート、モデル、またはデータ ドリブン サブスクリプションがすべて非アクティブ化されます。 データ ソース接続情報がなければ、アイテムを実行することはできません。 これらのアイテムをアクティブ化するには、各アイテムを開いて、以下の操作を行います。  
  
-   共有データ ソースを参照するレポートおよびデータ ドリブン サブスクリプションの場合は、レポートのプロパティまたはサブスクリプションでデータ ソース接続情報を指定するか、必要な値が設定された新しい共有データ ソースを選択できます。  
  
-   モデルや、そのモデルを使用するレポート ビルダー レポートの場合は、新しい共有データ ソースを指定する必要があります。 モデルでは、データ ソース接続情報が、共有データ ソースからのみ取得されます。  
  
 特定のデータ ソースを使用しているレポートおよびモデルの一覧を表示するには、共有データ ソースの [依存アイテム] ページを開きます。 このページには、レポート マネージャーまたは SharePoint のアプリケーション ページでデータ ソースを開くことによってアクセスできます。 [依存アイテム] ページにはデータ ドリブン サブスクリプションが表示されない点に注意してください。 共有データ ソースがサブスクリプションで使用されている場合、[依存アイテム] の一覧には、そのサブスクリプションが表示されません。  
  
 共有データ ソースの削除操作を元に戻すことはできません。 ただし、共有データ ソースをうっかり削除してしまったとしても、削除したデータ ソースと同じプロパティ値で新たに作成し直すことは可能です。 レポート、モデル、またはデータ ドリブン サブスクリプションを 1 つずつ開いて、共有データ ソースと、それを使用しているアイテムとを再バインドする必要はありますが、データ ソースのプロパティが以前と同じであれば、引き続き以前と同じようにそれらを使用できます。  
  
## <a name="see-also"></a>参照  
 [作成および共有データ ソースの管理&#40;Reporting Services の SharePoint 統合モード&#41;](../create-manage-shared-data-sources-reporting-services-sharepoint-integrated-mode.md)   
 [データ接続、データ ソース、および Reporting Services の接続文字列](../data-connections-data-sources-and-connection-strings-in-reporting-services.md)   
 [レポート データ ソースを管理します。](manage-report-data-sources.md)   
 [レポート マネージャー &#40;SSRS ネイティブ モード&#41;](../report-manager-ssrs-native-mode.md)   
 [埋め込みし、共有データ接続またはデータ ソース&#40;レポート ビルダーおよび SSRS&#41;](../embedded-and-shared-data-connections-or-data-sources-report-builder-and-ssrs.md)   
 [[データ ソース] プロパティ ページ &#40;レポート マネージャー&#41;](../data-sources-properties-page-report-manager.md)   
 [作成、削除、または共有データ ソース変更&#40;レポート マネージャー&#41;](../create-delete-or-modify-a-shared-data-source-report-manager.md)   
 [レポートのデータ ソースのプロパティを構成する&#40;レポート マネージャー&#41;](configure-data-source-properties-for-a-report-report-manager.md)  
  
  
