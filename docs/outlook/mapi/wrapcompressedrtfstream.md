---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439800"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Textdatenstrom im unkomprimierten Rich Text Format (RTF) aus dem komprimierten Format, das in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parameter

 _lpCompressedRTFStream_
  
> [in] Zeiger auf einen Datenstrom, der auf der PR_RTF_COMPRESSED einer Nachricht geöffnet wird. 
    
 _ulFlags_
  
> [in] Bitmaske von Optionskennzeichen für die Funktion. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_MODIFY 
  
> Gibt an, ob der Client die zurückgegebene umschlossene Streamschnittstelle lesen oder schreiben möchte. 
    
STORE_UNCOMPRESSED_RTF 
  
> Nicht komprimiertes RTF sollte in den Datenstrom geschrieben werden, auf den  _lpCompressedRTFStream verweist_
    
 _lpUncompressedRTFStream_
  
> [out] Zeiger auf den Speicherort, an dem **WrapCompressedRTFStream** einen Datenstrom für die nicht komprimierte RTF zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Wenn das MAPI_MODIFY im  _ulFlags-Parameter_ übergeben wird, muss der  _lpCompressedRTFStream-Parameter_ bereits zum Lesen und Schreiben geöffnet sein. Neuer, nicht komprimierter RTF-Text sollte in die stream-Schnittstelle geschrieben werden, die in _lpUncompressedRTFStream zurückgegeben wird._ Da das Anfügen des vorhandenen Datenstroms nicht möglich ist, muss der gesamte Nachrichtentext geschrieben werden. 
  
Wenn null im  _ulFlags-Parameter_ übergeben wird, wird  _lpCompressedRTFStream_ möglicherweise schreibgeschützt geöffnet. Nur der gesamte Nachrichtentext kann aus der stream-Schnittstelle gelesen werden, die in _lpUncompressedRTFStream zurückgegeben wird._ Es ist nicht möglich, ab der Mitte des Datenstroms zu suchen. 
  
 **WrapCompressedRTFStream** geht davon aus, dass der Zeiger des komprimierten Datenstroms auf den Anfang des Datenstroms festgelegt ist. Bestimmte OLE **IStream-Methoden** werden vom zurückgegebenen nicht komprimierten Datenstrom nicht unterstützt. Dazu gehören **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** und **IStream::UnlockRegion**. Zum Kopieren in den gesamten Datenstrom ist eine Lese-/Schreibschleife erforderlich. 
  
Da der Client neue RTF im unkomprimierten Format schreibt, sollte er **WrapCompressedRTFStream** verwenden, anstatt direkt in den Datenstrom zu schreiben. RTF-bewusste Clients sollten nach dem STORE_UNCOMPRESSED_RTF-Flag in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft suchen und es an **WrapCompressed RTFStream** übergeben, wenn es festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[RTFSync](rtfsync.md)

