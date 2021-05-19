---
title: QuickSteps zum Entwickeln eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte zum Entwickeln eines Outlook Social Connector (OSC) vorgeschlagen.
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424217"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>QuickSteps zum Entwickeln eines Anbieters

Zum Entwickeln eines OSC-Anbieters müssen Sie die folgenden allgemeinen Schritte ausführen:
  
- Implementieren Sie die vier obligatorischen Schnittstellen: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md). Abhängig von der Unterstützung Ihres sozialen Netzwerks für das Zwischenspeichern von Anmeldeinformationen, das Folgen einer Person im sozialen Netzwerk oder die dynamische Synchronisierung von Freunden und ihren Aktivitäten sollten Sie die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementieren. 
    
- Testen und debuggen Sie parallel zur Implementierung von Schnittstellen den OSC-Anbieter. 

- Bereitstellen des OSC-Anbieters.  

- Durchführen der letzten Tests vor der Veröffentlichung.
    
## <a name="step-a-implementing-interfaces"></a>Schritt A: Implementieren von Schnittstellen

Ein OSC-Anbieter implementiert Schnittstellen, damit das OSC diese Schnittstellen verwenden kann, um über den OSC-Anbieter erforderliche Informationen über oder aus dem sozialen Netzwerk zu erhalten. Diese Informationen umfassen Folgendes:
  
- So stellen Sie einem Benutzer das Anmeldedialogfeld des Kontos vor.    
- Gibt an, ob der Anbieter die Anzeige von Freunden oder Aktivitäten unterstützt, die im sozialen Netzwerk angezeigt werden.    
- Anzeigen von Freunden und Aktivitäten in der Visitenkarte oder Outlook Personenbereich.     
- Informationen zum Aktualisieren von Freunden oder Aktivitäten auf der Visitenkarte oder im Personenbereich.
    
Die Informationen werden in der Regel vom Anbieter an die OSC in Form von XML-Zeichenfolgen als Ausgabeparameter von Schnittstellenmethoden übergeben. Sowohl der OSC als auch ein OSC-Anbieter entsprechen dem XML-Schema des OSC-Anbieters. Daher benötigen Sie bei der Implementierung der Schnittstellen ein gutes Verständnis dafür, wie Das XML-Schema es Ihnen ermöglicht, Informationen wie oben aufgeführt anzugeben. 

In den folgenden Ressourcen wird erläutert, wie Sie XML für Anbieterfunktionen, Freunde und Aktivitäten angeben:
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)    
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)    
- [Capabilities XML(Beispiel)](capabilities-xml-example.md)   
- [XML für Funktionen](xml-for-capabilities.md)    
- [Friends-XML-Beispiel](friends-xml-example.md)    
- [XML für Freunde](xml-for-friends.md)   
- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)   
- [XML für Aktivitäten](xml-for-activities.md)
    
Bevor Sie mit der Implementierung beginnen, lesen Sie auch die folgenden Themen, um Später im Debugprozess Zeit zu sparen:
  
- [Technische Anforderungen](technical-requirements.md)    
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)    
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Schritt B: Debuggen

Im Thema [Debuggen eines Anbieters](debugging-a-provider.md) werden Debugverfahren vorgeschlagen, die Sie bei der Entwicklung eines OSC-Anbieters verwenden können. 
  
Während Der Entwicklung können Sie sich auch auf [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) beziehen, um sich ein besseres Verständnis des erwarteten Verhaltens in bestimmten Szenarien (z. B. einfache und formularbasierte Authentifizierung) zu verschaffen. 
  
## <a name="step-c-deploying"></a>Schritt C: Bereitstellen

Weitere Informationen zu Bereitstellungsanforderungen finden Sie in den folgenden Themen:
  
- [Bereitstellen eines Providers](deploying-a-provider.md)    
- [Registrieren eines Anbieters](registering-a-provider.md)   
- [Prüfliste für die Installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Schritt D: Abschließende Tests vor der Veröffentlichung

Abhängig von Ihrem sozialen Netzwerk und dem OSC-Anbieter gibt es in der Regel anbieterspezifische Tests, die Sie vor der Veröffentlichung Ihres Anbieters durchführen sollten. Eine vorgeschlagene Liste der Tests finden Sie unter [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

