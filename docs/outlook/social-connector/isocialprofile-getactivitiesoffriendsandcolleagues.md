---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Diese Methode ist in Outlook Social Connector 2013 veraltet.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406892"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Diese Methode ist in Outlook Social Connector 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Bemerkungen

Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten. OSC ignoriert die **cacheActivities** -Einstellung im Capabilities-XML und ruft diese Methode nicht mehr auf. Zur Unterstützung der Suche nach dynamischen Aktivitäten implementieren Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen **** Sie GetActivities und **DynamicActivitiesLookupEx** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen. 
  
Weitere Informationen dazu, wie die OSC-Aktivitäten von Freunden abgerufen werden, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

