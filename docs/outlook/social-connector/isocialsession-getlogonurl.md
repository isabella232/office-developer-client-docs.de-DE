---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Ruft eine Zeichenfolge, die eine URL darstellt, die für die Darstellung eines Formulars browserbasierte für dem Benutzer während der Webauthentifizierung verwendet wird.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795982"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Ruft eine Zeichenfolge, die eine URL darstellt, die für die Darstellung eines Formulars browserbasierte für dem Benutzer während der Webauthentifizierung verwendet wird.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parameter

_url_
  
> [out] Eine Zeichenfolge, die eine URL für das Formular in der Webauthentifizierung enthält.
    
## <a name="remarks"></a>Bemerkungen

Nachdem das Formular für den Benutzer angezeigt wird, wird die [ISocialSession::LogonWeb](isocialsession-logonweb.md) -Methode mit einer leeren Zeichenfolge für den Parameter _ConnectIn_ aufgerufen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

