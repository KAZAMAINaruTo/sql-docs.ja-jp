---
title: "ストリーム (Visual C++ 構文のインデックス #import) |Microsoft ドキュメント"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
dev_langs:
- C++
helpviewer_keywords:
- Stream collection [ADO]
ms.assetid: e59d0687-1f5a-45c5-9d0a-c1f27079495d
caps.latest.revision: 10
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 77c960197a8439127820c8d1b5e8f807d5b0e1fd
ms.contentlocale: ja-jp
ms.lasthandoff: 09/09/2017

---
# <a name="stream-visual-c-syntax-index-with-import"></a>ストリーム (Visual C++ 構文のインデックス #import)
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
 [ストリーム オブジェクト (ADO)](../../../ado/reference/ado-api/stream-object-ado.md)
