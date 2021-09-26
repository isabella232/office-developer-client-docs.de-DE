---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5fc5914f6af792bb59d8063e87ceb29ca0ccf8ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620940"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen beibehalten wird, um Datenverluste zu verhindern.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der MAPI-Anbieter ist bereit, dass der MAPI-Client sofort beendet wird. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

