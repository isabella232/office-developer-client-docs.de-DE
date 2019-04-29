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
  
Fragt den MAPI-Anbieter ab, um das schnelle Herunterfahren zu unterstützen. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter unterstützt den MAPI-Client für schnelles Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht für schnelles Herunterfahren.
    
## <a name="remarks"></a>Bemerkungen

MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) -Schnittstelle implementieren und die **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** -Methode MAPI_E_NO_SUPPORT zurückgeben. Für Outlook als MAPI-Client bewirkt dies, dass Outlook auf alle externen Verweise wartet, bevor es beendet wird. 
  
Abhängig von der Windows-Registrierungseinstellung des Benutzers für das schnelle Herunterfahren verhindert die Implementierung der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt, dass ein Client schnell heruntergefahren wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

