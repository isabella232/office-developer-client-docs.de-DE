---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die Person, die vom Parameter "Email" als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird, hinzu.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423258"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Fügt die Person, die vom Parameter " _Email_ " als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird, hinzu. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameter

_emailAddress_
  
> in Eine Zeichenfolge, die eine e-Mail-Adresse einer Person enthält.
    
## <a name="remarks"></a>Bemerkungen

Der Parameter " _Email_ Address" muss eine gültige SMTP-Adresse sein. Wenn der Outlook-Anbieter für soziale Netzwerke (OSC) die **followPerson** -Methode in den **Funktionen**als **true** festgelegt hat und das Argument für die e-mailemail nicht mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter die OSC_E_NOT_FOUND zurückgeben. __ Fehler. Wenn der Anbieter **followPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben.
  
Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **followPerson** als **true** in- **Funktionen**festgelegt hat, ruft der osc [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) anstelle von **ISocialSession:: followPerson **. Wenn der Anbieter die **ISocialSession2** -Schnittstelle nicht implementiert oder **ISocialSession2:: FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft osc **ISocialSession:: FollowPerson** auf, solange der Anbieter festgelegt **hat followPerson** als **true** in- **Funktionen**. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
Bei der Entscheidung, ob **ISocalSession:: FollowPerson** oder **ISocialSession2:: FollowPersonEx**implementiert werden soll, sollten Sie berücksichtigen, ob der Anbieter die anderen Methoden in **ISocialSession2**benötigt und ob Sie die _ djsplayName_ -Parameter in **FollowPersonEx**.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

