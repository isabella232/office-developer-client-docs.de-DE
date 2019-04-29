---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Ruft eine Zeichenfolge, die eine eindeutige soziale Netzwerk-ID für eine bestimmte soziale Netzwerkverbindung darstellt.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433276"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Ruft eine Zeichenfolge, die eine eindeutige soziale Netzwerk-ID für eine bestimmte soziale Netzwerkverbindung darstellt. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parameter

_networkIdentifier_
  
> Out Eine Zeichenfolge, die eine eindeutige soziale Netzwerk-ID enthält.
    
## <a name="remarks"></a>Bemerkungen

Eine eindeutige Netzwerk-ID ist eine Zeichenfolge, die das soziale Netzwerk des Outlook Social Connector (OSC)-Anbieters identifiziert. Diese Methode kann auch E_NOTIMPL zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

