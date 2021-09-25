---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6fba63f5939eb6fb6e789fa2b083c9a7716c528c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592396"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Adressen der MAPI-Speicherzuweisung und der Zuordnungsfunktionen ab ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parameter

 _lppAllocateBuffer_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer-Funktion.** **MAPIAllocateBuffer** weist Arbeitsspeicher zu. 
    
 _lppAllocateMore_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore-Funktion.** **MAPIAllocateMore** weist zusätzlichen Speicher für Speicher zu, der ursprünglich mithilfe von **MAPIAllocateBuffer** zugewiesen wurde.
    
 _lppFreeBuffer_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIFreeBuffer-Funktion.** **MAPIFreeBuffer** gibt Arbeitsspeicher frei. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Funktionsadressen wurden erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetMemAllocRoutines-Methode** wird für alle Unterstützungsobjekte implementiert. Dienstanbieter rufen **GetMemAllocRoutines** auf, um die Adressen der drei Speicherzuweisungsfunktionen abzurufen, die an ihre Initialisierungsfunktion übergeben werden ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

