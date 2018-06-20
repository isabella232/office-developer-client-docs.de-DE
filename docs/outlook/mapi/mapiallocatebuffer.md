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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793107"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Hinweise

Rufen Sie während der **MAPIAllocateBuffer** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem. Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen. Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist. 
  
Die [MAPIFreeBuffer](mapifreebuffer.md) Funktion-Versionen aufrufen verknüpft der **MAPIAllocateBuffer**, durch Aufrufen der [MAPIAllocateMore](mapiallocatemore.md) -Funktion und alle Puffer reservierte Speicherpuffer, wenn der Speicher nicht mehr benötigt wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIReallocateBuffer](mapireallocatebuffer.md)

