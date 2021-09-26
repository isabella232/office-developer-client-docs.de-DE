---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die von den Parametern "emailAddresses" und "displayName" als Freund des angemeldeten Benutzers im sozialen Netzwerk identifizierte Person hinzu.
ms.openlocfilehash: 6da454bb1c913951b492b8e6f4c63af9178134d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608818"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Fügt die von den  _Parametern "emailAddresses"_ und  _"displayName"_ als Freund des angemeldeten Benutzers im sozialen Netzwerk identifizierte Person hinzu. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameter

_emailAddresses_
  
> [in] Ein Array, das eine oder mehrere gültige SMTP-Adressen für eine Person im sozialen Netzwerk enthält.
    
_displayName_
  
> [in] Eine Zeichenfolge, die den Anzeigenamen der Person enthält, die als Freund hinzugefügt werden soll.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Outlook Connector für soziale Netzwerke (OSC) mehr als die SMTP-Adresse im Array im Parameter **emailAddresses** bereitstellt, kann der OSC-Anbieter davon ausgehen, dass das erste Element die primäre SMTP-Adresse ist. 
  
Wenn der Anbieter das **followPerson-Element** in der **Funktions-XML** auf **"true"** festgelegt hat und keines der Elemente für _emailAddresses_ mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND Fehler zurückgeben. Wenn der Anbieter **followPerson** in **den Funktionen** als **"false"** festgelegt hat, sollte der Anbieter den fehler OSC_E_FAIL zurückgeben. 
  
Wenn die **FollowPersonEx-Methode** erfolgreich ist, kann der Anbieter die Zeichenfolge im  _displayName-Parameter_ verwenden, um die Person in jeder nachfolgenden Friend-Bestätigungs-E-Mail zu adressieren, anstatt die Person anhand der SMTP-Adresse zu adressieren. Andererseits muss der Anbieter in der Lage sein, den OSC zu verarbeiten, der eine leere Zeichenfolge für den  _displayName-Parameter_ übergibt. 
  
Wenn der Anbieter die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementiert und **followPerson** in der Funktionen-XML auf **"true"** festgelegt hat, ruft osc **FollowPersonEx** anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)auf. Wenn der Anbieter **followPerson** als **"true"** festgelegt hat, die **ISocialSession2-Schnittstelle** jedoch nicht implementiert oder **FollowPersonEx** den OSC_E_NOTIMPL Fehler zurückgibt, ruft osc **ISocialSession::FollowPerson** auf.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

