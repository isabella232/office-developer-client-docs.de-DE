---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410553"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Speicherpuffer frei, der mit einem Aufruf der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) oder der [MAPIAllocateMore-Funktion zugewiesen](mapiallocatemore.md) wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parameter

 _lpBuffer_
  
> [in] Zeiger auf einen zuvor zugewiesenen Speicherpuffer. Wenn NULL im  _lpBuffer-Parameter_ übergeben wird, führt **MAPIFreeBuffer** nichts aus. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und der angeforderte Arbeitsspeicher wurde frei. **MAPIFreeBuffer** kann auch S_OK bereits frei werdende Speicherorte zurückgeben oder wenn der Speicherblock nicht mit **MAPIAllocateBuffer** und **MAPIAllocateMore** zugewiesen ist.
    
## <a name="remarks"></a>Hinweise

Wenn eine Clientanwendung oder ein Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md)aufruft, erstellt das Betriebssystem in einem zusammenhängenden Speicherpuffer eine oder mehrere komplexe Strukturen mit mehreren Zeigerebenen. Wenn eine MAPI-Funktion oder -Methode einen Puffer mit solchen Inhalten erstellt, kann ein Client später alle im Puffer enthaltenen Strukturen frei, indem er den Zeiger an **MAPIFreeBuffer** übergeben, der von der MAPI-Funktion zurückgegeben wird, von der der Puffer erstellt wurde. Damit ein Dienstanbieter einen Speicherpuffer mit **MAPIFreeBuffer** frei geben kann, muss er den Zeiger an diesen Puffer übergeben, der mit dem Supportobjekt des Anbieters zurückgegeben wird. 
  
Der Aufruf von **MAPIFreeBuffer** zum Freispeichern eines bestimmten Puffers muss ausgeführt werden, sobald ein Client oder Anbieter diesen Puffer verwendet hat. Durch einfaches Aufrufen der [IMAPISession::Logoff-Methode](imapisession-logoff.md) am Ende einer MAPI-Sitzung werden speicherpuffer nicht automatisch freigegeben. 
  
Ein Client oder Dienstanbieter sollte davon ausgehen, dass der in _lpBuffer_ übergebene Zeiger nach einer erfolgreichen Rückgabe von **MAPIFreeBuffer ungültig ist.** Wenn der Zeiger entweder einen vom Messagingsystem nicht über **MAPIAllocateBuffer** oder **MAPIAllocateMore** zugewiesenen Speicherblock oder einen freien Speicherblock angibt, ist das Verhalten von **MAPIFreeBuffer** nicht definiert. 
  
> [!NOTE]
> Wenn Sie einen Nullzeiger an **MAPIFreeBuffer** übergeben, wird der Anwendungsbereinigungscode einfacher und kleiner, da **MAPIFreeBuffer** Zeiger auf NULL initialisieren und dann im Bereinigungscode freiräumen kann, ohne sie zuerst testen zu müssen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

