---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438869"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass der MAPI-Client mit dem Herunterfahren fortfahren soll.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem hat versucht, geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client ein schnelles Herunterfahren durchführen wird.
    
## <a name="remarks"></a>Bemerkungen

Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die **IMAPIClientShutdown:: NotifyProcessShutdown** und [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) -Methoden basierend auf dem vom MAPI-Subsystem zurückgegebenen Ergebnis S_OK in die [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode. Weitere Informationen finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

