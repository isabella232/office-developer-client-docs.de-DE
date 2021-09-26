---
title: Unterstützen der Nachrichtendienstkonfiguration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f2b7c5dfc745ef97051f391d6a3dd68766ef844b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629529"
---
# <a name="supporting-message-service-configuration"></a>Unterstützen der Nachrichtendienstkonfiguration
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gehen Sie folgendermaßen vor, um die Konfiguration des Nachrichtendiensts zu unterstützen:
  
1. Implementieren Sie eine Einstiegspunktfunktion, die dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) entspricht. Nachrichtendienst-Einstiegspunktfunktionen verwalten den Zugriff auf Konfigurationsdaten und werden unter den folgenden Umständen aufgerufen: 
    
   - Wenn sich ein Client anmeldet, um Informationen zum Konfigurieren des Nachrichtendiensts abzurufen.
    
   - Wenn ein Client eine Konfigurationseigenschaft anzeigen oder ändern möchte. 
    
   Obwohl die meisten Nachrichtendienste Wie gewünscht Einstiegspunktfunktionen bereitstellen, sind diese Funktionen nicht unbedingt erforderlich. Nachrichtendienste können auf andere Weise Zugriff auf Konfigurationsdaten bereitstellen. Die Verwendung einer Einstiegspunktfunktion standardisiert und vereinfacht jedoch den Konfigurationsprozess.
    
   MAPI erwartet, dass alle Nachrichtendienst-Einstiegspunktfunktionen Eigenschaften aus den Profilabschnitten speichern und abrufen können, die ihrem Nachrichtendienst zugeordnet sind. Sie können diese Funktionalität interaktiv, programmgesteuert oder interaktiv und programmgesteuert unterstützen.
    
   Um die interaktive Konfiguration zu unterstützen, stellen Sie ein Eigenschaftenblatt bereit, das die Eigenschaften anzeigt, die bei der Konfiguration des Nachrichtendiensts beteiligt sind. Alternativ können Sie auch Eigenschaftenblätter für jeden konfigurierbaren Anbieter bereitstellen. Einige Nachrichtendienste schränken Benutzer auf eine schreibgeschützte Ansicht der Konfigurationseigenschaften ein. Andere Nachrichtendienste ermöglichen Benutzern das Vornehmen von Änderungen.
    
   Um die programmgesteuerte Konfiguration zu unterstützen, muss ihre Nachrichtendienst-Einstiegspunktfunktion ohne Benutzereingriff funktionieren können. Wenn Der Nachrichtendienst vom Profil-Assistenten aufgerufen werden kann, müssen Sie die programmgesteuerte Konfiguration unterstützen. Wenn sich Ihr Nachrichtendienst nicht selbst mithilfe des Profil-Assistenten konfigurieren lässt, können Sie auswählen, ob die programmgesteuerte Konfiguration unterstützt werden soll.
    
   Weitere Informationen zur Unterstützung der Konfiguration in einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter [MSGSERVICEENTRY.](msgserviceentry.md)
    
2. Veröffentlichen Sie den Namen Ihrer Nachrichtendienst-Einstiegspunktfunktion in der Konfigurationsdatei "Mapisvc.inf", indem Sie den folgenden Eintrag in den Nachrichtendienstabschnitt einschließen:
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. Erstellen Sie ein oder mehrere Dialogfelder für Eigenschaftenblätter zum Anzeigen von Konfigurationsdaten.
    
4. Führen Sie die folgenden Aufgaben aus, wenn Sie zulassen möchten, dass der Profil-Assistent Ihren Nachrichtendienst konfiguriert:
    
   - Implementieren Sie eine Einstiegspunktfunktion, die dem [WIZARDENTRY-Prototyp](wizardentry.md) entspricht. 
    
   - Implementieren Sie eine standardmäßige Windows Dialogfeldprozedur, die dem [SERVICEWIZARDDLGP PROTOTYPING-Prototyp](servicewizarddlgproc.md) entspricht. 
    
   - Verbessern Sie die Einstiegspunktfunktion des Nachrichtendiensts, um auf zusätzliche Ereignisse zu reagieren.
    
## <a name="see-also"></a>Siehe auch

- [Message Service-Implementierung](message-service-implementation.md)

