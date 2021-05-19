---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418218"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fragt den MAPI-Anbieter nach Unterstützung für schnelles Herunterfahren ab. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter unterstützt den MAPI-Client zum schnellen Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht, um schnelles Herunterfahren zu tun.
    
## <a name="remarks"></a>Hinweise

MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die [IMAPIProviderShutdown-Schnittstelle](imapiprovidershutdowniunknown.md) implementieren und die **IMAPIProviderShutdown::QueryFastShutdown-Methode** MAPI_E_NO_SUPPORT. Für Outlook als MAPI-Client führt dies dazu, dass Outlook warten, bis alle externen Verweise freigegeben werden, bevor sie beendet werden. 
  
Abhängig von der Registrierungseinstellung Windows Benutzer für schnelles Herunterfahren verhindert das Nicht implementieren der **IMAPIProviderShutdown-Schnittstelle** nicht unbedingt das schnelle Herunterfahren eines Clients. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

