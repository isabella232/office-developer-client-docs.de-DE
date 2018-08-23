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
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583008"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie während der **MAPIAllocateMore** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem. Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen. Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist. 
  
Die einzige Möglichkeit, einen Puffer mit **MAPIAllocateMore** reservierte Version ist, übergeben den Zeiger auf den Puffer im _LpObject_ -Parameter an die Funktion [MAPIFreeBuffer](mapifreebuffer.md) angegeben. Die Verknüpfung zwischen den Speicherpuffern mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** reserviert ermöglicht **MAPIFreeBuffer** , beide Puffer mit einem einzigen Aufruf freizugeben. 
  

