---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Meldet sich mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks an.
ms.openlocfilehash: 03d37024f8c537d85134e9abc4ca6b0f6c097cf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608824"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Meldet sich mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks an.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parameter

_Nutzername_
  
> [in] Eine Zeichenfolge, die den Benutzernamen für die Anmeldung enthält.
    
_password_
  
> [in] Eine Zeichenfolge, die das anzumeldende Kennwort enthält.
    
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

