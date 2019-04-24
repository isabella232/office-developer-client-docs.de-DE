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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350869"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fragt das MAPI-Subsystem zur Unterstützung des schnellen Herunterfahrens ab, das von geladenen MAPI-Anbietern bereitgestellt wird.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Rückgabewert

S_OK
  
> Das MAPI-Subsystem unterstützt den MAPI-Client für schnelles Herunterfahren.
    
MAPI_E_NO_SUPPORT
  
> Der MAPI-Anbieter unterstützt den MAPI-Client nicht für schnelles Herunterfahren.
    
## <a name="remarks"></a>Bemerkungen

Ob das MAPI-Subsystem den MAPI-Client für schnelles Herunterfahren unterstützt, hängt von der Windows-Registrierungseinstellung des Benutzers oder dem Standardverhalten des MAPI-Clients für schnelles Herunterfahren ab. Außerdem hängt es von der Fähigkeit der geladenen MAPI-Anbieter ab, das schnelle Herunterfahren zu unterstützen. Weitere Informationen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

