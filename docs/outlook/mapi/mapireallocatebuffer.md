---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793145"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Betrifft**: Outlook 
  
Ordnet Speicherpuffers neu. Es wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |omapix.h  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parameter

 _LPV_
  
> Ein Zeiger auf den Speicher neu reserviert werden.
    
 _ulSize_
  
> Die Größe des Puffers zuzuweisende in Bytes.
    
 _lppv_
  
> Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="remarks"></a>Hinweise

 **MAPIReallocateBuffer** ordnet einen neuen Block des Systemspeichers auf die angeforderte Größe und kopiert den Inhalt des Puffers übergeben wird, die in dieser neuen Block Arbeitsspeicher. Wenn der Block des Speichers, der übergeben wird interne Zeiger enthält, Ändern der Zeiger nicht entsprechend den neuen Speicherort. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)

