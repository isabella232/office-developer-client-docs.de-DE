---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die Person, die durch den Benutzer-ID-Parameter als einen Freund im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795996"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Entfernt die Person, die durch den _Benutzer-ID_ -Parameter als einen Freund im sozialen Netzwerk identifiziert. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameter

_Benutzer-ID_
  
> [in] Eine Zeichenfolge, die eine Benutzer-ID für soziale Netzwerke für eine Person enthält.
    
## <a name="remarks"></a>Hinweise

_UserID_ -Parameter muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk. 
  
Wenn der Anbieter Outlook Social Connector (OSC) **DoNotFollowPerson** als **true** in den XML-Code für **Funktionen**eingerichtet hat, muss der Anbieter den OSC_E_NOT_FOUND Fehler im Fall zurück, dass der Benutzer, dem Übergeben von ID in ein Benutzer im Netzwerk nicht übereinstimmt. Wenn der Anbieter **DoNotFollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

