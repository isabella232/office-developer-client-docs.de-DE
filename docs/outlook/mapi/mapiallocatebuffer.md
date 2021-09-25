---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c50f34f273f351bb0c2051247073cbc611013fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579481"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist einen Speicherpuffer zu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> [in] Größe des zuzuweisenden Puffers in Bytes. 
    
 _lppBuffer_
  
> [out] Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den angeforderten Speicherpuffer zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Während der **MAPIAllocateBuffer-Aufrufverarbeitung** ruft die aufrufende Implementierung einen Speicherblock vom Betriebssystem ab. Der Speicherpuffer wird einer gerade nummerierten Byteadresse zugeordnet. Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Bytes ein Vielfaches von vier ist. 
  
Durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) wird der von **MAPIAllocateBuffer** zugewiesene Speicherpuffer durch Aufrufen der [MAPIAllocateMore-Funktion](mapiallocatemore.md) und aller damit verknüpften Puffer frei, wenn der Arbeitsspeicher nicht mehr benötigt wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIReallocateBuffer](mapireallocatebuffer.md)

