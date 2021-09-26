---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Ruft eine automatisch konfigurierte ISocialSession-Schnittstelle ab.
ms.openlocfilehash: 5ed880294c12fa381b80210eb7e3fc16473ea7a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583030"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameter

_session_
  
> [out] Eine **ISocialSession**-Schnittstelle. 
    
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene **ISocialSession**-Schnittstelle wird basierend auf einer anbieterspezifischen Methode automatisch am Netzwerk angemeldet. 
  
Der Anbieter sollte den Fehler OSC_E_NOT_IMPLEMENTED zurückgeben, wenn das soziale Netzwerk die automatische Konfiguration nicht unterstützt. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

