---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792380"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Betrifft**: Outlook 
  
Ruft die Adressen der MAPI-Speicher Reservierung und Freigabe Funktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parameter

 _lppAllocateBuffer_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer** -Funktion. **MAPIAllocateBuffer** belegt. 
    
 _lppAllocateMore_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore** -Funktion. **MAPIAllocateMore** weist zusätzlichen Arbeitsspeicher für Speicher, der ursprünglich mithilfe von **MAPIAllocateBuffer**zugewiesen wurde.
    
 _lppFreeBuffer_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIFreeBuffer** -Funktion. **MAPIFreeBuffer** gibt Speicherplatz frei. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Funktion Adressen wurden erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::GetMemAllocRoutines** -Methode wird für alle Unterstützungsobjekte implementiert. Dienstanbieter anrufen **GetMemAllocRoutines** , um die Adressen der drei Speicherverwaltungsfunktionen abrufen, die an ihre Initialisierungsfunktion ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)) übergeben werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

