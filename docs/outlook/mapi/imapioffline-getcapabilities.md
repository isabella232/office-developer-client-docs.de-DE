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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572032"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft die Bedingungen für die Rückrufe durch eine offline-Objekt unterstützt werden.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameter

 _pulCapablities_
  
> [out] Eine Bitmaske der folgenden Funktion Flags:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> Das offline-Objekt ist offline Benachrichtigungen bereitstellen können.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> Das offline-Objekt ist online Benachrichtigungen bereitstellen können.
    
## <a name="remarks"></a>HinwBemerkungeneise

Beim Öffnen einer offline-Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)**, kann ein Client eine Abfrage auf [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) an, um einen Zeiger auf eine **IMAPIOffline** -Schnittstelle, und rufen **IMAPIOffline::GetCapabilities** , um die Rückrufe unterstützt zu erhalten durch das Objekt. Der Client kann, wählen Sie dann mithilfe von **IMAPIOfflineMgr**Rückrufe eingerichtet.
  
Beachten Sie, dass je nach den Mailserver für eine offline-Objekt, ein Objekt, das Rückrufe für den Onlinemodus wechseln unterstützt keine unbedingt Rückrufe unterstützt für den Wechsel in den Offlinemodus.
  
Beachten Sie, dass auch während ein offline-Objekt kann Rückrufe für Änderungen als online/offline unterstützen, die Offline Zustand-API nur online/offline ändert sich unterstützt und Clients müssen für nur solche Funktionen überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

