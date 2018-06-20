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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792324"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Betrifft**: Outlook 
  
Abfragen der MAPI-Anbieter für Schnelles Herunterfahren unterstützen. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der MAPI-Anbieter unterstützt den MAPI-Client zum Herunterfahren schnelle.
    
MAPI_E_NO_SUPPORT
  
> MAPI-Anbieter unterstützt keine den MAPI-Client zum Herunterfahren schnelle.
    
## <a name="remarks"></a>Hinweise

MAPI-Anbieter, die keine schnelle Herunterfahren von Clients unterstützen müssen sollten weiterhin die [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) -Schnittstelle implementieren, und haben die **IMAPIProviderShutdown::QueryFastShutdown** -Methode MAPI_E_NO_SUPPORT zurückgeben. Für Outlook als MAPI-Client bewirkt, dass dieser Outlook warten, dass alle externen Verweise freigegeben werden muss, bevor sie beendet wird. 
  
Je nach Windows-Registrierung des Benutzers verhindert Einstellung für das schnelle Herunterfahren nicht implementieren der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt ein schnelle Herunterfahren von Clients. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

