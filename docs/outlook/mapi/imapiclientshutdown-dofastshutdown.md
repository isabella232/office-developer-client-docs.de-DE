---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 531653f794b38fec68fac206963df04b55af20d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580027"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem hat angegeben, dass MAPI-Anbieter geladen werden, dass der MAPI-Client sofort beendet wird und die MAPI-Anbieter bereit für das Beenden des Clients sind.
    
MAPI_E_NO_SUPPORT
  
> Das MAPI-Subsystem unterstützt das schnelle Herunterfahren des Clients nicht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die Methoden [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::D oFastShutdown** basierend auf dem S_OK Ergebnis aufrufen, das vom MAPI-Subsystem in der [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) zurückgegeben wird. Weitere Informationen finden Sie unter ["Bewährte Methoden für schnelles Herunterfahren".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

