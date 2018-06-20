---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Meldet sich bei der Website für soziale Netzwerke mithilfe der angegebenen Benutzernamen und Kennwort.
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795990"
---
# <a name="isocialsessionlogon"></a>ISocialSession::Logon

Meldet sich bei der Website für soziale Netzwerke mithilfe der angegebenen Benutzernamen und Kennwort.
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a>Parameter

_Benutzername_
  
> [in] Eine Zeichenfolge, die den Benutzernamen zur Anmeldung bei enthält.
    
_password_
  
> [in] Eine Zeichenfolge, die das Kennwort zur Anmeldung bei enthält.
    
## <a name="see-also"></a>Siehe auch

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

