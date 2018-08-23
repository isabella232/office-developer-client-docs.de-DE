---
title: Unterstützende Nachricht Dienstkonfiguration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f9ac5d9cef09ce6d4f3006ecc804db6291cae77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579340"
---
# <a name="supporting-message-service-configuration"></a>Unterstützende Nachricht Dienstkonfiguration
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zur Unterstützung der Nachricht Dienstkonfiguration verwenden Sie die folgende Schritte aus:
  
1. Implementieren Sie eine Eintrag Point-Funktion, die den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp entspricht. Nachricht Webdienstfunktionen Entry Point Verwalten des Zugriffs auf Konfigurationsdaten und werden in den folgenden Umständen aufgerufen: 
    
   - Abrufen von Informationen zum Konfigurieren Ihrer Messagingdiensts beim Anmelden eines Clients an.
    
   - Wenn ein Client möchte anzeigen oder Ändern einer Konfigurationseigenschaft. 
    
   Obwohl die meisten Message-Dienste wie gewünscht Entry Point-Funktionen, bereitgestellt werden, sind diese Funktionen nicht zwingend erforderlich. Message-Dienste können auf die Konfigurationsdaten auf andere Weise bereitstellen. Jedoch eine Entry Point-Funktion verwenden standardisiert und vereinfacht den Prozess der Konfiguration.
    
   MAPI erwartet, dass alle Nachricht Service Eintrag Point-Funktionen können zum Speichern und Abrufen von Eigenschaften aus der Profil-Abschnitte, die ihre Nachrichtendienst zugeordnet sind. Sie können diese Funktionalität unterstützen, interaktiv, programmgesteuert oder beide programmgesteuert und interaktiv.
    
   Geben Sie zur Unterstützung der interaktiven Konfiguration eines Eigenschaftenblatts, das die Eigenschaften zum Konfigurieren Ihrer Messagingdiensts anzeigt. Optional können Sie auch Eigenschaftenseiten für jeden konfigurierbar Anbieter angeben. Einige Nachrichtendienste beschränken Benutzer zu einer nur-Lese-Ansicht von Konfigurationseigenschaften. andere Nachrichtendienste können Benutzer Änderungen vornehmen.
    
   Zur Unterstützung der programmgesteuerte Konfiguration muss Ihre Nachricht Service Entry Point-Funktion ohne Benutzereingriff arbeiten können. Wenn Ihre Nachricht Service mit dem Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen. Wenn Ihre Messagingdiensts nicht selbst konfiguriert werden soll, mithilfe der Profil-Assistent zulassen, können Sie ob programmgesteuerten Konfiguration unterstützt.
    
   Weitere Informationen zur Unterstützung der Konfiguration in einer Nachricht Diensteintrag Funktion finden Sie [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Veröffentlichen Sie den Namen Ihrer Nachricht Service Entry Point-Funktion in der Konfigurationsdatei Mapisvc.inf durch den folgenden Eintrag im Abschnitt Dienst Nachricht einschließlich:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Erstellen Sie eine oder mehrere Eigenschaft Blatt Dialogfelder für die Anzeige von Daten zur Konfiguration.
    
4. Führen Sie die folgenden Aufgaben aus, wenn Sie zulassen, des Profil-Assistenten, um Ihre Messagingdiensts zu konfigurieren möchten:
    
   - Implementieren Sie eine Eintrag Point-Funktion, die den [WIZARDENTRY](wizardentry.md) Prototyp entspricht. 
    
   - Implementieren Sie ein Windows Dialogfeld Feld Standardverfahren, die den [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) Prototyp entspricht. 
    
   - Verbessern Sie Ihre Nachricht Service Eintrag Point-Funktion, um auf zusätzliche Ereignisse zu reagieren.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtendienstimplementierung](message-service-implementation.md)

