---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 89846a334ef78aa5b8aba924afcbb625013cd65e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556581"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fragt den MAPI-Anbieter auf Unterstützung für schnelles Herunterfahren ab. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter unterstützt den MAPI-Client für schnelles Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht für schnelles Herunterfahren.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die [IMAPIProviderShutdown-Schnittstelle](imapiprovidershutdowniunknown.md) implementieren und die **IMAPIProviderShutdown::QueryFastShutdown-Methode** MAPI_E_NO_SUPPORT zurückgeben lassen. Für Outlook als MAPI-Client führt dies dazu, dass Outlook warten, bis alle externen Verweise freigegeben werden, bevor sie beendet werden. 
  
Abhängig von der Windows Registrierungseinstellung des Benutzers für schnelles Herunterfahren verhindert die Nichtimplierung der **IMAPIProviderShutdown-Schnittstelle** nicht notwendigerweise ein schnelles Herunterfahren des Clients. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

