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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408684"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem hat für geladene MAPI-Anbieter angegeben, dass der MAPI-Client sofort beendet wird, und die MAPI-Anbieter sind für den Clientabgang bereit.
    
MAPI_E_NO_SUPPORT
  
> Das MAPI-Subsystem unterstützt kein schnelles Herunterfahren des Clients.
    
## <a name="remarks"></a>Hinweise

Um Datenverluste durch das schnelle Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die [Methoden IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::D oFastShutdown** basierend auf dem S_OK-Ergebnis aufrufen, das vom MAPI-Subsystem in der [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) zurückgegeben wird. Weitere Informationen finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

