---
title: Für OSC typische Aufrufsequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: In diesem Abschnitt wird die Outlook OSC(Social Connector) typische Aufrufsequenzen von Mitgliedern in den OSC-Anbietererweiterungsschnittstellen beschrieben, die ein OSC-Anbieter implementiert.
ms.openlocfilehash: 5106bc31cab1854cba07d5188a5888ea5f382d50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566178"
---
# <a name="osc-typical-calling-sequences"></a>Für OSC typische Aufrufsequenzen

In diesem Abschnitt wird die Outlook OSC(Social Connector) typische Aufrufsequenzen von Mitgliedern in den OSC-Anbietererweiterungsschnittstellen beschrieben, die ein OSC-Anbieter implementiert. Die typischen Aufrufsequenzen veranschaulichen, wie und wann osc solche Schnittstellen und Methoden verwendet, um besser zu bestimmen, wie ein bestimmtes Element auf einer Anbietererweiterungsschnittstelle implementiert werden soll. Die tatsächliche Aufrufsequenz kann abhängig von den von der [ISocialProvider::GetCapabilities-Methode zurückgegebenen](isocialprovider-getcapabilities.md) Funktionen variieren. Beispiele für Funktionen sind: 
  
- Anbieterunterstützung für das Abrufen, Zwischenspeichern oder dynamisches Nachschlagen von Freunden und Aktivitäten aus dem sozialen Netzwerk.
    
- Die Benutzeroberfläche, die der OSC für die Benutzeranmeldung anzeigen soll.
    
- Der Authentifizierungstyp (z. B. formularbasierte Authentifizierung), der vom OSC verwendet werden soll.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Standardauthentifizierung:](basic-authentication.md)Beschreibt die typische Aufrufsequenz des OSC zur Unterstützung eines Office Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der OSC-Anbieter die Standardauthentifizierung unterstützt.
    
- [Formularbasierte Authentifizierung:](forms-based-authentication.md)Beschreibt die typische Aufrufsequenz des OSC zur Unterstützung eines Office Benutzers, der sich bei einem sozialen Netzwerk anmeldet, wenn der OSC-Anbieter die formularbasierte Authentifizierung unterstützt.
    
- Abrufen von [Aktivitäten:](getting-activities.md)Beschreibt die typische Aufrufsequenz des OSC zum Synchronisieren der Aktivitäten der Freunde des Office Benutzers aus einem sozialen Netzwerk, wenn der OSC-Anbieter des sozialen Netzwerks die Synchronisierung von Aktivitäten unterstützt.
    
- Abrufen von [Informationen zu Freunden:](getting-friends-information.md)Beschreibt die typische Anrufsequenz des OSC zum Synchronisieren der Freundesliste des Office Benutzers aus einem sozialen Netzwerk, wenn der OSC-Anbieter des sozialen Netzwerks die zwischengespeicherte Synchronisierung von Kontakten unterstützt.
    
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

