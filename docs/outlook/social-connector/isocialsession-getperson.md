---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem Parameter userID ab.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285330"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem Parameter _UserID_ ab. 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parameter

_userId_
  
> in Eine Zeichenfolge, die eine Benutzer-ID oder eine SMTP-Adresse einer Person enthält.
    
_result_
  
> Out Eine **ISocialPerson** -Schnittstelle. 
    
## <a name="remarks"></a>Bemerkungen

Der Parameter _UserID_ muss eine Benutzer-ID oder eine SMTP-Adresse sein. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

