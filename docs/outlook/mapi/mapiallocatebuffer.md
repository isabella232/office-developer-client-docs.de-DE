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
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425694"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist einen Speicherpuffer zu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> in Die Größe des Puffers in Byte, der reserviert werden soll. 
    
 _lppBuffer_
  
> Out Zeiger auf den zurückgegebenen reservierten Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der angeforderte Speicherpuffer wurde zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Während der **MAPIAllocateBuffer** -Anrufverarbeitung erwirbt die aufrufende Implementierung einen Speicherblock vom Betriebssystem. Der Arbeitsspeicherpuffer wird für eine gerade nummerierte Byte-Adresse zugewiesen. Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Byte ein Vielfaches von vier ist. 
  
Das Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion gibt den von **MAPIAllocateBuffer**zugewiesenen Speicherpuffer frei, indem die [MAPIAllocateMore](mapiallocatemore.md) -Funktion und alle damit verknüpften Puffer aufgerufen werden, wenn der Arbeitsspeicher nicht mehr benötigt wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIReallocateBuffer](mapireallocatebuffer.md)

