---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Diese Methode ist in OSC 1.1 veraltet.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795984"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Diese Methode ist in OSC 1.1 veraltet.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Bemerkungen

In Version 1.1 OSC starten, ruft der OSC nicht mehr **GetActivities**. Die OSC wird den Wert der **DynamicActivitiesLookup**ignoriert. Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen Sie **CacheActivities** als **"false"**, und **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

