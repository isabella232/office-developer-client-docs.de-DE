---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die Person, die von den Parametern "Email" und "displayName" identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339655"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Fügt die Person, die von den Parametern " _Email_ " und " _DisplayName_ " identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameter

_emailAddresses_
  
> in Ein Array, das eine oder mehrere gültige SMTP-Adressen für eine Person im sozialen Netzwerk enthält.
    
_displayName_
  
> in Eine Zeichenfolge, die den Anzeigenamen der Person enthält, die als Friend hinzugefügt werden soll.
    
## <a name="remarks"></a>Bemerkungen

Wenn der Outlook Connector für soziale Netzwerke (OSC) mehr als eine SMTP-Adresse im Array im **** Parameter Emails enthält, kann der osc-Anbieter davon ausgehen, dass das erste Element die primäre SMTP-Adresse ist. 
  
Wenn der Anbieter das **followPerson** -Element im **Capabilities** -XML als **true** festgelegt hat und keines der Elemente für _Email_ -Absender mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben. Wenn der Anbieter **followPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben. 
  
Wenn die **FollowPersonEx** -Methode erfolgreich ist, kann der Anbieter die Zeichenfolge im Parameter _DisplayName_ verwenden, um die Person in einer späteren Friend-Bestätigungs-e-Mail zu adressieren, statt die Person anhand der SMTP-Adresse zu adressieren. Andererseits muss der Anbieter in der Lage sein, den OSC zu behandeln, der eine leere Zeichenfolge für den _DisplayName_ -Parameter übergibt. 
  
Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **followPerson** als **true** im Capabilities-XML festgelegt hat, ruft osc **FollowPersonEx** anstelle von [ISocialSession: followPerson](isocialsession-followperson.md)auf. Wenn der Anbieter **followPerson** als **true** festgelegt, die **ISocialSession2** -Schnittstelle jedoch nicht implementiert oder **FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft osc **ISocialSession:: followPerson**auf.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

