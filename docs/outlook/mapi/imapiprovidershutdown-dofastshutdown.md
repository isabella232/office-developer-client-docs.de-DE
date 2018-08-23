---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563471"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, an den MAPI-Anbieter, dass der MAPI-Client sofort beendet wird, damit der MAPI-Anbieter ändert sich, um Datenverlust zu vermeiden beibehalten wird.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Anbieter ist bereit für den MAPI-Client sofort zu beenden. 
    
## <a name="see-also"></a>Siehe auch



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

