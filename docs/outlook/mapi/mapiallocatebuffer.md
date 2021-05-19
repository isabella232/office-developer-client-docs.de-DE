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
  
> [in] Größe des zu zugeordneten Puffers in Bytes. 
    
 _lppBuffer_
  
> [out] Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf ist erfolgreich und hat den angeforderten Speicherpuffer zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Während **der MAPIAllocateBuffer-Anrufverarbeitung** erhält die aufrufende Implementierung einen Speicherblock vom Betriebssystem. Der Speicherpuffer wird für eine byte-Adresse mit gleichmäßiger Nummer zugewiesen. Auf Plattformen, auf denen der lange ganzzahlige Zugriff effizienter ist, ordnet das Betriebssystem den Puffer einer Adresse zu, deren Größe in Bytes ein Vielfaches von vier ist. 
  
Durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) wird der von **MAPIAllocateBuffer zugewiesene** Speicherpuffer durch Aufrufen der [MAPIAllocateMore-Funktion](mapiallocatemore.md) und mit ihr verknüpfter Puffer frei, wenn der Arbeitsspeicher nicht mehr benötigt wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIReallocateBuffer](mapireallocatebuffer.md)

