---
title: Für OSC typische Aufrufsequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: In diesem Abschnitt werden die typischen Anruf Sequenzen für Outlook Social Connector (OSC) von Mitgliedern in den OSC-Erweiterbarkeitsschnittstellen beschrieben, die ein OSC-Anbieter implementiert.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356266"
---
# <a name="osc-typical-calling-sequences"></a>Für OSC typische Aufrufsequenzen

In diesem Abschnitt werden die typischen Anruf Sequenzen für Outlook Social Connector (OSC) von Mitgliedern in den OSC-Erweiterbarkeitsschnittstellen beschrieben, die ein OSC-Anbieter implementiert. Die typischen Aufrufsequenzen veranschaulichen, wie und wann der OSC solche Schnittstellen und Methoden verwendet, damit Sie besser bestimmen können, wie Sie ein bestimmtes Element auf einer Anbieter Erweiterungsschnittstelle implementieren können. Die tatsächliche Aufrufsequenz kann je nach den von der [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebenen Funktionen variieren. Beispiele für Funktionen sind: 
  
- Anbieterunterstützung für das Abrufen, Zwischenspeichern oder dynamisches Nachschlagen von Freunden und Aktivitäten aus dem sozialen Netzwerk.
    
- Die Benutzeroberfläche, die vom OSC für die Benutzeranmeldung angezeigt werden soll.
    
- Der Authentifizierungstyp (beispielsweise die formularbasierte Authentifizierung), der vom OSC verwendet werden soll.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Standardauthentifizierung](basic-authentication.md): Beschreibt die typische Anruffolge des osc zur Unterstützung eines Office-Benutzers, der sich an einem sozialen Netzwerk anmeldet, wenn der osc-Anbieter die Standardauthentifizierung unterstützt.
    
- [Formularbasierte Authentifizierung](forms-based-authentication.md): Beschreibt die typische Aufrufsequenz des osc zur Unterstützung eines Office-Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der osc-Anbieter die formularbasierte Authentifizierung unterstützt.
    
- [Abrufen von Aktivitäten](getting-activities.md): Beschreibt die typische Aufrufsequenz des osc, um die Aktivitäten der Freunde des Office-Benutzers von einem sozialen Netzwerk zu synchronisieren, wenn der Netzwerk-osc-Anbieter die Synchronisierung von Aktivitäten unterstützt.
    
- [Informationen zu Freunden](getting-friends-information.md): Beschreibt die typische Anruf Sequenz des osc, um die Freundesliste des Office-Benutzers aus einem sozialen Netzwerk zu synchronisieren, wenn der osc-Anbieter für soziale Netzwerke die zwischengespeicherte Synchronisierung von Kontakten unterstützt.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)

