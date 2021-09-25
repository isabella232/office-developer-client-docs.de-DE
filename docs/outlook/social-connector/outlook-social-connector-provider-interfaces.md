---
title: Outlook Anbieterschnittstellen für Connector für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Der Outlook Connector für soziale Netzwerke (OSC) ist ein Office Feature, das von Office Clientanwendungen gemeinsam genutzt wird, die eine Verbindung mit sozialen und geschäftlichen Netzwerken herstellen, damit Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office verlassen zu müssen.
ms.openlocfilehash: d45928fe371a69f5fa47a7b78cb2da7a9e49249b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566122"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Anbieterschnittstellen für Connector für soziale Netzwerke

Der Outlook Connector für soziale Netzwerke (OSC) ist ein Office Feature, das von Office Clientanwendungen gemeinsam genutzt wird, die eine Verbindung mit sozialen und geschäftlichen Netzwerken herstellen, damit Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office verlassen zu müssen. 
  
Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann. In der folgenden Tabelle sind die Schnittstellen in der OSC-Anbietererweiterung aufgeführt. Ein OSC-Anbieter muss vier der fünf Schnittstellen für die Kommunikation mit dem OSC implementieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md). Wenn der OSC-Anbieter die Synchronisierung von Aktivitäten, die bedarfsgesteuerte oder hybride Synchronisierung von Freunden, das Zwischenspeichern von Anmeldeinformationen und das Anmelden mit zwischengespeicherten Anmeldeinformationen oder die Möglichkeit, einer Person zu folgen, unterstützt, sollte der Anbieter [auch ISocialSession2](isocialsession2iunknown.md)implementieren.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Stellt eine Person im sozialen Netzwerk dar.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Stellt den angemeldeten Benutzer dar.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Stellt eine Instanz eines OSC-Anbieters dar.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Unterstützt die Synchronisierung von Aktivitäten, das Hinzufügen von Freunden, bei Bedarf oder die Hybridsynchronisierung von Freunden oder die Anmeldung am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.  <br/> |
   

