---
title: Für OSC typische Aufrufsequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: In diesem Abschnitt werden die typischen Outlook (Social Connector, OSC) von Mitgliedern in den Erweiterbarkeitsschnittstellen des OSC-Anbieters beschrieben, die von einem OSC-Anbieter implementiert werden.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413612"
---
# <a name="osc-typical-calling-sequences"></a>Für OSC typische Aufrufsequenzen

In diesem Abschnitt werden die typischen Outlook (Social Connector, OSC) von Mitgliedern in den Erweiterbarkeitsschnittstellen des OSC-Anbieters beschrieben, die von einem OSC-Anbieter implementiert werden. Die typischen Aufrufsequenzen veranschaulichen, wie und wann das OSC solche Schnittstellen und Methoden verwendet, damit Sie besser bestimmen können, wie ein bestimmtes Mitglied auf einer Anbieterergehnbarkeitsschnittstelle implementiert wird. Die tatsächliche Aufrufsequenz kann je nach den von der [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) zurückgegebenen Funktionen variieren. Beispiele für Funktionen sind: 
  
- Anbieterunterstützung zum Abrufen, Zwischenspeichern oder dynamischen Suchen von Freunden und Aktivitäten aus dem sozialen Netzwerk.
    
- Die Benutzeroberfläche, die das OSC für die Benutzeranmeldung anzeigen soll.
    
- Der Authentifizierungstyp (z. B. formularbasierte Authentifizierung), den das OSC verwenden soll.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Standardauthentifizierung](basic-authentication.md): Beschreibt die typische Anrufsequenz der OSC zur Unterstützung eines Office-Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der OSC-Anbieter die Standardauthentifizierung unterstützt.
    
- [Formularbasierte](forms-based-authentication.md)Authentifizierung : Beschreibt die typische Anrufsequenz der OSC zur Unterstützung eines Office-Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der OSC-Anbieter die formularbasierte Authentifizierung unterstützt.
    
- [Abrufen](getting-activities.md)von Aktivitäten : Beschreibt die typische Anrufsequenz des OSC zum Synchronisieren der Aktivitäten der Freunde des Office-Benutzers aus einem sozialen Netzwerk, wenn der Anbieter für soziale Netzwerke die Synchronisierung von Aktivitäten unterstützt.
    
- [Abrufen](getting-friends-information.md)von Freundesinformationen : Beschreibt die typische Anrufsequenz des OSC zum Synchronisieren der Freundesliste des Office-Benutzers aus einem sozialen Netzwerk, wenn der OsC-Anbieter für soziale Netzwerke die zwischengespeicherte Synchronisierung von Kontakten unterstützt.
    
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

