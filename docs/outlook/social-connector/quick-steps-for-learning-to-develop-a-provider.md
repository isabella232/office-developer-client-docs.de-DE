---
title: QuickSteps zum Entwickeln eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: In diesem Thema werden einige Schritte zum Entwickeln eines Outlook Social Connector (OSC)-Anbieters erläutert.
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329218"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>QuickSteps zum Entwickeln eines Anbieters

Zum Entwickeln eines OSC-Anbieters müssen Sie die folgenden allgemeinen Schritte ausführen:
  
- Implementieren Sie die vier obligatorischen Schnittstellen: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)und [ISocialPerson](isocialpersoniunknown.md). Abhängig von der Unterstützung ihres sozialen Netzwerks für das Zwischenspeichern von Anmeldeinformationen, nach einer Person im sozialen Netzwerk oder der dynamischen Synchronisierung von Freunden und ihren Aktivitäten, möchten Sie möglicherweise die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementieren. 
    
- Testen und Debuggen Sie parallel zum Implementieren von Schnittstellen den OSC-Anbieter. 

- Stellen Sie den OSC-Anbieter bereit.  

- Führen Sie die letzten Tests vor der Version aus.
    
## <a name="step-a-implementing-interfaces"></a>Schritt A: Implementieren von Schnittstellen

Ein OSC-Anbieter implementiert Schnittstellen, sodass OSC mithilfe dieser Schnittstellen die erforderlichen Informationen über oder aus dem sozialen Netzwerk über den OSC-Anbieter abrufen kann. Diese Informationen umfassen Folgendes:
  
- VorGehensWeise zum Darstellen des Konto Anmeldedialogfelds für einen Benutzer.    
- Ob der Anbieter unterstützt, Freunde oder Aktivitäten anzuzeigen, die im sozialen Netzwerk angezeigt werden.    
- Anzeigen von Freunden und Aktivitäten im Bereich VisitenKarte oder Outlook-Personen.     
- Zeitpunkt, zu dem die Informationen zu Freunden oder Aktivitäten auf der VisitenKarte oder im Personen Bereich aktualisiert werden sollen.
    
Die Informationen werden in der Regel vom Anbieter an den OSC in Form von XML-Zeichenfolgen als Ausgabeparameter der Interface-Methoden übergeben. Sowohl der OSC als auch ein OSC-Anbieter entsprechen dem XML-Schema des OSC-Anbieters. Daher benötigen Sie im Zuge der Implementierung der Schnittstellen ein gutes Verständnis dafür, wie Sie mit dem XML-Schema die oben aufgeführten Informationen angeben können. 

In den folgenden Ressourcen wird erläutert, wie Sie XML für Anbieter Funktionen, Freunde und Aktivitäten angeben:
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)    
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)    
- [XML-Beispiel für Funktionen](capabilities-xml-example.md)   
- [XML für Funktionen](xml-for-capabilities.md)    
- [XML-Beispiel für Freunde](friends-xml-example.md)    
- [XML für Freunde](xml-for-friends.md)   
- [XML-Beispiel für Aktivitätsfeeds](activity-feed-xml-example.md)   
- [XML für Aktivitäten](xml-for-activities.md)
    
Bevor Sie mit der Implementierung beginnen, sollten Sie auch die folgenden Themen konsultieren, um Zeit später beim Debugging zu sparen:
  
- [Technische Anforderungen](technical-requirements.md)    
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)    
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Schritt B: Debuggen

Das Thema [Debuggen eines Anbieters](debugging-a-provider.md) schlägt Debuggingverfahren vor, die Sie beim Entwickeln eines osc-Anbieters verwenden können. 
  
Während Sie sich entwickeln, können Sie auch auf die [Bereitstellung der Freigabe eines osc](getting-ready-to-release-an-osc-provider.md) -Anbieters verweisen, um ein besseres Verständnis des erwarteten Verhaltens in bestimmten Szenarien zu erlangen (beispielsweise grundlegende und formularbasierte Authentifizierung). 
  
## <a name="step-c-deploying"></a>Schritt C: Bereitstellen

Weitere Informationen zu Bereitstellungsanforderungen finden Sie in den folgenden Themen:
  
- [Bereitstellen eines Providers](deploying-a-provider.md)    
- [Registrieren eines Anbieters](registering-a-provider.md)   
- [PrüfListe für die Installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Schritt D: abschließende Tests vor der Freigabe

Je nach sozialem Netzwerk und OSC-Anbieter gibt es in der Regel anbieterspezifische Tests, die Sie ausführen müssen, bevor Sie Ihren Anbieter freigeben. Eine vorgeschlagene Liste von Tests finden Sie unter Vorbereiten der [Freigabe eines osc](getting-ready-to-release-an-osc-provider.md)-Anbieters.
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

