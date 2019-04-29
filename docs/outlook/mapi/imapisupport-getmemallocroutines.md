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
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415537"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Adressen der MAPI-Speicher Zuweisungs-und-Zuordnungsfunktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [mapifreebufferfreigegeben](mapifreebuffer.md)) ab.
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parameter

 _lppAllocateBuffer_
  
> Out Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer** -Funktion. **MAPIAllocateBuffer** weist Speicher zu. 
    
 _lppAllocateMore_
  
> Out Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore** -Funktion. **MAPIAllocateMore** weist zusätzlichen Arbeitsspeicher für den Arbeitsspeicher zu, der ursprünglich mithilfe von **MAPIAllocateBuffer**zugewiesen wurde.
    
 _lppFreeBuffer_
  
> Out Ein Zeiger auf einen Zeiger auf die **mapifreebufferfreigegeben** -Funktion. **Mapifreebufferfreigegeben** gibt Arbeitsspeicher frei. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Funktions Adressen wurden erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: GetMemAllocRoutines** -Methode wird für alle Support-Objekte implementiert. Dienstanbieter rufen **GetMemAllocRoutines** auf, um die Adressen der drei Speicher Zuordnungsfunktionen abzurufen, die an Ihre Initialisierungsfunktion übergeben werden ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

