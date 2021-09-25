---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f51e657fb3ab2c05a28af24a91c38d990b5d132
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616936"
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
    
## <a name="remarks"></a>Bemerkungen

Der Abmeldevorgang wird in der Regel gestartet, wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um eine Sitzung zu beenden. MapI ruft dann die **IABLogon::Logoff-Methode** jedes Adressbuchanbieters auf, um den Abmeldevorgang zu starten. 
  
Die **IABLogon::Logoff-Methode** führt Folgendes aus: 
  
- Gibt alle geöffneten Objekte frei, z. B. alle Unterobjekte oder das Statusobjekt.
    
- Gibt das Supportobjekt des Anbieters frei.
    
Weitere Informationen zum Abmeldevorgang von Adressbuchanbietern finden Sie unter [Herunterfahren eines Dienstanbieters.](shutting-down-a-service-provider.md)
  
## <a name="see-also"></a>Siehe auch



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

