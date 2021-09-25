---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Diese Methode ist in Outlook Connector für soziale Netzwerke 2013 veraltet.
ms.openlocfilehash: c225cd19c2e3d02ebddae70ccd98ad5d59f783ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563245"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Diese Methode ist in Outlook Connector für soziale Netzwerke 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>HinwBemerkungeneise

Ab Outlook Connector für soziale Netzwerke 2013 unterstützt OSC nur die Synchronisierung von Aktivitäten bei Bedarf und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten. Der OSC ignoriert die **Einstellung "cacheActivities"** in der Funktions-XML und ruft diese Methode nicht auf. Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche dynamischer Aktivitäten zu unterstützen. Legen Sie **"cacheActivities"** als **"false",** **"getActivities"** und **"dynamicActivitiesLookupEx"** auf **"true"** fest, wodurch der OSC aufgefordert wird, stattdessen **ISocialSession2::GetActivitiesEx** aufzurufen. 
  
Weitere Informationen dazu, wie der OSC die Aktivitäten von Freunden abruft, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Siehe auch

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

