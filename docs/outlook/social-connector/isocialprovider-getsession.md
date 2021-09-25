---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Ruft eine ISocialSession-Schnittstelle ab.
ms.openlocfilehash: b26d02622ee4debe1136c3840d20e93648c69d25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629137"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab. 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameter

_session_
  
> [out] Eine **ISocialSession**-Schnittstelle. 
    
## <a name="remarks"></a>Bemerkungen

Der Outlook Connector für soziale Netzwerke (OSC) verwendet die **ISocialSession-Schnittstelle,** um sich beim sozialen Netzwerk anzumelden. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

