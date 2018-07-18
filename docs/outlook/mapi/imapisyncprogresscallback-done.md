---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792431"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**Betrifft**: Outlook 
  
 Microsoft Outlook informiert, dass die Synchronisierung abgeschlossen ist. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Parameter

 **hThreadDoneEvent**
  
> Ein Ereignis, das zurück, um Microsoft Outlook können Sie das Handle Schließen zulassen übergeben wird. Es kann NULL sein.
    
 **hResult**
  
> Ein HRESULT Endstatus des Fortschritts angibt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

