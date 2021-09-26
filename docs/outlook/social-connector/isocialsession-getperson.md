---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem userID-Parameter ab.
ms.openlocfilehash: 7546232b4ea758331dfd2ff5f794a0d14cafd590
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608822"
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Der  _parameter userID_ muss eine Benutzer-ID oder SMTP-Adresse sein. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

