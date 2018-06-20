---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten aller vom HashedAddresses-Parameter angegebenen Benutzer darstellt.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795998"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten aller vom _HashedAddresses_ -Parameter angegebenen Benutzer darstellt. 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameter

_hashedAddresses_
  
> [in] Eine Struktur, die gibt ein Array von Hash SMTP-Adressen für eine Gruppe von Benutzern.
    
_startTime_
  
> [in] Der Zeitpunkt, nach dem erstellten Aktivitäten zurückgegeben werden.
    
_Aktivitäten_
  
> [out] Eine XML-Zeichenfolge, die den Satz von Aktivitäten durch _HashedAddresses_ im sozialen Netzwerk seit _StartTime_angegebenen Benutzer darstellt.
    
## <a name="remarks"></a>Hinweise

Die OSC **GetActivitiesEx** aufgerufen, wenn der OSC-Anbieter bedarfsgesteuerten Synchronisierung von Aktivitäten unterstützt. Die OSC speichert die Informationen, die in _Aktivitäten_ im Speicher zurückgegeben. Weitere Informationen darüber, wie die OSC verwendet und diese Informationen im Speicher aktualisiert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).
  
Outlook Social Connector 2013 ab, der OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und ruft nur **GetActivitiesEx** um Aktivitäten zu erhalten. Legen Sie zur Unterstützung der Aktivitäten auf Abruf Lookup **CacheActivities** , wie **"false"**, und **GetActivities** und **DynamicActivitiesLookupEx** als **true**und die OSC **GetActivitiesEx**aufgerufen werden.
  
Die zurückgegebene XML-Zeichenfolge muss die Schemadefinition für **ActivityFeed**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen.
  
Die Zeichenfolge _HashedAddresses_ stellt einen Satz von Hash Adressen für jeden Benutzer im Bereich Personen angezeigt. Hash SMTP-Adressen werden mithilfe der vom **HashFunction** -Element in der Anbieter **Funktionen** XML angegebenen Hashfunktion verschlüsselt. Der Benutzer hat keinen Friend der angemeldete Benutzer von der [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt werden. 
  
Der Parameter _StartTime_ ist **ein Datumswert in koordinierter Weltzeit (UTC)** . Ortszeit Werte müssen in UTC **Datum** konvertiert werden soll. 
  
Aktivitäten, die die **GetActivitiesEx** -Methode gibt benötigen einen Erstellung Time-Wert, der _Werte von StartTime_ größer ist kleiner oder gleich **jetzt**. Wenn keine Änderungen zwischen **StartTime** und **jetzt**aufgetreten sind, muss der Anbieter einen OSC_E_NO_CHANGES Fehler zurück.
  
## <a name="see-also"></a>Siehe auch

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)

