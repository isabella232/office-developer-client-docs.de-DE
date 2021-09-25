---
title: QuickSteps zum Entwickeln eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte zum Entwickeln eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) vorgeschlagen.
ms.openlocfilehash: 3dbb4e40a3cfe3d2b37c7b2fb9ef60515640adc6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629060"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>QuickSteps zum Entwickeln eines Anbieters

Um einen OSC-Anbieter zu entwickeln, müssen Sie die folgenden allgemeinen Schritte ausführen:
  
- Implementieren Sie die vier obligatorischen Schnittstellen: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md). Abhängig von der Unterstützung Ihres sozialen Netzwerks für das Zwischenspeichern von Anmeldeinformationen, dem Folgen einer Person im sozialen Netzwerk oder dem dynamischen Synchronisieren von Freunden und deren Aktivitäten sollten Sie die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementieren. 
    
- Testen und debuggen Sie parallel zur Implementierung von Schnittstellen den OSC-Anbieter. 

- Stellen Sie den OSC-Anbieter bereit.  

- Führen Sie abschließende Tests vor der Veröffentlichung durch.
    
## <a name="step-a-implementing-interfaces"></a>Schritt A: Implementieren von Schnittstellen

Ein OSC-Anbieter implementiert Schnittstellen, sodass der OSC diese Schnittstellen verwenden kann, um über den OSC-Anbieter erforderliche Informationen über oder aus dem sozialen Netzwerk abzurufen. Diese Informationen umfassen Folgendes:
  
- Anzeigen des Anmeldedialogfelds für ein Konto für einen Benutzer    
- Gibt an, ob der Anbieter das Anzeigen von Freunden oder Aktivitäten wie im sozialen Netzwerk unterstützt.    
- Anzeigen von Freunden und Aktivitäten im Kontaktkarten- oder Outlook Personenbereich.     
- Wann die Informationen zu Freunden oder Aktivitäten auf der Visitenkarte oder im Personenbereich aktualisiert werden sollen.
    
Die Informationen werden in der Regel vom Anbieter an osc übergeben, in Form von XML-Zeichenfolgen als Ausgabeparameter von Schnittstellenmethoden. Sowohl der OSC als auch ein OSC-Anbieter entsprechen dem OSC-Anbieter-XML-Schema. Daher benötigen Sie bei der Implementierung der Schnittstellen ein gutes Verständnis dafür, wie Sie mit dem XML-Schema Informationen wie oben aufgeführt angeben können. 

In den folgenden Ressourcen wird erläutert, wie Sie XML für Anbieterfunktionen, Freunde und Aktivitäten angeben:
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)    
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)    
- [Xml-Beispiel für Funktionen](capabilities-xml-example.md)   
- [XML für Funktionen](xml-for-capabilities.md)    
- [Xml-Beispiel für Freunde](friends-xml-example.md)    
- [XML für Freunde](xml-for-friends.md)   
- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)   
- [XML für Aktivitäten](xml-for-activities.md)
    
Bevor Sie mit der Implementierung beginnen, lesen Sie auch die folgenden Themen, um Später im Debugprozess Zeit zu sparen:
  
- [Technische Anforderungen](technical-requirements.md)    
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)    
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Schritt B: Debuggen

Im Thema ["Debuggen eines Anbieters"](debugging-a-provider.md) werden Debuggingprozeduren vorgeschlagen, die Sie beim Entwickeln eines OSC-Anbieters verwenden können. 
  
Während der Entwicklung können Sie sich auch auf ["Vorbereiten der Veröffentlichung eines OSC-Anbieters"](getting-ready-to-release-an-osc-provider.md) beziehen, um ein besseres Verständnis des erwarteten Verhaltens in bestimmten Szenarien (z. B. standard- und formularbasierte Authentifizierung) zu erhalten. 
  
## <a name="step-c-deploying"></a>Schritt C: Bereitstellen

Lesen Sie die folgenden Themen, um mehr über die Bereitstellungsanforderungen zu erfahren:
  
- [Bereitstellen eines Providers](deploying-a-provider.md)    
- [Registrieren eines Anbieters](registering-a-provider.md)   
- [Prüfliste für die Installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Schritt D: Abschließende Tests vor der Veröffentlichung

Abhängig von Ihrem sozialen Netzwerk und dem OSC-Anbieter gibt es in der Regel anbieterspezifische Tests, die Sie durchführen sollten, bevor Sie Ihren Anbieter freigeben. Eine vorgeschlagene Liste von Tests finden Sie unter ["Vorbereiten der Veröffentlichung eines OSC-Anbieters".](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

