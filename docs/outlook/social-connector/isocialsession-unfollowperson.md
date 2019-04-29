---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die Person, die durch den Parameter userID als Freund im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418435"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Entfernt die Person, die durch den Parameter _UserID_ als Freund im sozialen Netzwerk identifiziert wird. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameter

_userID_
  
> in Eine Zeichenfolge, die eine soziale Netzwerk-Benutzer-ID für eine Person enthält.
    
## <a name="remarks"></a>Bemerkungen

Der Parameter " _UserID_ " muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk sein. 
  
Wenn der Outlook Social Connector-Anbieter (OSC) **doNotFollowPerson** als **true** im XML for **Capabilities**festgelegt hat, muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben, falls die Benutzer-ID, die übergeben wird, keinem Benutzer im Netzwerk entspricht. Wenn der Anbieter **doNotFollowPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

