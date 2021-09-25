---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Unterstützt das Hinzufügen von Freunden, die On-Demand- oder hybride Synchronisierung von Freunden, die Synchronisierung von Aktivitäten bei Bedarf oder das Anmelden am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.
ms.openlocfilehash: 4c6b34b01092c215cca5c18d332c3ec6e28647fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574503"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Unterstützt das Hinzufügen von Freunden, die On-Demand- oder hybride Synchronisierung von Freunden, die Synchronisierung von Aktivitäten bei Bedarf oder das Anmelden am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.
  
## <a name="members"></a>Members

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialSession2-Schnittstelle** verfügbar sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Methode  <br/> |Fügt die von den  _Parametern "emailAddresses"_ und  _"displayName"_ als Freund des angemeldeten Benutzers im sozialen Netzwerk identifizierte Person hinzu.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der Benutzer darstellt, die durch den  _HashedAddresses-Parameter_ angegeben sind.  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Methode  <br/> |Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die vom Parameter  _"personsAddresses" angegebenen_ Benutzer enthält.  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Methode  <br/> |Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein anbieter für Outlook Connector für soziale Netzwerke (OSC) kann diese Schnittstelle implementieren, wenn der Anbieter die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung am sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen unterstützt. Wenn der OSC-Anbieter **ISocialSession2** implementiert und folgende Personen im sozialen Netzwerk unterstützt, würde der OSC [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)aufrufen, und der Anbieter muss auch **ISocialSession2::FollowPersonEx** implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Anbieterschnittstellen für Connector für soziale Netzwerke](outlook-social-connector-provider-interfaces.md)

