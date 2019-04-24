---
title: Unterstützen der Nachrichtendienstkonfiguration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350610"
---
# <a name="supporting-message-service-configuration"></a>Unterstützen der Nachrichtendienstkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gehen Sie folgendermaßen vor, um die Nachrichtendienst Konfiguration zu unterstützen:
  
1. Implementieren Sie eine Einstiegspunktfunktion, die dem [MSGSERVICEENTRY](msgserviceentry.md) -Prototyp entspricht. Einstiegspunktfunktionen für den Nachrichtendienst verwalten den Zugriff auf Konfigurationsdaten und werden in den folgenden Situationen aufgerufen: 
    
   - Wenn ein Client sich anmeldet, um Informationen zum Konfigurieren des Nachrichtendiensts abzurufen.
    
   - Wenn ein Client eine Konfigurationseigenschaft anzeigen oder ändern möchte. 
    
   Obwohl die meisten Nachrichtendienste Einstiegspunktfunktionen bereitstellen, sind diese Funktionen nicht unbedingt erforderlich. Nachrichtendienste können auf andere Weise auf Konfigurationsdaten zugreifen. Die Verwendung einer Einstiegspunktfunktion standardisiert und vereinfacht jedoch den Konfigurationsprozess.
    
   MAPI erwartet, dass alle Einstiegspunktfunktionen des Nachrichtendiensts Eigenschaften aus den Profil Abschnitten speichern und abrufen können, die dem Nachrichtendienst zugeordnet sind. Sie können diese Funktionalität interaktiv, programmgesteuert oder interaktiv und programmgesteuert unterstützen.
    
   Zur Unterstützung der interaktiven Konfiguration geben Sie ein Eigenschaftenfenster an, in dem die an der Konfiguration des Nachrichtendiensts beteiligten Eigenschaften angezeigt werden. Optional können Sie auch Eigenschaftenblätter für jeden konfigurierbaren Anbieter bereitstellen. Einige Nachrichtendienste schränken Benutzer auf eine schreibgeschützte Ansicht der Konfigurationseigenschaften ein. andere Nachrichtendienste ermöglichen es Benutzern, Änderungen vorzunehmen.
    
   Zur Unterstützung der programmgesteuerten Konfiguration muss Ihre Nachrichtendienst-Einstiegspunktfunktion ohne Benutzereingriff arbeiten können. Wenn der Nachrichtendienst vom Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen. Wenn sich der Nachrichtendienst nicht mit dem Profil-Assistenten konfigurieren lässt, können Sie auswählen, ob die programmgesteuerte Konfiguration unterstützt werden soll.
    
   Weitere Informationen zur Unterstützung der Konfiguration in einer Einstiegspunktfunktion für den Nachrichtendienst finden Sie unter [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Veröffentlichen Sie den Namen der Einstiegspunktfunktion des Nachrichtendiensts in der Konfigurationsdatei MAPISVC. inf, indem Sie den folgenden Eintrag im Abschnitt Nachrichtendienst einschließen:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Erstellen Sie ein oder mehrere Eigenschaftenblatt-Dialogfelder zum Anzeigen von Konfigurationsdaten.
    
4. Führen Sie die folgenden Aufgaben aus, wenn Sie zulassen möchten, dass der Profil-Assistent Ihren Nachrichtendienst konfiguriert:
    
   - Implementieren Sie eine Einstiegspunktfunktion, die dem [WIZARDENTRY](wizardentry.md) -Prototyp entspricht. 
    
   - Implementieren Sie eine Windows-Standarddialogfeld-Prozedur, die dem [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) -Prototyp entspricht. 
    
   - Verbessern Sie die Einstiegspunktfunktion Ihres Nachrichtendiensts, um auf zusätzliche Ereignisse zu reagieren.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtendienst Implementierung](message-service-implementation.md)

