---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Ruft eine ISocialSession-Schnittstelle.
ms.openlocfilehash: 59e6f61e1954f64d875c6336b211dcb530100252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795991"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle. 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameter

_Sitzung_
  
> [out] Eine **ISocialSession** -Schnittstelle. 
    
## <a name="remarks"></a>Hinweise

Outlook Social Connector (OSC) verwendet die **ISocialSession** -Schnittstelle in sozialen Netzwerken anmelden. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

