---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418148"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fragt das MAPI-Subsystem nach Unterstützung für schnelles Herunterfahren ab, die von geladenen MAPI-Anbietern bereitgestellt wird.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem unterstützt den MAPI-Client zum schnellen Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht, um schnelles Herunterfahren zu tun.
    
## <a name="remarks"></a>Hinweise

Ob das MAPI-Subsystem den MAPI-Client zum schnellen Herunterfahren unterstützt, hängt von der Windows-Registrierungseinstellung des Benutzers oder vom Standardverhalten des MAPI-Clients für schnelles Herunterfahren ab. Es hängt auch davon ab, ob die geladenen MAPI-Anbieter schnelles Herunterfahren unterstützen können. Weitere Informationen finden Sie unter [Fast Shutdown User Options](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

