---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9d5200a901cc692d4929edfba5a547a45ffe23c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551149"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordnet einen Speicherpuffer neu an. Sie wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) verwendet. 
  
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
  
> Ein Zeiger auf den Speicher, der neu zugewiesen werden soll.
    
 _ulSize_
  
> Die Größe des zuzuweisenden Puffers in Bytes.
    
 _lppv_
  
> Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.
    
## <a name="remarks"></a>HinwBemerkungeneise

 **MAPIReallocateBuffer** weist einen neuen Speicherblock der angeforderten Größe zu und kopiert den Inhalt des Puffers, der an diesen neuen Speicherblock übergeben wird. Wenn der übergebene Speicherblock interne Zeiger enthält, ändern sich die Zeiger nicht so, dass sie mit der neuen Position übereinstimmen. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)

