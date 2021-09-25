---
title: Vorbereiten der Veröffentlichung eines OSC-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt werden Tests vorgeschlagen, die Sie durchführen können, bevor Sie Ihren osc-Anbieter (Outlook Connector für soziale Netzwerke) freigeben.
ms.openlocfilehash: 32fe16dacb0af5b42b6884de1982452076d5615f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629186"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Vorbereiten der Veröffentlichung eines OSC-Anbieters

In diesem Abschnitt werden Tests vorgeschlagen, die Sie durchführen können, bevor Sie Ihren osc-Anbieter (Outlook Connector für soziale Netzwerke) freigeben. Sie können beginnen, auf die Themen in diesem Abschnitt zu verweisen und einige dieser Tests während Ihrer Entwicklungs- und Testphasen durchzuführen, aber Sie sollten diese Tests zum Zeitpunkt der Veröffentlichung abgeschlossen haben. 

Diese Tests überprüfen die grundlegende Funktionalität Ihrer Implementierung der OSC-Anbieterschnittstellen in Bezug auf die Funktionen, die Sie für den OSC-Anbieter angeben. Obwohl es sich bei OSC um ein Feature handelt, das von mehreren Office Clientanwendungen gemeinsam verwendet wird, verwenden diese Tests Outlook als Client, um die grundlegende Funktionalität zu testen. Sie sollten ermitteln, ob für Features, die für Ihren Anbieter spezifisch sind, andere Tests erforderlich sind.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Testen der Bereitstellung:](testing-deployment.md)Beschreibt Szenarien, auf die Sie testen sollten, um einen OSC-Anbieter zu installieren und zu deinstallieren.
    
- [Testfunktionen, Authentifizierung und Konfiguration:](testing-capabilities-authentication-and-configuration.md)Beschreibt Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und authentifizieren eines Benutzers für ein soziales Netzwerk.
    
- [Testen der folgenden und Stop-Following Personen:](testing-following-and-stop-following-persons.md)Beschreibt Szenarien zum Testen der Fähigkeit des OSC-Anbieters, eine Person als Freund hinzuzufügen oder einen Freund aus dem sozialen Netzwerk zu entfernen. 
    
- [Testen von Freunden:](testing-friends.md)Beschreibt Tests und Szenarien, um zu überprüfen, ob der OSC-Anbieter abhängig vom vom Anbieter unterstützten Synchronisierungsmodus gegebenenfalls Daten von Freunden und Nicht-Freunden zurückgibt.
    
- [Testaktivitäten:](testing-activities.md)Beschreibt Tests und Szenarien, um zu überprüfen, ob der OSC-Anbieter abhängig vom vom Anbieter unterstützten Synchronisierungsmodus gegebenenfalls Aktivitäten von Freunden und Nicht-Freunden zurückgibt.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  

