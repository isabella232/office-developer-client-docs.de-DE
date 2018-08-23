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
ms.openlocfilehash: 4301fb504439cf0ebd70b5ece589c812cb74844e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585297"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Abfragen der MAPI-Anbieter für Schnelles Herunterfahren unterstützen. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der MAPI-Anbieter unterstützt den MAPI-Client zum Herunterfahren schnelle.
    
MAPI_E_NO_SUPPORT
  
> MAPI-Anbieter unterstützt keine den MAPI-Client zum Herunterfahren schnelle.
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-Anbieter, die keine schnelle Herunterfahren von Clients unterstützen müssen sollten weiterhin die [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) -Schnittstelle implementieren, und haben die **IMAPIProviderShutdown::QueryFastShutdown** -Methode MAPI_E_NO_SUPPORT zurückgeben. Für Outlook als MAPI-Client bewirkt, dass dieser Outlook warten, dass alle externen Verweise freigegeben werden muss, bevor sie beendet wird. 
  
Je nach Windows-Registrierung des Benutzers verhindert Einstellung für das schnelle Herunterfahren nicht implementieren der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt ein schnelle Herunterfahren von Clients. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

