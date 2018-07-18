---
title: Für OSC typische Aufrufsequenzen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Dieser Abschnitt beschreibt die typischen aufrufende Outlook Social Connector (OSC) Sequenzen der Elemente in die OSC-Anbieter Erweiterungsschnittstellen, die ein OSC-Anbieter implementiert.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796074"
---
# <a name="osc-typical-calling-sequences"></a>Für OSC typische Aufrufsequenzen

Dieser Abschnitt beschreibt die typischen aufrufende Outlook Social Connector (OSC) Sequenzen der Elemente in die OSC-Anbieter Erweiterungsschnittstellen, die ein OSC-Anbieter implementiert. Die normalen aufrufenden Sequenzen veranschaulichen, wie und wann die OSC verwendet diese Schnittstellen und Methoden, mit der Sie eine bessere können bestimmen, wie einen bestimmten Member für einen Anbieter Erweiterbarkeitsschnittstelle implementiert. Die tatsächliche aufrufende Sequenz kann je nach den Möglichkeiten, die von der [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebene variieren. Die folgenden: Beispiele für Funktionen 
  
- Anbieter unterstützt für die erste, Zwischenspeichern oder dynamisch Nachschlagen Freunde und Aktivitäten aus dem sozialen Netzwerk.
    
- Die Benutzeroberfläche, die die OSC für die Benutzeranmeldung angezeigt werden sollen.
    
- Der Authentifizierungstyp (beispielsweise formularbasierte Authentifizierung), den die OSC verwendet werden soll.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Standardauthentifizierung](basic-authentication.md): Beschreibt die typische aufrufende Abfolge der die OSC unterstützen Sie einen Office-Benutzer, die mit einem sozialen Netzwerk angemeldet ist, wenn der OSC-Anbieter Standardauthentifizierung unterstützt.
    
- [Formularbasierte Authentifizierung](forms-based-authentication.md): Beschreibt die typische aufrufende Abfolge der die OSC unterstützen Sie einen Office-Benutzer, die mit einem sozialen Netzwerk angemeldet ist, wenn der OSC-Anbieter formularbasierte Authentifizierung unterstützt.
    
- [Erste Aktivitäten](getting-activities.md): Beschreibt die typische aufrufende Abfolge der die OSC zum Synchronisieren der Aktivitäten des Office-Benutzers Freunde aus einem sozialen Netzwerk, wenn der OSC-Anbieter für soziale Netzwerke Synchronisierung von Aktivitäten unterstützt.
    
- [Erste Freunde Informationen](getting-friends-information.md): Beschreibt die normale aufrufende Abfolge der die OSC Freunde-Liste der Office-Benutzer von einem sozialen Netzwerk, synchronisieren, wenn der OSC-Anbieter für soziale Netzwerke zwischengespeicherten Synchronisierung von Kontakten unterstützt.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  
- [Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)

