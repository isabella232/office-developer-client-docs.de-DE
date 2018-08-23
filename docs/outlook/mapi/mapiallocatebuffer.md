---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579599"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ordnet einen Arbeitsspeicherpuffer. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> [in] Größe des Puffers zuzuweisende in Bytes. 
    
 _lppBuffer_
  
> [out] Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und angeforderten Pufferüberläufe zurückgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie während der **MAPIAllocateBuffer** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem. Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen. Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist. 
  
Die [MAPIFreeBuffer](mapifreebuffer.md) Funktion-Versionen aufrufen verknüpft der **MAPIAllocateBuffer**, durch Aufrufen der [MAPIAllocateMore](mapiallocatemore.md) -Funktion und alle Puffer reservierte Speicherpuffer, wenn der Speicher nicht mehr benötigt wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIReallocateBuffer](mapireallocatebuffer.md)

