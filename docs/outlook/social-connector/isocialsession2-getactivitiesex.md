---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten der einzelnen durch den hashedAddresses-Parameter angegebenen Benutzer darstellt.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336449"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten der einzelnen durch den _hashedAddresses_ -Parameter angegebenen Benutzer darstellt. 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameter

_hashedAddresses_
  
> in Eine Struktur, die ein Array von Hash-SMTP-Adressen für eine Gruppe von Benutzern angibt.
    
_startTime_
  
> in Die Zeit, nach der die erstellten Aktivitäten zurückgegeben werden.
    
_Aktivitäten_
  
> Out Eine XML-Zeichenfolge, die den Satz von Aktivitäten der Benutzer darstellt, die von _hashedAddresses_ im sozialen Netzwerk seit _Startzeit_angegeben sind.
    
## <a name="remarks"></a>Bemerkungen

OSC ruft **GetActivitiesEx** auf, wenn der osc-Anbieter die bedarfsgesteuerte Synchronisierung von Aktivitäten unterstützt. OSC speichert die Informationen, die in _Aktivitäten_ im Arbeitsspeicher zurückgegeben werden. Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und ruft nur **GetActivitiesEx** zum Abrufen von Aktivitäten auf. Zur Unterstützung der Suche nach Anforderungs Aktivitäten legen Sie **cacheActivities** als **false**, und GetActivities und **dynamicActivitiesLookupEx** als **true**fest, und der osc ruft **GetActivitiesEx**auf. ****
  
Die zurückgegebene XML-Zeichenfolge muss der Schema Definition für **activityFeed**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert.
  
Der _hashedAddresses_ -Sring stellt einen Satz von Hash Adressen für jeden Benutzer dar, der im Personen Bereich angezeigt wird. Die Hash-SMTP-Adressen werden mithilfe der Hashfunktion verschlüsselt, die durch das **hashFunction** -Element in den XML- **Funktionen** des Anbieters angegeben wird. Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt wird. 
  
Der __ StartTime-Parameter ist ein **Datums** Wert in koordinierter Weltzeit (UTC). Lokale Zeitwerte müssen in UTC- **Datums** Werte konvertiert werden. 
  
Aktivitäten, die von der **GetActivitiesEx** -Methode zurückgegeben werden, müssen einen Wert für __ die Erstellungszeit haben, der größer als StartTime und kleiner als oder gleich **Now**ist. Wenn zwischen **Startzeit** und **Now**keine Änderungen aufgetreten sind, muss der Anbieter einen OSC_E_NO_CHANGES-Fehler zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)

