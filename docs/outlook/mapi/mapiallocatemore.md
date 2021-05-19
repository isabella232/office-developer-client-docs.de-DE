---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435390"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist einen Speicherpuffer zu, der mit einem anderen Puffer verknüpft ist, der zuvor mit der [MAPIAllocateBuffer-Funktion zugewiesen](mapiallocatebuffer.md) wurde. 
  
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
  
> [in] Größe des zu zugeordneten neuen Puffers in Bytes. 
    
 _lpObject_
  
> [in] Zeiger auf einen vorhandenen MAPI-Puffer, der mit **MAPIAllocateBuffer zugewiesen wurde.**
    
 _lppBuffer_
  
> [out] Zeiger auf den zurückgegebenen, neu zugewiesenen Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf ist erfolgreich und hat einen Zeiger auf den angeforderten Arbeitsspeicher zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Während **der MAPIAllocateMore-Anrufverarbeitung** erhält die aufrufende Implementierung einen Speicherblock vom Betriebssystem. Der Speicherpuffer wird für eine byte-Adresse mit gleichmäßiger Nummer zugewiesen. Auf Plattformen, auf denen der lange ganzzahlige Zugriff effizienter ist, ordnet das Betriebssystem den Puffer einer Adresse zu, deren Größe in Bytes ein Vielfaches von vier ist. 
  
Die einzige Möglichkeit, einen mit **MAPIAllocateMore zugewiesenen** Puffer frei zu geben, ist das Übergeben des im _lpObject-Parameter_ angegebenen Pufferzeigers an die [MAPIFreeBuffer-Funktion.](mapifreebuffer.md) Die Verknüpfung zwischen den Speicherpuffern, die [mapIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** zugeordnet sind, ermöglicht **MAPIFreeBuffer,** beide Puffer mit einem einzigen Aufruf frei zu lassen. 
  

