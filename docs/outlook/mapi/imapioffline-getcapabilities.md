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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321315"
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
  
> Out Eine Bitmaske der folgenden Capability Flags:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Das Offline-Objekt kann offline Benachrichtigungen bereitstellen.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Das Offline-Objekt kann online Benachrichtigungen bereitstellen.
    
## <a name="remarks"></a>Bemerkungen

Beim Öffnen eines Offline Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** kann ein Client [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) Abfragen, um einen Zeiger auf eine **IMAPIOffline** -Schnittstelle abzurufen, und **IMAPIOffline::** getcapabilitiess aufrufen, um die unterstützten Rückrufe herauszufinden. durch das Objekt. Der Client kann dann Rückrufe mithilfe von **IMAPIOfflineMgr**einrichten.
  
Beachten Sie, dass abhängig vom e-Mail-Server für ein Offlineobjekt ein Objekt, das Rückrufe für das Online schalten unterstützt, nicht notwendigerweise Rückrufe für das offline schalten unterstützen wird.
  
Beachten Sie, dass ein Offlineobjekt Rückrufe für andere Änderungen als Online/Offline möglicherweise unterstützt, die Offlinestatus-API jedoch nur Online/Offline-Änderungen und Clients nur für solche Funktionen überprüfen muss.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

