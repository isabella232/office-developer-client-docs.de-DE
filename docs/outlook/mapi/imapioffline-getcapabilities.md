---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 229900a1d00b8764266c45795462deb470762eb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564204"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Bedingungen ab, unter denen Rückrufe von einem Offlineobjekt unterstützt werden.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameter

 _pulCapablities_
  
> [out] Eine Bitmaske der folgenden Funktionsflags:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Das Offlineobjekt kann Offlinebenachrichtigungen bereitstellen.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Das Offlineobjekt kann Onlinebenachrichtigungen bereitstellen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Beim Öffnen eines Offlineobjekts mit **[HrOpenOfflineObj](hropenofflineobj.md)** kann ein Client [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) abfragen, um einen Zeiger auf eine **IMAPIOffline-Schnittstelle** abzurufen, und **IMAPIOffline::GetCapabilities** aufrufen, um die vom Objekt unterstützten Rückrufe herauszufinden. Der Client kann dann callbacks mithilfe von **IMAPIOfflineMgr** einrichten.
  
Beachten Sie, dass abhängig vom E-Mail-Server für ein Offlineobjekt ein Objekt, das Rückrufe für das Onlineschalten unterstützt, nicht notwendigerweise Rückrufe für das Offlineschalten unterstützt.
  
Beachten Sie außerdem, dass ein Offlineobjekt zwar Rückrufe für andere Änderungen als Online/Offline unterstützen kann, die Offlinestatus-API jedoch nur Online-/Offlineänderungen unterstützt und Clients nur nach solchen Funktionen suchen müssen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

