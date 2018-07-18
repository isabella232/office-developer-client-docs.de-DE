---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die Person, die durch den Parameter EmailAddress als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795987"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Fügt die Person, die durch den Parameter _EmailAddress_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameter

_emailAddress_
  
> [in] Eine Zeichenfolge, die eine e-Mail-Adresse einer Person enthält.
    
## <a name="remarks"></a>Bemerkungen

Der Parameter _EmailAddress_ muss eine gültige SMTP-Adresse sein. Wenn der Anbieter Outlook Social Connector (OSC) die **FollowPerson** -Methode als **true** , in **Funktionen festgelegt hat**und das Argument für _EmailAddress_ keinen Benutzer im Netzwerk überein stimmt, muss der Anbieter die OSC_E_NOT_FOUND zurück. Fehler. Wenn der Anbieter **FollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben.
  
Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und hat **FollowPerson** in **Funktionen**als **true** festgelegt, wird die OSC [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von **ISocialSession::FollowPerson aufrufen. **. Wenn der Anbieter nicht die **ISocialSession2** -Schnittstelle implementiert oder **ISocialSession2::FollowPersonEx** wird der OSC_E_NOTIMPL Fehler zurückgegeben, wird die OSC **ISocialSession::FollowPerson** aufrufen, solange der Anbieter **festgelegt hat FollowPerson** als **true** **Funktionen**. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).
  
Bei der Entscheidung, ob **ISocalSession::FollowPerson** oder **ISocialSession2::FollowPersonEx**zu implementieren, Sie berücksichtigen sollten, ob der Anbieter die andere Methoden in **ISocialSession2**benötigt, und ob können Sie die _verwenden. DjsplayName_ -Parameter im **FollowPersonEx**.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

