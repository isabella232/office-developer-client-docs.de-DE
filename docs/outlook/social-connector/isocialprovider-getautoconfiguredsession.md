---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Ruft eine automatisch konfigurierte ISocialSession-Schnittstelle ab.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285779"
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

