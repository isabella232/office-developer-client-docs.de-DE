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
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584933"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Abfragen des MAPI-Subsystems für Schnelles Herunterfahren unterstützt, die von geladenen MAPI-Anbieter bereitgestellt wird.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>R�ckgabewert

S_OK
  
> MAPI-Subsystems unterstützt den MAPI-Client zum Herunterfahren schnelle.
    
MAPI_E_NO_SUPPORT
  
> MAPI-Anbieter unterstützt keine den MAPI-Client zum Herunterfahren schnelle.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ob die MAPI-Subsystems auf Herunterfahren schnelle führen Sie den MAPI-Client unterstützt, hängt von Einstellung in der Windows-Registrierung des Benutzers oder das Standardverhalten des MAPI-Client für Schnelles Herunterfahren. Außerdem hängt die Möglichkeit der geladenen MAPI-Anbieter zur Unterstützung von schnellen Herunterfahren. Weitere Informationen finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

