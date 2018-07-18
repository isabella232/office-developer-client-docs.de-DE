---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem UserID-Parameter.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795985"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem _UserID_ -Parameter. 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> [in] Eine Zeichenfolge, die eine Benutzer-ID oder SMTP-Adresse einer Person enthält.
    
_Ergebnis_
  
> [out] Eine **ISocialPerson** -Schnittstelle. 
    
## <a name="remarks"></a>Bemerkungen

Der _Benutzer-ID_ -Parameter muss eine Benutzer-ID oder SMTP-Adresse sein. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

