---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af4c5b0305f8de8b31ca54747db2d3faed68131f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609187"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Textdatenstrom im nicht komprimierten Rich-Text-Format (RTF) aus dem komprimierten Format, das in der **eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) verwendet wird. 
  
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
  
> [in] Zeiger auf einen Datenstrom, der in der PR_RTF_COMPRESSED Eigenschaft einer Nachricht geöffnet ist. 
    
 _ulFlags_
  
> [in] Bitmaske von Optionsflags für die Funktion. Die folgenden Flags können festgelegt werden:
    
MAPI_MODIFY 
  
> Gibt an, ob der Client die zurückgegebene umschlossene Datenstromschnittstelle lesen oder schreiben möchte. 
    
STORE_UNCOMPRESSED_RTF 
  
> Nicht komprimiertes RTF sollte in den Stream geschrieben werden, auf den von _lpCompressedRTFStream_ verwiesen wird.
    
 _lpUncompressedRTFStream_
  
> [out] Zeiger auf die Position, an der **WrapCompressedRTFStream** einen Datenstrom für das nicht komprimierte RTF zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das MAPI_MODIFY Flag im  _ulFlags-Parameter_ übergeben wird, muss der  _Parameter lpCompressedRTFStream_ bereits zum Lesen und Schreiben geöffnet sein. Neuer, nicht komprimierter RTF-Text sollte in die Streamschnittstelle geschrieben werden, die in  _lpUncompressedRTFStream_ zurückgegeben wird. Da es nicht möglich ist, den vorhandenen Datenstrom anzufügen, muss der gesamte Nachrichtentext geschrieben werden. 
  
Wenn null im  _ulFlags-Parameter_ übergeben wird, kann  _lpCompressedRTFStream_ schreibgeschützt geöffnet werden. Nur der gesamte Nachrichtentext kann aus der Streamschnittstelle gelesen werden, die in  _lpUncompressedRTFStream_ zurückgegeben wird. Es ist nicht möglich, beginnend mit der Mitte des Datenstroms zu suchen. 
  
 **WrapCompressedRTFStream** geht davon aus, dass der Zeiger des komprimierten Datenstroms auf den Anfang des Datenstroms festgelegt ist. Bestimmte OLE **IStream-Methoden** werden vom zurückgegebenen nicht komprimierten Stream nicht unterstützt. Dazu gehören **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** und **IStream::UnlockRegion**. Um in den gesamten Datenstrom zu kopieren, ist eine Lese-/Schreibschleife erforderlich. 
  
Da der Client neue RTF im nicht komprimierten Format schreibt, sollte **wrapCompressedRTFStream** verwendet werden, anstatt direkt in den Stream zu schreiben. RTF-fähige Clients sollten nach dem STORE_UNCOMPRESSED_RTF Flag in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) suchen und es an **WrapCompressed RTFStream** übergeben, wenn es festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[RTFSync](rtfsync.md)

