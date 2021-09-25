---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1184944d55438cdaf2dc574a7e37c3ff8c4aaf7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625357"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Informiert Microsoft Outlook, dass die Synchronisierung abgeschlossen ist. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Parameter

 **hThreadDoneEvent**
  
> Ein Ereignis, das zurück übergeben wird, damit Microsoft Outlook das Handle schließen kann. Er kann NULL sein.
    
 **Hresult**
  
> Ein HRESULT, der den endgültigen Status des Fortschritts angibt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

