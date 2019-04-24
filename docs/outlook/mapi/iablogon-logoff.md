---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339298"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert den ABMELDEPROZESS.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der ABMELDEPROZESS wurde erfolgreich initiiert.
    
## <a name="remarks"></a>Bemerkungen

Der ABMELDEPROZESS wird in der Regel gestartet, wenn ein Client die [IMAPISession:: Abmelde](imapisession-logoff.md) Methode aufruft, um eine Sitzung zu beenden. MAPI ruft dann die **IABLogon:: Abmelde** Methode jedes Adressbuch Anbieters auf, um den ABMELDEPROZESS zu starten. 
  
Die **IABLogon:: Logout** -Methode führt die folgenden Aktionen aus: 
  
- Gibt alle geöffneten Objekte wie alle unter Objekte oder das Status-Objekt frei.
    
- Gibt das Support Objekt des Anbieters frei.
    
Weitere Informationen zum ABMELDEPROZESS von Adressbuch Anbietern finden Sie unter [Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

