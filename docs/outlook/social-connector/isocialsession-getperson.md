---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem userID-Parameter ab.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439821"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Ruft eine [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) basierend auf dem  _userID-Parameter_ ab. 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> [in] Eine Zeichenfolge, die eine Benutzer-ID oder SMTP-Adresse einer Person enthält.
    
_result_
  
> [out] Eine **ISocialPerson-Schnittstelle.** 
    
## <a name="remarks"></a>Hinweise

Der  _parameter userID_ muss eine Benutzer-ID oder EINE SMTP-Adresse sein. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

