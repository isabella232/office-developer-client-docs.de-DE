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
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796001"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Diese Methode ist in Outlook Social Connector 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Bemerkungen

Starten in Outlook Connector für soziale Netzwerke 2013, die OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und nicht zwischengespeichert oder Hybrid Synchronisierung von Aktivitäten. Die OSC ignoriert die Einstellung **CacheActivities** in die XML-Funktionen und diese Methode nicht mehr aufgerufen. Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen Sie **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird. 
  
Weitere Informationen dazu, wie die OSC Freunde Aktivitäten abruft finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

