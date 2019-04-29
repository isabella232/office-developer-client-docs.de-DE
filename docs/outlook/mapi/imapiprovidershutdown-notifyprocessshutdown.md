---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405247"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen soll, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter führt Aktionen aus, um Datenverluste beim Herunterfahren des MAPI-Clients zu verhindern.
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

