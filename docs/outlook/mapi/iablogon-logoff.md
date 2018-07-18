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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791973"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Betrifft**: Outlook 
  
Initiiert den Prozess abmelden.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Prozess für die Abmeldung wurde erfolgreich initiiert.
    
## <a name="remarks"></a>Bemerkungen

Der Prozess für die Abmeldung wird in der Regel gestartet, wenn ein Client beenden eine Sitzung die [IMAPISession::Logoff](imapisession-logoff.md) Methode aufruft. MAPI ruft dann jede Adressbuchanbieter **IABLogon::Logoff** -Methode, um den Abmeldung zu starten. 
  
Die **IABLogon::Logoff** -Methode führt Folgendes aus: 
  
- Gibt alle geöffneten Objekte, wie alle Unterobjekte oder das Statusobjekt frei.
    
- Gibt den Anbieter DSO-Objekt frei.
    
Weitere Informationen zum Abmeldevorgang, von adressbuchanbietern implementierte finden Sie unter [Herunterfahren nach unten a Service Provider](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

