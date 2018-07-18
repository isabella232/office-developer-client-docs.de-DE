---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die Person, die durch die Parameter EmailAddresses und DisplayName als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796005"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Fügt die Person, die durch die Parameter _EmailAddresses_ und _DisplayName_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameter

_emailAddresses_
  
> [in] Ein Array mit einem oder mehreren gültige SMTP-Adressen für eine Person im sozialen Netzwerk.
    
_displayName_
  
> [in] Eine Zeichenfolge, die den Anzeigenamen der Person, die als Freund hinzugefügt werden soll.
    
## <a name="remarks"></a>Bemerkungen

Wenn Outlook Social Connector (OSC) bietet mehr als auf kann SMTP-Adresse des Arrays in den Parameter **EmailAddresses** die OSC-Anbieter wird vorausgesetzt, dass das erste Element die primäre SMTP-Adresse ist. 
  
Wenn der Anbieter das **FollowPerson** -Element als **true** , in der **Funktionen** XML festgelegt hat und keine Elemente für _EmailAddresses_ einen Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND Fehler zurück. Wenn der Anbieter **FollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben. 
  
Wenn die **FollowPersonEx** -Methode erfolgreich ist, können der Anbieter die Zeichenfolge in der Parameter _DisplayName_ die Person in alle nachfolgenden Friend-e-Mail, statt die SMTP-Adresse die Person adressieren behandeln. Andererseits, muss der Anbieter die OSC übergeben einer leeren Zeichenfolge für den Parameter _"DisplayName"_ behandeln können. 
  
Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **FollowPerson** als **true** in die XML-Funktionen eingerichtet hat, ruft der OSC **FollowPersonEx** anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md). Wenn der Anbieter **FollowPerson** als **true** festgelegt wurde, aber nicht die **ISocialSession2** -Schnittstelle implementiert oder **FollowPersonEx** wird der OSC_E_NOTIMPL Fehler zurückgegeben, ruft der OSC **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

