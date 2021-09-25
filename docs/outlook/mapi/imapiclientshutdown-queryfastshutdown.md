---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 487ef45b6ef611114d841f8f4c585a059d09265d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580013"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fragt das MAPI-Subsystem auf Unterstützung für schnelles Herunterfahren ab, die von geladenen MAPI-Anbietern bereitgestellt wird.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem unterstützt den MAPI-Client für schnelles Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht für schnelles Herunterfahren.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ob das MAPI-Subsystem das schnelle Herunterfahren des MAPI-Clients unterstützt, hängt von der Registrierungseinstellung Windows des Benutzers oder vom Standardverhalten des MAPI-Clients für schnelles Herunterfahren ab. Es hängt auch davon ab, ob die geladenen MAPI-Anbieter schnelles Herunterfahren unterstützen können. Weitere Informationen finden Sie unter ["Benutzeroptionen für schnelles Herunterfahren".](fast-shutdown-user-options.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

