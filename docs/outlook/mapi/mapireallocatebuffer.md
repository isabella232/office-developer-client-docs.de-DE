---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435285"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Speicherpuffer neu zu. Es wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |omapix.h  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parameter

 _lpv_
  
> Ein Zeiger auf den speicher, der neu zugewiesen werden soll.
    
 _ulSize_
  
> Die Größe des zu zugeordneten Puffers in Bytes.
    
 _lppv_
  
> Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="remarks"></a>Hinweise

 **MAPIReallocateBuffer** weist einen neuen Speicherblock der angeforderten Größe zu und kopiert den Inhalt des Puffers, der an diesen neuen Speicherblock übergeben wird. Wenn der übergebene Speicherblock interne Zeiger enthält, ändern sich die Zeiger nicht an den neuen Speicherort. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)

