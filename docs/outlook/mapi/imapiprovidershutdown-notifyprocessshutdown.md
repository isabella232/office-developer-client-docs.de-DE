---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 25ea48649d1a58fbc753024e048e15d068374e90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575863"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen wird, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter ergreift Maßnahmen, um Datenverluste zu verhindern, wenn der MAPI-Client heruntergefahren wird.
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

