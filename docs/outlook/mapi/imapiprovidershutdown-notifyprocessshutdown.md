---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592052"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt den MAPI-Anbieter, dass ein MAPI-Client ausführt, ein Schnelles Herunterfahren, so dass der Anbieter Aktionen, um Datenverlust zu vermeiden nutzen kann.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Anbieter ist Aktionen um Datenverlust zu vermeiden, wenn der MAPI-Client beendet wird.
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

