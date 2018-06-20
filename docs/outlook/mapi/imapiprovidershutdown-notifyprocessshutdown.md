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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792298"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Betrifft**: Outlook 
  
Zeigt den MAPI-Anbieter, dass ein MAPI-Client ausführt, ein Schnelles Herunterfahren, so dass der Anbieter Aktionen, um Datenverlust zu vermeiden nutzen kann.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Anbieter ist Aktionen um Datenverlust zu vermeiden, wenn der MAPI-Client beendet wird.
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

