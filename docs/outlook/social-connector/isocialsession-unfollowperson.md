---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die person, die durch den parameter userID als Freund im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418435"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Entfernt die person, die durch den  _parameter userID_ als Freund im sozialen Netzwerk identifiziert wird. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameter

_userID_
  
> [in] Eine Zeichenfolge, die eine Benutzer-ID des sozialen Netzwerks für eine Person enthält.
    
## <a name="remarks"></a>Hinweise

Der  _parameter userID_ muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk sein. 
  
Wenn der Outlook Social Connector (OSC)-Anbieter **doNotFollowPerson** in der XML für Funktionen als **true** festgelegt **hat,** muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben, wenn die übergebene Benutzer-ID keinem Benutzer im Netzwerk zutrifft. Wenn der Anbieter **doNotFollowPerson** **in** funktionen als **false** festgelegt hat, sollte der Anbieter den Fehler OSC_E_FAIL zurückgeben. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

