---
title: QuickSteps zum Entwickeln eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte erfahren Sie mehr über das Entwickeln eines Providers Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796081"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>QuickSteps zum Entwickeln eines Anbieters

Um einen OSC-Anbieter zu entwickeln, müssen Sie die folgenden allgemeinen Schritte ausführen:
  
- Die vier obligatorischen Schnittstellen implementieren: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md). Je nach Ihrem sozialen Netzwerk-Unterstützung für das Zwischenspeichern von Anmeldeinformationen, die nach einer Person für das soziale Netzwerk oder dynamisch synchronisieren Freunde und deren Aktivitäten möchten Sie möglicherweise die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementieren. 
    
- Parallel mit Schnittstellen implementieren testen und Debuggen des OSC-Anbieters. 

- Bereitstellen des OSC-Anbieters.  

- Führen Sie die endgültige Tests vor der Freigabe.
    
## <a name="step-a-implementing-interfaces"></a>Schritt A: Implementieren von Schnittstellen

Ein OSC-Anbieter implementiert Schnittstellen, damit die OSC diese Schnittstellen verwenden kann, um die erforderlichen Informationen zu oder aus dem sozialen Netzwerk, über den OSC-Anbieter zu erhalten. Dazu gehören folgende:
  
- Wie Sie im Anmeldedialogfeld Konto für einen Benutzer darstellen.    
- Gibt an, ob der Anbieter mit Freunde oder Aktivitäten unterstützt wie auf dem sozialen Netzwerk angezeigt.    
- Wie in der Visitenkarte oder Outlook Personenbereich Freunde und Aktivitäten angezeigt.     
- Wann Freunde oder Aktivitäten Informationen auf der Visitenkarte oder Personenbereich zu aktualisieren.
    
Die Informationen wird an die OSC in Form von XML-Zeichenfolgen als Output-Parameter von Schnittstellenmethoden in der Regel vom Anbieter übergeben. Die OSC und einem OSC-Anbieter werden mit dem OSC-Anbieter XML-Schema entsprechen. Im Rahmen die Schnittstellen implementieren, benötigen Sie daher verstehen, wie das XML-Schema Sie Informationen angeben, wie oben aufgelisteten können. 

Die folgenden Ressourcen wird erläutert, wie XML für Anbieterfunktionen für, Freunde und Aktivitäten angeben:
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)    
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)    
- [Funktionen XML-Beispiel](capabilities-xml-example.md)   
- [XML-Code für Funktionen](xml-for-capabilities.md)    
- [Freunde XML-Beispiel](friends-xml-example.md)    
- [XML-Code für Freunde](xml-for-friends.md)   
- [Beispiel für eine Aktivität Feed XML](activity-feed-xml-example.md)   
- [XML-Code für Aktivitäten](xml-for-activities.md)
    
Bevor Sie die Implementierung starten, finden Sie auch in den folgenden Themen Zeit zu sparen Sie weiter unten in den Debugvorgang:
  
- [Technische Anforderungen](technical-requirements.md)    
- [Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md)    
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Schritt B: Debuggen

Das Thema schlägt [Debuggen eines Providers](debugging-a-provider.md) Debuggen von Prozeduren, die Sie beim Entwickeln eines OSC-Providers verwenden können. 
  
Während Sie entwickeln, finden Sie auch auf [Erste bereit OSC-Providers](getting-ready-to-release-an-osc-provider.md) für ein besseres Verständnis der das erwartete Verhalten in bestimmten Szenarien (z. B. grundlegende und formularbasierte Authentifizierung) verwendet werden soll. 
  
## <a name="step-c-deploying"></a>Schritt C: Bereitstellen

Finden Sie unter den folgenden Themen Informationen zu Anforderungen für die Bereitstellung zu erhalten:
  
- [Bereitstellen eines Providers](deploying-a-provider.md)    
- [Registrieren eines Providers](registering-a-provider.md)   
- [Checkliste für Installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Schritt D: Final Tests vor der Freigabe

Je nach Ihrem sozialen Netzwerk und die OSC-Anbieter stehen in der Regel anbieterspezifische Tests aus, die Sie ausführen sollten, bevor Sie vom Dienstanbieter freigeben. Eine Liste mit vorgeschlagenen von Tests finden Sie unter [Erste bereit OSC-Providers](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

