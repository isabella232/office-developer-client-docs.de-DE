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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418995"
---
# <a name="supporting-message-service-configuration"></a>Unterstützen der Nachrichtendienstkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie das folgende Verfahren, um die Konfiguration des Nachrichtendiensts zu unterstützen:
  
1. Implementieren Sie eine Einstiegspunktfunktion, die dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) entspricht. Nachrichtendienst-Einstiegspunktfunktionen verwalten den Zugriff auf Konfigurationsdaten und werden unter den folgenden Umständen aufgerufen: 
    
   - Wenn sich ein Client anmeldet, um Informationen zum Konfigurieren des Nachrichtendiensts abzurufen.
    
   - Wenn ein Client eine Konfigurationseigenschaft anzeigen oder ändern möchte. 
    
   Obwohl die meisten Nachrichtendienste Einstiegspunktfunktionen bereitstellen, sind diese Funktionen nicht unbedingt erforderlich. Nachrichtendienste können auf andere Weise Zugriff auf Konfigurationsdaten bieten. Durch die Verwendung einer Einstiegspunktfunktion wird jedoch der Konfigurationsprozess standardisiert und vereinfacht.
    
   MAPI erwartet, dass alle Nachrichtendienst-Einstiegspunktfunktionen Eigenschaften aus den Profilabschnitten speichern und abrufen können, die ihrem Nachrichtendienst zugeordnet sind. Sie können diese Funktionalität interaktiv, programmgesteuert oder sowohl interaktiv als auch programmgesteuert unterstützen.
    
   Um die interaktive Konfiguration zu unterstützen, stellen Sie ein Eigenschaftenblatt zur Verfügung, das die Eigenschaften anzeigt, die beim Konfigurieren des Nachrichtendiensts beteiligt sind. Optional können Sie auch Eigenschaftenblätter für jeden konfigurierbaren Anbieter liefern. Einige Nachrichtendienste beschränken Benutzer auf eine schreibgeschützte Ansicht von Konfigurationseigenschaften. Mit anderen Nachrichtendiensten können Benutzer Änderungen vornehmen.
    
   Um die programmgesteuerte Konfiguration zu unterstützen, muss ihre Nachrichtendienst-Einstiegspunktfunktion ohne Benutzereingriff funktionieren können. Wenn Ihr Nachrichtendienst vom Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen. Wenn ihr Nachrichtendienst sich nicht mithilfe des Profil-Assistenten konfigurieren lässt, können Sie auswählen, ob die programmgesteuerte Konfiguration unterstützt werden soll.
    
   Weitere Informationen zur Unterstützung der Konfiguration in einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter [MSGSERVICEENTRY](msgserviceentry.md).
    
2. Veröffentlichen Sie den Namen ihrer Nachrichtendienst-Einstiegspunktfunktion in der Konfigurationsdatei Mapisvc.inf, indem Sie den folgenden Eintrag im Abschnitt Nachrichtendienst hinzufügen:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Erstellen Sie ein oder mehrere Eigenschaftenblattdialogfelder zum Anzeigen von Konfigurationsdaten.
    
4. Führen Sie die folgenden Aufgaben aus, wenn Sie dem Profil-Assistenten die Konfiguration des Nachrichtendiensts ermöglichen möchten:
    
   - Implementieren Sie eine Einstiegspunktfunktion, die dem [WIZARDENTRY-Prototyp](wizardentry.md) entspricht. 
    
   - Implementieren Sie eine Windows- und Standarddialogfeldprozedur, die dem [SERVICEWIZARDDLGPROC-Prototyp](servicewizarddlgproc.md) entspricht. 
    
   - Erweitern Sie die Einstiegspunktfunktion des Nachrichtendiensts, um auf zusätzliche Ereignisse zu reagieren.
    
## <a name="see-also"></a>Siehe auch

- [Implementierung des Nachrichtendiensts](message-service-implementation.md)

