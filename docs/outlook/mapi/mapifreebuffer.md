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
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793144"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Betrifft**: Outlook 
  
Gibt einen mit einem Aufruf der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) oder die Funktion [MAPIAllocateMore](mapiallocatemore.md) reservierten Speicherpuffer frei. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parameter

 _lpBuffer_
  
> [in] Zeiger auf einen Puffer zuvor reservierter Speicher. Wenn NULL in der _LpBuffer_ -Parameter übergeben wird, hat **MAPIFreeBuffer** keine Auswirkung. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und den angeforderten Speicher freigegeben. **MAPIFreeBuffer** können auch S_OK zurückgeben, auf dem bereits freigegebenen Speicherorte oder wenn die Arbeitsspeicher-Block mit **MAPIAllocateBuffer** und **MAPIAllocateMore**kein Speicherplatz zugeordnet ist.
    
## <a name="remarks"></a>Hinweise

In der Regel, wenn eine Clientanwendung oder Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md), der Betriebssystem-Konstrukte in einen zusammenhängenden Speicherpuffers einen oder mehrere komplexe Strukturen mit mehreren Ebenen von Zeigern aufruft. Wenn ein MAPI-Funktion oder -Methode einen Puffer mit solchen Inhalte erstellt, kann ein Client später frei alle Strukturen, die im Puffer enthalten sind, indem Sie den Zeiger auf den Puffer zurückgegeben, die von der MAPI-Funktion, die den Puffer erstellt an **MAPIFreeBuffer** übergeben. Einem Dienstanbieter mit **MAPIFreeBuffer**Speicherpuffers frei muss er den Zeiger dem Puffer mit DSO-Objekt für den Anbieter zurückgegebenen bestehen. 
  
Der Aufruf **MAPIFreeBuffer** auf einen bestimmten Puffer frei so bald wie ein Client vorgenommen werden muss, oder Anbieter wird nach Abschluss des Vorgangs mit diesen Puffer. Einfach die [IMAPISession::Logoff](imapisession-logoff.md) -Methode aufruft, am Ende des MAPI-Sitzung wird nicht automatisch Speicherpuffern freigegeben. 
  
Ein Client oder Dienstanbieter sollte auf der Annahme ausgeführt werden, dass nach dem erfolgreichen Beenden **MAPIFreeBuffer** _LpBuffer_ übergebene Zeiger ungültig ist. Wenn der Zeiger entweder einen nicht von der messaging-System über **MAPIAllocateBuffer** oder **MAPIAllocateMore** oder einen Speicherblock freien reservierten Arbeitsspeicher Block gibt, ist das Verhalten der **MAPIFreeBuffer** nicht definiert. 
  
> [!NOTE]
> Übergeben einen null-Zeiger an **MAPIFreeBuffer** macht Anwendung Bereinigungscode einfacher und kleinere, da **MAPIFreeBuffer** können Zeiger auf NULL initialisiert, und klicken Sie dann in der Bereinigungscode frei, ohne sie zuerst zu testen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

