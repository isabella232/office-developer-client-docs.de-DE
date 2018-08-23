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
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594593"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Textstream in nicht komprimierten Rich Text Format (RTF) aus der komprimierten Format in der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) verwendet. 
  
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
  
> [in] Zeiger in ein Stream-Objekt auf die PR_RTF_COMPRESSED-Eigenschaft einer Nachricht geöffnet. 
    
 _ulFlags_
  
> [in] Bitmaske der Optionsflags für die Funktion. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_MODIFY 
  
> Gibt an, ob der Client beabsichtigt zum Lesen oder Schreiben der gepackten Stream-Schnittstelle, die zurückgegeben wird. 
    
STORE_UNCOMPRESSED_RTF 
  
> Nicht komprimierten RTF sollte in das Stream-Objekt auf den _LpCompressedRTFStream_ geschrieben werden
    
 _lpUncompressedRTFStream_
  
> [out] Zeiger auf den Speicherort, in dem **WrapCompressedRTFStream** einen Stream für die nicht komprimierten RTF zurückgibt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Wenn das Flag MAPI_MODIFY im _UlFlags_ -Parameter übergeben wird, muss der Parameter _LpCompressedRTFStream_ bereits zum Lesen und Schreiben geöffnet sein. Neue, nicht komprimierten RTF-Text sollte in die Benutzeroberfläche der Stream-Objekt zurückgegeben, die in _LpUncompressedRTFStream_geschrieben werden. Da es nicht möglich, den vorhandenen Stream anzufügen ist, muss der gesamte Nachrichtentext geschrieben werden. 
  
Wenn 0 (null) im _UlFlags_ -Parameter übergeben wird, kann dann _LpCompressedRTFStream_ schreibgeschützt geöffnet werden. Nur der gesamte Nachrichtentext kann über die Stream-Schnittstelle, die in _LpUncompressedRTFStream_zurückgegeben gelesen werden. Es ist nicht möglich, den Suchvorgang starten der Mitte des Stream-Objekts. 
  
 **WrapCompressedRTFStream** wird davon ausgegangen, dass die komprimierte Stream Zeiger an den Anfang des Datenstroms festgelegt ist. Bestimmte OLE **IStream** -Methoden werden von der nicht komprimierten zurückgegebene Stream nicht unterstützt. **IStream:: Clone**, **:: LockRegion**, **:: Revert**, **IStream:: Seek**, **:: setSize**, **:: Stat**und **:: UnlockRegion**beinhalten. Um den gesamten Datenstrom zu kopieren, wird eine Schleife Lese-/Schreibzugriff benötigt. 
  
Da der Client nicht komprimierten Format neue RTF schreibt, sollte **WrapCompressedRTFStream**, anstatt direkt an den Stream schreiben verwendet werden. RTF-fähigen Clients sollte das Flag STORE_UNCOMPRESSED_RTF in der Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) suchen und übergeben es an **WrapCompressed RTFStream** , wenn sie festgelegt ist. 
  
## <a name="see-also"></a>Siehe auch



[RTFSync](rtfsync.md)

