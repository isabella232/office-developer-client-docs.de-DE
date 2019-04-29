---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Unterstützt das Hinzufügen von Freunden, der on-Demand-oder Hybrid Synchronisierung von Freunden, der bedarfsgesteuerten Synchronisierung von Aktivitäten oder der Anmeldung am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408831"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Unterstützt das Hinzufügen von Freunden, der on-Demand-oder Hybrid Synchronisierung von Freunden, der bedarfsgesteuerten Synchronisierung von Aktivitäten oder der Anmeldung am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.
  
## <a name="members"></a>Members

In der folgenden Tabelle sind die Member aufgeführt, die auf der **ISocialSession2** -Schnittstelle verfügbar sind. 
  
|**Name**|**Mitgliedstyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Methode  <br/> |Fügt die Person, die von den Parametern " _Email_ " und " _DisplayName_ " identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der durch den _hashedAddresses_ -Parameter angegebenen Benutzer darstellt.  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Methode  <br/> |Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den _personsAddresses_ -Parameter angegebenen Benutzer enthält.  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Methode  <br/> |Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen am Netzwerkstandort für soziale Netzwerke an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Outlook Social Connector-Anbieter (OSC) kann diese Schnittstelle implementieren, wenn der Anbieter die on-Demand-oder Hybrid Synchronisierung von Freunden, die bedarfsgesteuerte Synchronisierung von Aktivitäten oder die Anmeldung am sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen unterstützt. Wenn der OSC-Anbieter **ISocialSession2** implementiert und folgende Personen im sozialen Netzwerk unterstützt, würde osc [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession: FollowPerson](isocialsession-followperson.md)aufrufen, und der Anbieter muss **ISocialSession2:: FollowPersonEx**.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Social Connector-Anbieterschnittstellen](outlook-social-connector-provider-interfaces.md)

