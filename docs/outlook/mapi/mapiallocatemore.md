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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357316"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Reserviert einen Arbeitsspeicherpuffer, der mit einem anderen Puffer verknüpft ist, der zuvor mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion reserviert wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> in Die Größe des neuen Puffers in Bytes, der reserviert werden soll. 
    
 _lpObject_
  
> in Zeiger auf einen vorhandenen MAPI-Puffer, der mit **MAPIAllocateBuffer**zugeordnet ist.
    
 _lppBuffer_
  
> Out Zeiger auf den zurückgegebenen, neu zugewiesenen Puffer.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat einen Zeiger auf den angeforderten Speicher zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Während der **MAPIAllocateMore** -Anrufverarbeitung erwirbt die aufrufende Implementierung einen Speicherblock vom Betriebssystem. Der Arbeitsspeicherpuffer wird für eine gerade nummerierte Byte-Adresse zugewiesen. Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Byte ein Vielfaches von vier ist. 
  
Die einzige Möglichkeit zum Freigeben eines mit **MAPIAllocateMore** zugeordneten Puffers besteht darin, den im _lpObject_ -Parameter angegebenen Pufferzeiger an die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion zu übergeben. Die Verknüpfung zwischen den Speicherpuffern, die mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** reserviert wurden, ermöglicht **mapifreebufferfreigegeben** das Freigeben beider Puffer mit einem einzelnen Aufruf. 
  

