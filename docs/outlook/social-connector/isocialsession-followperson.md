---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die vom parameter emailAddress identifizierte Person als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.
ms.openlocfilehash: 6c0c4d31dd1627a13b15b0b779c2e798ab9fd64b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590408"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Fügt die vom parameter  _emailAddress identifizierte_ Person als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameter

_emailAddress_
  
> [in] Eine Zeichenfolge, die eine E-Mail-Adresse einer Person enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der  _parameter emailAddress_ muss eine gültige SMTP-Adresse sein. Wenn der anbieter für Outlook Connector für soziale Netzwerke (OSC) die **followPerson-Methode** in den **Funktionen** auf **"true"** festgelegt hat und das Argument für _"emailAddress"_ nicht mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND Fehler zurückgeben. Wenn der Anbieter **followPerson** in **den Funktionen** als **"false"** festgelegt hat, sollte der Anbieter den fehler OSC_E_FAIL zurückgeben.
  
Wenn der Anbieter die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementiert und **followPerson** in **den Funktionen** auf **"true"** festgelegt hat, ruft osc [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von **ISocialSession::FollowPerson** auf. Wenn der Anbieter die **ISocialSession2-Schnittstelle** nicht implementiert oder **ISocialSession2::FollowPersonEx** den OSC_E_NOTIMPL Fehler zurückgibt, ruft osc **ISocialSession::FollowPerson** auf, solange der Anbieter **followPerson** in **Funktionen** auf **"true"** festgelegt hat. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
Bei der Entscheidung, ob **ISocalSession::FollowPerson** oder **ISocialSession2::FollowPersonEx** implementiert werden soll, sollten Sie überlegen, ob Ihr Anbieter die anderen Methoden in **ISocialSession2** benötigt und ob Sie den  _parameter djsplayName_ in **FollowPersonEx** verwenden können.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

