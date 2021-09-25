---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die Person, die vom Parameter userID als Freund im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: bea5af2abe2d8046f4ff0788e46d9fb57ce5d5ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594909"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Entfernt die Person, die vom  _Parameter userID_ als Freund im sozialen Netzwerk identifiziert wird. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameter

_Userid_
  
> [in] Eine Zeichenfolge, die eine Benutzer-ID für ein soziales Netzwerk für eine Person enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der  _parameter userID_ muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk sein. 
  
Wenn der anbieter Outlook Connector für soziale Netzwerke (OSC) **doNotFollowPerson** im XML für **Funktionen** auf **"true"** festgelegt hat, muss der Anbieter den OSC_E_NOT_FOUND Fehler zurückgeben, falls die übergebene Benutzer-ID nicht mit einem Benutzer im Netzwerk übereinstimmt. Wenn der Anbieter **doNotFollowPerson** in **den Funktionen** als **"false"** festgelegt hat, sollte der Anbieter den OSC_E_FAIL Fehler zurückgeben. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

