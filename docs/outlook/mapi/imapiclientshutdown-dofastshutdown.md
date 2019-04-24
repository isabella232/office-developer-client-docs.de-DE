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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350904"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass der MAPI-Client sofort den Clientprozess beenden soll.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem hat den geladenen MAPI-Anbietern angezeigt, dass der MAPI-Client sofort beendet wird, und die MAPI-Anbieter sind bereit für den Client-Exit.
    
MAPI_E_NO_SUPPORT
  
> Das MAPI-Subsystem unterstützt das schnelle Herunterfahren des Clients nicht.
    
## <a name="remarks"></a>Bemerkungen

Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::D ofastshutdown** -Methoden basierend auf dem vom MAPI-Subsystem zurückgegebenen Ergebnis S_OK in die [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode. Weitere Informationen finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

