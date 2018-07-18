---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Ruft eine Zeichenfolge, die einen eindeutigen für soziale Netzwerkbezeichner für eine bestimmte sozialen Netzwerkverbindung darstellt.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796109"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Ruft eine Zeichenfolge, die einen eindeutigen für soziale Netzwerkbezeichner für eine bestimmte sozialen Netzwerkverbindung darstellt. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parameter

_networkIdentifier_
  
> [out] Eine Zeichenfolge, die einen eindeutige für soziale Netzwerkbezeichner enthält.
    
## <a name="remarks"></a>Bemerkungen

Eine eindeutige ID ist eine Zeichenfolge, die Outlook Social Connector (OSC) Anbieter für soziale Netzwerke identifiziert. Diese Methode kann auch E_NOTIMPL zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

