---
title: ADO オブジェクトとインターフェイス |Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- ADO, objects and interfaces
- objects [ADO]
ms.assetid: d0b7e254-c89f-4406-b846-a060ef038c30
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: f0bba8402bb49d481886e4c81071443873834c8c
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47660650"
---
# <a name="ado-objects-and-interfaces"></a>ADO のオブジェクトとインターフェイス
これらのオブジェクト間のリレーションシップが表現されて、 [ADO オブジェクト モデル](../../../ado/reference/ado-api/ado-object-model.md)します。  
  
 各オブジェクトは、対応するコレクションに格納できます。 たとえば、[エラー](../../../ado/reference/ado-api/error-object.md)オブジェクトを含めることができます、[エラー](../../../ado/reference/ado-api/errors-collection-ado.md)コレクション。 詳細については、次を参照してください。 [ADO コレクション](../../../ado/reference/ado-api/ado-collections.md)」、または特定のコレクション。  
  
|||  
|-|-|  
|[IADOCommandConstruction](https://msdn.microsoft.com/library/windows/desktop/aa965677.aspx)|ADOCommand オブジェクトから基になる ole DB コマンドを取得するために使用します。|  
|[ADORecordConstruction](../../../ado/reference/ado-api/adorecordconstruction-interface.md)|ADO を構築します**レコード**から OLE DB オブジェクト**行**C/C++ アプリケーション内のオブジェクト。|  
|[ADORecordsetConstruction](../../../ado/reference/ado-api/adorecordsetconstruction-interface.md)|ADO を構築します**Recordset**から OLE DB オブジェクト**行セット**C/C++ アプリケーション内のオブジェクト。|  
|[ADOStreamConstruction インターフェイス](../../../ado/reference/ado-api/adostreamconstruction-interface.md)|ADO を構築します**Stream**から OLE DB オブジェクト**IStream** C/C++ アプリケーション内のオブジェクト。|  
|[Command](../../../ado/reference/ado-api/command-object-ado.md)|データ ソースに対して実行する特定のコマンドを定義します。<br /><br /> **コマンド**オブジェクトは、スクリプトを実行することはありません。|  
|[Connection](../../../ado/reference/ado-api/connection-object-ado.md)|データ ソースへの接続を開くを表します。<br /><br /> **接続**オブジェクトがスクリプトを実行します。|  
|[IDSOShapeExtensions インターフェイス](../../../ado/reference/ado-api/idsoshapeextensions-interface.md)|SHAPE プロバイダーの基になる ole DB データ ソース オブジェクトを取得します。|  
|[Error](../../../ado/reference/ado-api/error-object.md)|プロバイダーを含む 1 つの操作に関連するデータ アクセス エラーの詳細が含まれています。<br /><br /> **エラー**オブジェクトは、スクリプトを実行することはありません。|  
|[フィールド](../../../ado/reference/ado-api/field-object.md)|一般的なデータ型のデータの列を表します。|  
|[パラメーター](../../../ado/reference/ado-api/parameter-object.md)|パラメーターまたはに関連付けられている引数を表します、**コマンド**オブジェクトがパラメーター化クエリまたはストアド プロシージャに基づいています。<br /><br /> **パラメーター**オブジェクトは、スクリプトを実行することはありません。|  
|[プロパティ](../../../ado/reference/ado-api/property-object-ado.md)|プロバイダーによって定義されている ADO オブジェクトの動的な特性を表します。|  
|[レコード](../../../ado/reference/ado-api/record-object-ado.md)|行を表します、 **Recordset**、ディレクトリまたはファイル システム内のファイル。 **レコード**オブジェクトがスクリプトを実行します。|  
|[レコード セット](../../../ado/reference/ado-api/recordset-object-ado.md)|ベース テーブル、またはコマンドの実行の結果からレコード セットを表します。 いつでもでも、 **Recordset**オブジェクトとして現在のレコード セット内で 1 つのレコードのみを参照します。<br /><br /> **Recordset**オブジェクトがスクリプトを実行します。|  
|[ストリーム](../../../ado/reference/ado-api/stream-object-ado.md)|データのバイナリ ストリームを表します。<br /><br /> **Stream**オブジェクトがスクリプトを実行します。|  
  
## <a name="see-also"></a>参照  
 [ADO の API リファレンス](../../../ado/reference/ado-api/ado-api-reference.md)   
 [ADO のコレクション](../../../ado/reference/ado-api/ado-collections.md)   
 [ADO の動的プロパティ](../../../ado/reference/ado-api/ado-dynamic-properties.md)   
 [ADO の列挙定数](../../../ado/reference/ado-api/ado-enumerated-constants.md)   
 [付録 b: ADO エラー](../../../ado/guide/appendixes/appendix-b-ado-errors.md)   
 [ADO イベント](../../../ado/reference/ado-api/ado-events.md)   
 [ADO メソッド](../../../ado/reference/ado-api/ado-methods.md)   
 [ADO オブジェクト モデル](../../../ado/reference/ado-api/ado-object-model.md)   
 [ADO のプロパティ](../../../ado/reference/ado-api/ado-properties.md)
