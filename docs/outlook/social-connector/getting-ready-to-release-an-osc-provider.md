---
title: Bereiten Sie sich auf die Veröffentlichung eines OSC-Anbieters vor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt werden Tests vorgeschlagen, die Sie durchführen können, bevor Sie Outlook Social Connector (OSC) veröffentlichen.
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414662"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Bereiten Sie sich auf die Veröffentlichung eines OSC-Anbieters vor

In diesem Abschnitt werden Tests vorgeschlagen, die Sie durchführen können, bevor Sie Outlook Social Connector (OSC) veröffentlichen. Sie können beginnen, sich auf die Themen in diesem Abschnitt zu beziehen und einige dieser Tests während der Entwicklungs- und Testphase durchzuführen, aber Sie sollten diese Tests bis zum Zeitpunkt der Veröffentlichung abgeschlossen haben. 

Diese Tests überprüfen die grundlegende Funktionalität Ihrer Implementierung der OSC-Anbieterschnittstellen im Hinblick auf die funktionen, die Sie für den OSC-Anbieter angeben. Auch wenn das OSC ein Feature ist, das von mehreren Office-Clientanwendungen gemeinsam genutzt wird, verwenden diese Tests Outlook als Client, um die grundlegenden Funktionen zu testen. Sie sollten bestimmen, ob andere Tests für für Ihren Anbieter spezifische Features erforderlich sind.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Testbereitstellung:](testing-deployment.md)Beschreibt Szenarien, die Sie testen sollten, um einen OSC-Anbieter zu installieren und zu deinstallieren.
    
- [Testfunktionen, Authentifizierung und Konfiguration:](testing-capabilities-authentication-and-configuration.md)Beschreibt Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und zur Authentifizierung eines Benutzers für ein soziales Netzwerk.
    
- [Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Beschreibt Szenarien zum Testen der Fähigkeit des OSC-Anbieters, eine Person als Freund hinzuzufügen oder einen Freund aus dem sozialen Netzwerk zu entfernen. 
    
- [Testen von](testing-friends.md)Freunden : Beschreibt Tests und Szenarien, um zu überprüfen, ob der OSC-Anbieter abhängig vom vom Anbieter unterstützten Synchronisierungsmodus ggf. Daten von Freunden und Nicht-Freunden zurückgibt.
    
- [Testaktivitäten](testing-activities.md): Beschreibt Tests und Szenarien, um zu überprüfen, ob der OSC-Anbieter aktivitäten von Freunden und Nicht-Freunden entsprechend zurückgibt, je nach dem vom Anbieter unterstützten Synchronisierungsmodus.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  

