---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Ruft eine Zeichenfolge ab, die eine URL darstellt, die für die Darstellung eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.
ms.openlocfilehash: eeb822c40541ffb46fb8ac3087aa7bef21601d04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590394"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Ruft eine Zeichenfolge ab, die eine URL darstellt, die für die Darstellung eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parameter

_url_
  
> [out] Eine Zeichenfolge, die eine URL für das formular enthält, das bei der Webauthentifizierung verwendet wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem das Formular dem Benutzer angezeigt wurde, wird die [ISocialSession::LogonWeb-Methode](isocialsession-logonweb.md) mit einer leeren Zeichenfolge für den  _connectIn-Parameter_ aufgerufen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

