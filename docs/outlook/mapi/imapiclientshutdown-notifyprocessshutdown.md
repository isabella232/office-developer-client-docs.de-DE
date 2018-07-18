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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 04a9b631c3a4f33282bce44e06d92e089349c76b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792061"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Betrifft**: Outlook 
  
Gibt an, fahren Sie der Zweck der MAPI-Client, fortsetzen.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Subsystems hat versucht, um geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client wird ein Schnelles Herunterfahren führen.
    
## <a name="remarks"></a>Bemerkungen

Verlust von Daten über das schnelle Herunterfahren von einem MAPI-Client zu vermeiden, sollten MAPI-Clients die basierend auf dem S_OK Ergebnis des MAPI-Subsystems in zurückgegebene **IMAPIClientShutdown::NotifyProcessShutdown** und [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) -Methoden aufrufen. die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode. Weitere Informationen finden Sie unter [Bewährte Methoden für Schnelles Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

