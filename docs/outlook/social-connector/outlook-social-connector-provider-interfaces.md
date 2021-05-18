---
title: Outlook Schnittstellen für Anbieter für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam genutzt wird und verbindungen mit sozialen und geschäftlichen Netzwerken herstellt, sodass Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422810"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Schnittstellen für Anbieter für soziale Netzwerke

Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam genutzt wird und verbindungen mit sozialen und geschäftlichen Netzwerken herstellt, sodass Benutzer mit den Personen in ihren Netzwerken in Kontakt bleiben können, ohne Office. 
  
Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der das OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann. In der folgenden Tabelle sind die Schnittstellen in der Erweiterbarkeit des OSC-Anbieters aufgeführt. Ein OSC-Anbieter muss vier der fünf Schnittstellen implementieren, um mit dem OSC zu kommunizieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md). Wenn der OSC-Anbieter die Synchronisierung von Aktivitäten, die On-Demand- oder Hybridsynchronisierung von Freunden, das Zwischenspeichern von Anmeldeinformationen und die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen oder die Möglichkeit unterstützt, einer Person zu folgen, sollte der Anbieter [auch ISocialSession2](isocialsession2iunknown.md)implementieren.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Stellt eine Person im sozialen Netzwerk dar.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Stellt den angemeldeten Benutzer dar.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Stellt eine Instanz eines OSC-Anbieters dar.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Unterstützt das Synchronisieren von Aktivitäten, das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.  <br/> |
   

