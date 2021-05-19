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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416398"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initiiert den Abmeldevorgang.
  
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
  
> Der Abmeldevorgang wurde erfolgreich initiiert.
    
## <a name="remarks"></a>Hinweise

Der Abmeldevorgang wird in der Regel gestartet, wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um eine Sitzung zu beenden. MAPI ruft dann die **IABLogon::Logoff-Methode** jedes Adressbuchanbieters auf, um den Abmeldevorgang zu starten. 
  
Die **IABLogon::Logoff-Methode** führt die folgenden Schritte aus: 
  
- Gibt alle geöffneten Objekte frei, z. B. alle Unterobjekte oder das Statusobjekt.
    
- Gibt das Supportobjekt des Anbieters frei.
    
Weitere Informationen zum Abmeldevorgang von Adressbuchanbietern finden Sie unter [Shutting Down a Service Provider](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

