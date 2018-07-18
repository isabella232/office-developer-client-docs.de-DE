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
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793120"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Betrifft**: Outlook 
  
Ordnet Speicherpuffers, die mit einer anderen zuvor mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) reservierten Puffer verknüpft ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameter

 _cbSize_
  
> [in] Größe in Bytes des neuen Puffers zugeordnet werden. 
    
 _lpObject_
  
> [in] Zeiger auf eine vorhandene MAPI-Puffer mit **MAPIAllocateBuffer**reserviert.
    
 _lppBuffer_
  
> [out] Zeiger auf das zurückgegebene Puffer neu zugewiesen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und hat einen Zeiger auf den angeforderten Speicher zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Rufen Sie während der **MAPIAllocateMore** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem. Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen. Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist. 
  
Die einzige Möglichkeit, einen Puffer mit **MAPIAllocateMore** reservierte Version ist, übergeben den Zeiger auf den Puffer im _LpObject_ -Parameter an die Funktion [MAPIFreeBuffer](mapifreebuffer.md) angegeben. Die Verknüpfung zwischen den Speicherpuffern mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** reserviert ermöglicht **MAPIFreeBuffer** , beide Puffer mit einem einzigen Aufruf freizugeben. 
  

