---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Diese Methode ist in Outlook Social Connector 2013 veraltet.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286164"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Diese Methode ist in Outlook Social Connector 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Bemerkungen

Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten. OSC ignoriert die **cacheActivities** -Einstellung im Capabilities-XML und ruft diese Methode nicht auf. Zur Unterstützung der Suche nach dynamischen Aktivitäten implementieren Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen Sie **cacheActivities** als **false**, GetActivities und **dynamicActivitiesLookupEx** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen. **** 
  
Weitere Informationen dazu, wie die OSC-Aktivitäten von Freunden abgerufen werden, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

