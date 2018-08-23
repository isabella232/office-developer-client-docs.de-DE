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
ms.openlocfilehash: e85e2da4d63442dc1fb912c5941be9d6f6f53824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593788"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

 **MAPIReallocateBuffer** ordnet einen neuen Block des Systemspeichers auf die angeforderte Größe und kopiert den Inhalt des Puffers übergeben wird, die in dieser neuen Block Arbeitsspeicher. Wenn der Block des Speichers, der übergeben wird interne Zeiger enthält, Ändern der Zeiger nicht entsprechend den neuen Speicherort. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)

