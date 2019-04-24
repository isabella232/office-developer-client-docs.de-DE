---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Ruft eine ISocialSession-Schnittstelle ab.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285772"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab. 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameter

_session_
  
> [out] Eine **ISocialSession**-Schnittstelle. 
    
## <a name="remarks"></a>Bemerkungen

Der Outlook Connector für soziale Netzwerke (OSC) verwendet die **ISocialSession** -Schnittstelle zum Anmelden am sozialen Netzwerk. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

