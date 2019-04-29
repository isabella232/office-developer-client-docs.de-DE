---
title: Outlook Social Connector-Anbieterschnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam mit sozialen und geschäftlichen Netzwerken verbunden ist, sodass Benutzer in Kontakt mit den Personen in ihren Netzwerken bleiben können, ohne Office zu verlassen.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422810"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Social Connector-Anbieterschnittstellen

Der Outlook Social Connector (OSC) ist ein Office-Feature, das von Office-Clientanwendungen gemeinsam mit sozialen und geschäftlichen Netzwerken verbunden ist, sodass Benutzer in Kontakt mit den Personen in ihren Netzwerken bleiben können, ohne Office zu verlassen. 
  
Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), die es dem OSC ermöglicht, auf soziale Netzwerkdaten auf eine Art und Weise zuzugreifen, die unabhängig von den APIs der einzelnen sozialen Netzwerke ist. In der folgenden Tabelle sind die Schnittstellen der OSC-Anbieter Erweiterbarkeit aufgeführt. Ein OSC-Anbieter muss vier der fünf Schnittstellen implementieren, die mit dem OSC kommunizieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md). Wenn der OSC-Anbieter die Synchronisierung von Aktivitäten, die on-Demand-oder Hybrid Synchronisierung von Freunden, das Zwischenspeichern von Anmeldeinformationen und die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen oder die Möglichkeit zur Verfolgung einer Person unterstützt, sollte der Anbieter ISocialSession2 implementieren. [ ](isocialsession2iunknown.md).
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Stellt eine Person im sozialen Netzwerk dar.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Stellt den angemeldeten Benutzer dar.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Stellt eine Instanz eines OSC-Anbieters dar.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Stellt eine Verbindung zu einem sozialen Netzwerkstandort dar.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Unterstützt das Synchronisieren von Aktivitäten, Hinzufügen von Freunden, on-Demand-oder Hybrid Synchronisierung von Freunden oder Anmelden am sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.  <br/> |
   

