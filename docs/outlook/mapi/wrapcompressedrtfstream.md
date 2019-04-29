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
  
Erstellt einen Textstream im unkomprimierten Rich-Text-Format (RTF) aus dem komprimierten Format, das in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parameter

 _lpCompressedRTFStream_
  
> in Zeiger auf einen Stream, der für die PR_RTF_COMPRESSED-Eigenschaft einer Nachricht geöffnet wird. 
    
 _ulFlags_
  
> in Bitmaske von Options-Flags für die Funktion. Die folgenden Flags können festgelegt werden:
    
MAPI_MODIFY 
  
> Gibt an, ob der Client die eingebundene Datenstromschnittstelle lesen oder schreiben möchte, die zurückgegeben wird. 
    
STORE_UNCOMPRESSED_RTF 
  
> Unkomprimiertes RTF sollte in den Stream geschrieben werden, auf den durch _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> Out Zeiger auf die Position, an der **WrapCompressedRTFStream** einen Stream für das unkomprimiert RTF zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Wenn das MAPI_MODIFY-Flag im _ulFlags_ -Parameter übergeben wird, muss der _lpCompressedRTFStream_ -Parameter bereits zum Lesen und Schreiben geöffnet sein. Neuer, nicht komprimierter RTF-Text sollte in die in _lpUncompressedRTFStream_zurückgegebene Stream-Schnittstelle geschrieben werden. Da der vorhandene Stream nicht angefügt werden kann, muss der gesamte Nachrichtentext geschrieben werden. 
  
Wenn NULL im _ulFlags_ -Parameter übergeben wird, kann _lpCompressedRTFStream_ schreibgeschützt geöffnet werden. Nur der gesamte Nachrichtentext kann aus der in _lpUncompressedRTFStream_zurückgegebenen Stream-Schnittstelle ausgelesen werden. Es ist nicht möglich, in der Mitte des Streams zu suchen. 
  
 **WrapCompressedRTFStream** geht davon aus, dass der Zeiger des komprimierten Streams auf den Anfang des Streams festgelegt ist. Bestimmte OLE **IStream** -Methoden werden vom zurückgegebenen unkomprimierten Stream nicht unterstützt. Hierzu gehört **IStream:: Clone**, **IStream**:: LockRegion, **IStream:: Revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: stat**und **IStream:: UnlockRegion**. Zum Kopieren in den gesamten Stream ist eine Read/Write-Schleife erforderlich. 
  
Da der Client neues RTF im unkomprimierten Format schreibt, sollte es **WrapCompressedRTFStream**verwenden, statt direkt in den Stream zu schreiben. RTF-fähige Clients sollten in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft nach dem STORE_UNCOMPRESSED_RTF-Flag suchen und es an **WrapCompressed RTFStream** weitergeben, wenn es festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[RTFSync](rtfsync.md)

