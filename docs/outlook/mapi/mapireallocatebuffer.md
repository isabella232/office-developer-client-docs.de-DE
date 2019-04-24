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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270238"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ordnet einen Arbeitsspeicherpuffer neu zu. Sie wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |omapix. h  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> Ein Zeiger auf den Speicher, der neu zugeordnet werden soll.
    
 _ulSize_
  
> Die Größe des Puffers in Byte, der reserviert werden soll.
    
 _LPPV_
  
> Ein Zeiger auf den zurückgegebenen reservierten Puffer.
    
## <a name="remarks"></a>Bemerkungen

 **MAPIReallocateBuffer** weist einen neuen Speicherblock der angeforderten Größe zu und kopiert den Inhalt des Puffers, der an diesen neuen Speicherblock übergeben wird. Wenn der übergebene Speicherblock interne Zeiger enthält, werden die Zeiger nicht so geändert, dass Sie mit dem neuen Speicherort übereinstimmen. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)

