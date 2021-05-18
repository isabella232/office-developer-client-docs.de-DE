---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die person hinzu, die durch den parameter emailAddress als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423258"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Fügt die person hinzu, die durch den  _parameter emailAddress_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameter

_emailAddress_
  
> [in] Eine Zeichenfolge, die eine E-Mail-Adresse einer Person enthält.
    
## <a name="remarks"></a>Hinweise

Der  _parameter emailAddress_ muss eine gültige SMTP-Adresse sein. Wenn der Outlook Social Connector (OSC)-Anbieter die **followPerson-Methode** **in** funktionen als **true** festgelegt hat und das Argument _für emailAddress_ keinem Benutzer im Netzwerk zutrifft, muss der Anbieter den Fehler OSC_E_NOT_FOUND zurückgeben. Wenn der Anbieter **followPerson** in den Funktionen als **false** festgelegt **hat,** sollte der OSC_E_FAIL zurückgeben.
  
Wenn der Anbieter die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementiert und **followPerson** **in** funktionen als **true** festgelegt hat, wird [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) von der OSC anstelle von **ISocialSession::FollowPerson aufruft.** Wenn der Anbieter die **ISocialSession2-Schnittstelle** nicht implementiert oder **ISocialSession2::FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, wird **ISocialSession::FollowPerson** vom OSC aufruft, solange der Anbieter **followPerson** in funktionen als **true** festgelegt **hat.** Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
Bei der Entscheidung, ob **ISocalSession::FollowPerson** oder **ISocialSession2::FollowPersonEx** implementiert werden soll, sollten Sie überlegen, ob Ihr Anbieter die anderen Methoden in **ISocialSession2** benötigt und ob Sie den  _parameter djsplayName_ in **FollowPersonEx** verwenden können.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

