---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die person hinzu, die durch die Parameter emailAddresses und displayName als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429831"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Fügt die person hinzu, die durch die  _Parameter emailAddresses_ und  _displayName_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameter

_emailAddresses_
  
> [in] Ein Array, das eine oder mehrere gültige SMTP-Adressen für eine Person im sozialen Netzwerk enthält.
    
_displayName_
  
> [in] Eine Zeichenfolge, die den Anzeigenamen der Person enthält, die als Freund hinzugefügt werden soll.
    
## <a name="remarks"></a>Hinweise

Wenn der Outlook Social Connector (OSC) mehr als die SMTP-Adresse im Array im **parameter emailAddresses** enthält, kann der OSC-Anbieter davon ausgehen, dass das erste Element die primäre SMTP-Adresse ist. 
  
Wenn der Anbieter das **followPerson-Element**  im Funktionen-XML als **true** festgelegt hat und keines der Elemente für _emailAddresses_ einem Benutzer im Netzwerk zutrifft, muss der Anbieter den Fehler OSC_E_NOT_FOUND zurückgeben. Wenn der Anbieter **followPerson** in den Funktionen als **false** festgelegt **hat,** sollte der OSC_E_FAIL zurückgeben. 
  
Wenn die **FollowPersonEx-Methode** erfolgreich ist, kann der Anbieter die Zeichenfolge im  _displayName-Parameter_ verwenden, um die Person in jeder nachfolgenden E-Mail zur Freundesbestätigung anstatt die Person über die SMTP-Adresse zu adressieren. Andererseits muss der Anbieter in der Lage sein, das OSC zu verarbeiten, das eine leere Zeichenfolge für den _parameter displayName übergeben._ 
  
Wenn der Anbieter die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementiert und **followPerson** im Funktionen-XML als **true** festgelegt hat, ruft das OSC **FollowPersonEx** anstelle von [ISocialSession::FollowPerson auf.](isocialsession-followperson.md) Wenn der Anbieter **followPerson** als **true** festgelegt hat, aber die **ISocialSession2-Schnittstelle** nicht implementiert, oder **FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft das OSC **ISocialSession::FollowPerson auf.**
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

