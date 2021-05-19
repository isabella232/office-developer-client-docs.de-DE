---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433374"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Bedingungen ab, für die Rückrufe von einem Offlineobjekt unterstützt werden.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameter

 _pulCapablities_
  
> [out] Eine Bitmaske der folgenden Funktionskennzeichen:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Das Offlineobjekt kann Offlinebenachrichtigungen bereitstellen.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Das Offlineobjekt kann Onlinebenachrichtigungen bereitstellen.
    
## <a name="remarks"></a>Hinweise

Beim Öffnen eines Offlineobjekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** kann ein Client [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) abfragen, um einen Zeiger auf eine **IMAPIOffline-Schnittstelle** zu erhalten, und **IMAPIOffline::GetCapabilities** aufrufen, um die vom Objekt unterstützten Rückrufe zu finden. Der Client kann dann mithilfe von **IMAPIOfflineMgr** Rückrufe einrichten.
  
Beachten Sie, dass ein Objekt, das Rückrufe für den Onlinebetrieb unterstützt, abhängig vom E-Mail-Server für ein Offlineobjekt nicht unbedingt Rückrufe für den Offlinebetrieb unterstützt.
  
Beachten Sie außerdem, dass ein Offlineobjekt zwar Rückrufe für andere Änderungen als Online/Offline unterstützt, die Offlinestatus-API jedoch nur Online-/Offlineänderungen unterstützt, und Clients müssen nur auf diese Funktionen überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

