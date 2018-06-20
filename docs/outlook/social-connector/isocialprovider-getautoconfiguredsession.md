---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Ruft eine automatisch konfigurierte ISocialSession-Schnittstelle.
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795997"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md) -Schnittstelle. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameter

_Sitzung_
  
> [out] Eine **ISocialSession** -Schnittstelle. 
    
## <a name="remarks"></a>Hinweise

Die zurückgegebene **ISocialSession** -Schnittstelle wird automatisch mit dem Netzwerk, basierend auf einer Methode, die an den Anbieter spezifisch sind angemeldet. 
  
Der Anbieter sollte den OSC_E_NOT_IMPLEMENTED Fehler zurückgegeben, wenn das soziale Netzwerk die automatische Konfiguration nicht unterstützt. Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Siehe auch

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

