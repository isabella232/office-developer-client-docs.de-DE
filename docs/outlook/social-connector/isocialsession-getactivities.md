---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Diese Methode ist in OSC 1.1 veraltet.
ms.openlocfilehash: 6cc6137091ec1c10cd2e92f904149597935b094a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608816"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Diese Methode ist in OSC 1.1 veraltet.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>HinwBemerkungeneise

Ab OSC 1.1 ruft osc **getActivities** nicht mehr auf. Der OSC ignoriert den Wert von **dynamicActivitiesLookup.** Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche dynamischer Aktivitäten zu unterstützen. Legen Sie **"cacheActivities"** als **"false"** und **"getActivities"** und **"dynamicActivitiesLookupEx"** auf **"true"** fest, wodurch der OSC aufgefordert wird, stattdessen **ISocialSession2::GetActivitiesEx** aufzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

