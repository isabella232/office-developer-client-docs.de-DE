---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Diese Methode ist in Outlook Connector für soziale Netzwerke 2013 veraltet.
ms.openlocfilehash: e3cd51e920baa0abb834f9100676e5234752adcc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583037"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Diese Methode ist in Outlook Connector für soziale Netzwerke 2013 veraltet.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>HinwBemerkungeneise

Ab Outlook Connector für soziale Netzwerke 2013 unterstützt OSC nur die Synchronisierung von Aktivitäten bei Bedarf und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten. Der OSC ignoriert die Einstellung **"cacheActivities"** in der Funktions-XML und ruft diese Methode nicht mehr auf. Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche dynamischer Aktivitäten zu unterstützen. Legen Sie **"getActivities"** und **"dynamicActivitiesLookupEx"** auf **"true"** fest, wodurch der OSC aufgefordert wird, stattdessen **ISocialSession2::GetActivitiesEx** aufzurufen. 
  
Weitere Informationen dazu, wie der OSC die Aktivitäten von Freunden abruft, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

