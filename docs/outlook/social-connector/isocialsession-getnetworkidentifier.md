---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für ein soziales Netzwerk für eine bestimmte Verbindung mit einem sozialen Netzwerk darstellt.
ms.openlocfilehash: deaaf3e3380602738e9427d403db658c0f1f62df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560326"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für ein soziales Netzwerk für eine bestimmte Verbindung mit einem sozialen Netzwerk darstellt. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parameter

_networkIdentifier_
  
> [out] Eine Zeichenfolge, die einen eindeutigen Bezeichner für soziale Netzwerke enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein eindeutiger Netzwerkbezeichner ist eine Zeichenfolge, die das soziale Netzwerk des Outlook Osc-Anbieters identifiziert. Diese Methode kann auch E_NOTIMPL zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

