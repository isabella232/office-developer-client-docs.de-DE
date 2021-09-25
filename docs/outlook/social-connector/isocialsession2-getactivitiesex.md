---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den HashedAddresses-Parameter angegeben sind.
ms.openlocfilehash: 152c8750bd92dc1f7ee8bd363d4406ffe1017ac1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563168"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den  _HashedAddresses-Parameter_ angegeben sind. 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameter

_hashedAddresses_
  
> [in] Eine Struktur, die ein Array von SMTP-Hashadressen für eine Gruppe von Benutzern angibt.
    
_Starttime_
  
> [in] Die Zeit, nach der die erstellten Aktivitäten zurückgegeben werden.
    
_activities_
  
> [out] Eine XML-Zeichenfolge, die den Satz von Aktivitäten der Benutzer darstellt, die seit _startTime_ von _HashedAddresses_ im sozialen Netzwerk angegeben wurden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der OSC ruft **GetActivitiesEx** auf, wenn der OSC-Anbieter die On-Demand-Synchronisierung von Aktivitäten unterstützt. Der OSC speichert die zurückgegebenen Informationen in  _Aktivitäten_ im Arbeitsspeicher. Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)
  
Ab Outlook Connector für soziale Netzwerke 2013 unterstützt osc nur die Synchronisierung von Aktivitäten bei Bedarf und ruft nur **GetActivitiesEx** auf, um Aktivitäten abzurufen. Um die Suche nach Bedarfsaktivitäten zu unterstützen, legen Sie **"cacheActivities"** auf **"false"** und **"getActivities"** und **"dynamicActivitiesLookupEx"** auf **"true"** fest, und der OSC ruft **GetActivitiesEx** auf.
  
Die zurückgegebene XML-Zeichenfolge muss der Schemadefinition für **activityFeed** entsprechen, wie im Schema für die OSC-Anbietererweiterung definiert.
  
Der  _HashedAddresses-Sring_ stellt eine Reihe von Hashadressen für jeden Benutzer dar, der im Personenbereich angezeigt wird. Die SMTP-Hashadressen werden mithilfe der hashing-Funktion verschlüsselt, die durch das **hashFunction-Element** in der **XML-Funktionen** des Anbieters angegeben wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession::LoggedOnUserName-Eigenschaft](isocialsession-loggedonusername.md) dargestellt wird. 
  
Der  _startTime-Parameter_ ist ein **Date-Wert** in koordinierter Weltzeit (COORDINATED Universal Time, UTC). Ortszeitwerte müssen in **UTC-Datumswerte** konvertiert werden. 
  
Aktivitäten, die die **GetActivitiesEx** -Methode zurückgibt, müssen einen Erstellungszeitwert aufweisen, der größer als  _startTime_ und kleiner als oder gleich **Now** ist. Wenn zwischen **startTime** und **Now** keine Änderungen vorgenommen wurden, muss der Anbieter einen OSC_E_NO_CHANGES Fehler zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

