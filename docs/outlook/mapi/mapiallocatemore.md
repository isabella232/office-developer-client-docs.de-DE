---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83867eae14cf147e38ca9a72051bc6f4ba3be0bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610146"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist einen Speicherpuffer zu, der mit einem anderen Puffer verknüpft ist, der zuvor mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugeordnet wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> [in] Größe des zuzuweisenden neuen Puffers in Bytes. 
    
 _lpObject_
  
> [in] Zeiger auf einen vorhandenen MAPI-Puffer, der mit **MAPIAllocateBuffer** zugeordnet wurde.
    
 _lppBuffer_
  
> [out] Zeiger auf den zurückgegebenen, neu zugewiesenen Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat einen Zeiger auf den angeforderten Speicher zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Während der **MAPIAllocateMore-Anrufverarbeitung** ruft die aufrufende Implementierung einen Speicherblock vom Betriebssystem ab. Der Speicherpuffer wird einer gerade nummerierten Byteadresse zugeordnet. Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Bytes ein Vielfaches von vier ist. 
  
The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function. Die Verknüpfung zwischen den mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** zugeordneten Speicherpuffern ermöglicht **MAPIFreeBuffer** die Freigabe beider Puffer mit einem einzigen Aufruf. 
  

