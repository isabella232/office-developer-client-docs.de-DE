---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Diese Methode ist in OSC 1,1 veraltet.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285455"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Diese Methode ist in OSC 1,1 veraltet.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Bemerkungen

Ab OSC 1,1 ruft der OSC getActivities nicht mehr **** auf. OSC ignoriert den Wert von **dynamicActivitiesLookup**. Zur Unterstützung der Suche nach dynamischen Aktivitäten implementieren Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen **Sie cacheActivities** als **false**, **** und GetActivities und **DYNAMICACTIVITIESLOOKUPEX** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

