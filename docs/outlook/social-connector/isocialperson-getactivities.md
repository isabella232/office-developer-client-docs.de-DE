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
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795963"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Diese Methode ist in Outlook Social Connector 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Bemerkungen

Starten in Outlook Connector für soziale Netzwerke 2013, die OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und nicht zwischengespeichert oder Hybrid Synchronisierung von Aktivitäten. Die OSC ignoriert die Einstellung **CacheActivities** in die XML-Funktionen und ruft diese Methode nicht auf. Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode. Legen Sie **CacheActivities** als **false**, **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird. 
  
Weitere Informationen dazu, wie die OSC Freunde Aktivitäten abruft finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

