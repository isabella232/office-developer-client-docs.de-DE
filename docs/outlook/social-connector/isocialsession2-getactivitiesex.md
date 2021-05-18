---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den HashedAddresses-Parameter angegeben werden.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404337"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den  _HashedAddresses-Parameter angegeben_ werden. 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameter

_hashedAddresses_
  
> [in] Eine Struktur, die ein Array mit #A0 mit Hash für eine Gruppe von Benutzern angibt.
    
_startTime_
  
> [in] Die Zeit, nach der die erstellten Aktivitäten zurückgegeben werden.
    
_activities_
  
> [out] Eine XML-Zeichenfolge, die den Satz von Aktivitäten der Benutzer darstellt, die von _hashedAddresses_ im sozialen Netzwerk seit _startTime angegeben werden._
    
## <a name="remarks"></a>Hinweise

Das OSC ruft **GetActivitiesEx auf,** wenn der OSC-Anbieter die On-Demand-Synchronisierung von Aktivitäten unterstützt. Das OSC speichert die in Aktivitäten zurückgegebenen  _Informationen_ im Arbeitsspeicher. Weitere Informationen dazu, wie das OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
Ab Outlook Social Connector 2013 unterstützt das OSC nur die On-Demand-Synchronisierung von Aktivitäten und ruft **nur GetActivitiesEx** auf, um Aktivitäten zu erhalten. Legen Sie **cacheActivities** als **false** und **getActivities** und **dynamicActivitiesLookupEx** als **true** vor, um die Suche nach On-Demand-Aktivitäten zu unterstützen, und das OSC wird **GetActivitiesEx aufrufen.**
  
Die zurückgegebene XML-Zeichenfolge muss der Schemadefinition für **activityFeed** entsprechen, wie im Schema für die Erweiterbarkeit des OSC-Anbieters definiert.
  
Der  _HashedAddresses-Sring_ stellt eine Gruppe von Hashadressen für jeden Benutzer dar, der im Personenbereich angezeigt wird. Die #A0 mit Hash werden mithilfe der hashing-Funktion verschlüsselt, die durch das **hashFunction-Element** in der #A1 des **Anbieters angegeben** wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession::LoggedOnUserName-Eigenschaft dargestellt](isocialsession-loggedonusername.md) wird. 
  
Der  _parameter startTime_ ist ein **Date-Wert** in koordinierter Weltzeit (Coordinated Universal Time, UTC). Ortszeitwerte müssen in **UTC-Datumswerte konvertiert** werden. 
  
Aktivitäten, die die **GetActivitiesEx-Methode** zurückgibt, müssen einen Erstellungszeitwert haben, der größer als _startTime_ und kleiner als oder gleich **Now ist.** Wenn zwischen **startTime** und **Now** keine Änderungen vorgenommen wurden, muss der Anbieter einen Fehler OSC_E_NO_CHANGES zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

