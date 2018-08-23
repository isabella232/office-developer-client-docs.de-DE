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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577814"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetMemAllocRoutines** -Methode wird für alle Unterstützungsobjekte implementiert. Dienstanbieter anrufen **GetMemAllocRoutines** , um die Adressen der drei Speicherverwaltungsfunktionen abrufen, die an ihre Initialisierungsfunktion ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)) übergeben werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

