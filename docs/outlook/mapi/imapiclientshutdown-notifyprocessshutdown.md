---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 88512a6e55bc550e717dae4fda0ca41fce09d221
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571822"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Absicht des MAPI-Clients an, mit dem Herunterfahren fortzufahren.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem hat versucht, geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client ein schnelles Herunterfahren durchführen wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die Methoden **IMAPIClientShutdown::NotifyProcessShutdown** und [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) basierend auf dem S_OK Ergebnis aufrufen, das vom MAPI-Subsystem in der [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) zurückgegeben wird. Weitere Informationen finden Sie unter ["Bewährte Methoden für schnelles Herunterfahren".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

