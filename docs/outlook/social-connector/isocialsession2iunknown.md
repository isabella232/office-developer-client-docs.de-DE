---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Unterstützt das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408831"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Unterstützt das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialSession2-Schnittstelle verfügbar** sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Methode  <br/> |Fügt die person hinzu, die durch die  _Parameter emailAddresses_ und  _displayName_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der Benutzer darstellt, die durch den  _HashedAddresses-Parameter angegeben_ werden.  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Methode  <br/> |Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die benutzer enthält, die durch den  _parameter personsAddresses angegeben_ werden.  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Methode  <br/> |Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Outlook Social Connector (OSC)-Anbieter kann diese Schnittstelle implementieren, wenn der Anbieter die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen unterstützt. Wenn der OSC-Anbieter **ISocialSession2 implementiert** und folgende Personen im sozialen Netzwerk unterstützt, würde das OSC [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)aufrufen, und der Anbieter muss **auch ISocialSession2::FollowPersonEx** implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Schnittstellen für Anbieter für soziale Verbindungen](outlook-social-connector-provider-interfaces.md)

