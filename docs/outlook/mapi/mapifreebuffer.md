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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346662"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Speicherpuffer frei, der mit einem Aufruf der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion oder der [MAPIAllocateMore](mapiallocatemore.md) -Funktion reserviert wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parameter

 _lpBuffer_
  
> in Zeiger auf einen zuvor reservierten Speicherpuffer. Wenn NULL im _lpBuffer_ -Parameter übergeben wird, bewirkt **mapifreebufferfreigegeben** nichts. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf wurde erfolgreich durchgeführt und der angeforderte Arbeitsspeicher freigegeben. **Mapifreebufferfreigegeben** kann auch S_OK auf bereits freigegebenen Speicherorten zurückgeben oder wenn der Speicherblock nicht mit **MAPIAllocateBuffer** und **MAPIAllocateMore**zugeordnet ist.
    
## <a name="remarks"></a>Bemerkungen

Wenn eine Clientanwendung oder ein Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md)aufruft, erstellt das Betriebssystem in der Regel eine oder mehrere komplexe Strukturen mit mehreren Zeiger Ebenen in einem zusammenhängenden Speicherpuffer. Wenn eine MAPI-Funktion oder-Methode einen Puffer mit solchen Inhalten erstellt, kann ein Client später alle im Puffer enthaltenen Strukturen freigeben, indem er an **mapifreebufferfreigegeben** den Zeiger auf den Puffer übergibt, der von der MAPI-Funktion zurückgegeben wurde, die den Puffer erstellt hat. Damit ein Dienstanbieter einen Speicherpuffer mithilfe von **mapifreebufferfreigegeben**freigeben kann, muss er den Zeiger an diesen Puffer übergeben, der mit dem Support Objekt des Anbieters zurückgegeben wird. 
  
Der Aufruf an **mapifreebufferfreigegeben** , einen bestimmten Puffer freizugeben, muss vorgenommen werden, sobald ein Client oder Anbieter diesen Puffer verwendet. Beim einfachen Aufrufen der [IMAPISession:: Logout](imapisession-logoff.md) -Methode am Ende einer MAPI-Sitzung werden Speicherpuffer nicht automatisch freigegeben. 
  
Ein Client oder Dienstanbieter sollte davon ausgehen, dass der in _lpBuffer_ übergebene Zeiger nach einer erfolgreichen Rückgabe von **mapifreebufferfreigegeben**ungültig ist. Wenn der Zeiger entweder einen vom Messagingsystem nicht zugewiesenen Speicherblock über **MAPIAllocateBuffer** oder **MAPIAllocateMore** oder einen freien Speicherblock angibt, ist das Verhalten von **mapifreebufferfreigegeben** nicht definiert. 
  
> [!NOTE]
> Durch das Übergeben eines NULL-Zeigers an **mapifreebufferfreigegeben** wird der Anwendungs Bereinigungscode einfacher und kleiner, da **MAPIFREEBUFFERFREIGEGEBEN** Zeiger auf Null initialisieren und dann im Bereinigungscode freigeben kann, ohne Sie zuerst testen zu müssen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

