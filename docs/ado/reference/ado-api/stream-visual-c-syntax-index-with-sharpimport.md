---
title: 'Stream (Visual C 構文のインデックスで #import) |Microsoft Docs'
ms.prod: sql
ms.prod_service: connectivity
ms.technology: connectivity
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
dev_langs:
- C++
helpviewer_keywords:
- Stream collection [ADO]
ms.assetid: e59d0687-1f5a-45c5-9d0a-c1f27079495d
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: 9b66a3549fde85f7806443a0cf5fa1299739e6f7
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2018
ms.locfileid: "47663200"
---
# <a name="stream-visual-c-syntax-index-with-import"></a>Stream (Visual C 構文のインデックスで #import)
## <a name="methods"></a>メソッド  
  
```  
HRESULT Cancel( );  
  
HRESULT Close( );  
  
HRESULT CopyTo( struct _Stream * DestStream, int CharNumber );  
  
HRESULT Flush( );  
  
HRESULT LoadFromFile( _bstr_t FileName );  
  
HRESULT Open( const _variant_t & Source, enum  
    ConnectModeEnum Mode, enum     StreamOpenOptionsEnum Options, _bstr_t  
    UserName, _bstr_t Password );  
  
_variant_t Read( long NumBytes );  
  
_bstr_t ReadText( long NumChars );  
  
HRESULT SaveToFile( _bstr_t FileName, enum SaveOptionsEnum  
    Options );  
  
HRESULT SetEOS( );  
  
HRESULT SkipLine( );  
  
HRESULT Write( const _variant_t & Buffer );  
  
HRESULT WriteText( _bstr_t Data, enum StreamWriteEnum  
    Options );  
```  
  
## <a name="properties"></a>[プロパティ]  
  
```  
_bstr_t GetCharset( );  
void PutCharset( _bstr_t pbstrCharset );  
__declspec(property(get=GetCharset,put=PutCharset)) _bstr_t Charset;  
  
VARIANT_BOOL GetEOS( );  
__declspec(property(get=GetEOS)) VARIANT_BOOL EOS;  
  
enum LineSeparatorEnum GetLineSeparator( );  
void PutLineSeparator( enum LineSeparatorEnum pLS );  
__declspec(property(get=GetLineSeparator,put=PutLineSeparator)) enum  
    LineSeparatorEnum LineSeparator;  
  
enum ConnectModeEnum GetMode( );  
void PutMode( enum ConnectModeEnum pMode );  
__declspec(property(get=GetMode,put=PutMode)) enum ConnectModeEnum Mode;  
  
long GetPosition( );  
void PutPosition( long pPos );  
__declspec(property(get=GetPosition,put=PutPosition)) long Position;  
  
long GetSize( );  
__declspec(property(get=GetSize)) long Size;  
  
enum ObjectStateEnum GetState( );  
__declspec(property(get=GetState)) enum ObjectStateEnum State;  
  
enum StreamTypeEnum GetType( );  
void PutType( enum StreamTypeEnum ptype );  
__declspec(property(get=GetType,put=PutType)) enum StreamTypeEnum Type;  
```  
  
## <a name="see-also"></a>参照  
 [Stream オブジェクト (ADO)](../../../ado/reference/ado-api/stream-object-ado.md)
