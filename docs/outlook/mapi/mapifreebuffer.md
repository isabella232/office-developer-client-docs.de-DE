---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b952e6a62af99f9aa1a1afd0ec96102e54318c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556077"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Speicherpuffer frei, der mit einem Aufruf der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) oder der [MAPIAllocateMore-Funktion](mapiallocatemore.md) zugeordnet ist. 
  
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
  
> [in] Zeiger auf einen zuvor zugewiesenen Speicherpuffer. Wenn NULL im  _lpBuffer-Parameter_ übergeben wird, führt **MAPIFreeBuffer** keine Aktion aus. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den angeforderten Speicher freigegeben. **MAPIFreeBuffer** kann auch S_OK an bereits freigegebenen Speicherorten zurückgeben oder wenn der Speicherblock nicht mit **MAPIAllocateBuffer** und **MAPIAllocateMore** zugeordnet ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine Clientanwendung oder ein Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md)aufruft, erstellt das Betriebssystem in einem zusammenhängenden Speicherpuffer eine oder mehrere komplexe Strukturen mit mehreren Zeigerebenen. Wenn eine MAPI-Funktion oder -Methode einen Puffer mit einem solchen Inhalt erstellt, kann ein Client später alle im Puffer enthaltenen Strukturen freigeben, indem er den Zeiger an **MAPIFreeBuffer** an den Puffer übergibt, der von der MAPI-Funktion zurückgegeben wird, die den Puffer erstellt hat. Damit ein Dienstanbieter einen Speicherpuffer mit **MAPIFreeBuffer** freigibt, muss er den Zeiger an diesen Puffer übergeben, der mit dem Supportobjekt des Anbieters zurückgegeben wird. 
  
Der Aufruf von **MAPIFreeBuffer** zum Freigeben eines bestimmten Puffers muss erfolgen, sobald ein Client oder Anbieter diesen Puffer nicht mehr verwendet. Durch den einfachen Aufruf der [IMAPISession::Logoff-Methode](imapisession-logoff.md) am Ende einer MAPI-Sitzung werden keine Speicherpuffer automatisch freigegeben. 
  
Ein Client oder Dienstanbieter sollte davon ausgehen, dass der in  _lpBuffer_ übergebene Zeiger nach einer erfolgreichen Rückgabe von **MAPIFreeBuffer** ungültig ist. Wenn der Zeiger entweder einen Speicherblock angibt, der nicht vom Messagingsystem über **MAPIAllocateBuffer** oder **MAPIAllocateMore** oder einen freien Speicherblock zugewiesen wurde, ist das Verhalten von **MAPIFreeBuffer** nicht definiert. 
  
> [!NOTE]
> Das Übergeben eines NULL-Zeigers an **MAPIFreeBuffer** macht den Anwendungsbereinigungscode einfacher und kleiner, da **MAPIFreeBuffer** Zeiger auf NULL initialisieren und sie dann im Bereinigungscode freigeben kann, ohne sie zuerst testen zu müssen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

