---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792067"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Betrifft**: Outlook 
  
Gibt an, dass der MAPI-Client der Client sofort zu beenden.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Subsystems hat geladen MAPI-Anbieter angegeben, dass der MAPI-Client wird sofort beendet, und die MAPI-Anbieter bereit für den Client beenden sind.
    
MAPI_E_NO_SUPPORT
  
> MAPI-Subsystems bietet keine Unterstützung für schnelle Herunterfahren von Clients.
    
## <a name="remarks"></a>Bemerkungen

Verlust von Daten über das schnelle Herunterfahren von einem MAPI-Client zu vermeiden, sollten MAPI-Clients die basierend auf dem S_OK Ergebnis des MAPI-Subsystems in zurückgegebene [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::DoFastShutdown** -Methoden aufrufen. die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode. Weitere Informationen finden Sie unter [Bewährte Methoden für Schnelles Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

