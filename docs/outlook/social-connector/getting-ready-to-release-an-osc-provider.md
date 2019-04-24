---
title: Vorbereiten der Freigabe eines OSC-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt werden Tests vorgeschlagen, die Sie vor der Freigabe des OSC-Anbieters (Outlook Social Connector) ausführen können.
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327153"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Vorbereiten der Freigabe eines OSC-Anbieters

In diesem Abschnitt werden Tests vorgeschlagen, die Sie vor der Freigabe des OSC-Anbieters (Outlook Social Connector) ausführen können. Sie können mit den Themen in diesem Abschnitt beginnen und einige dieser Tests während der Entwicklungs-und Testphase durchführen, aber Sie sollten diese Tests mit der Zeit abgeschlossen haben, die Sie freigeben. 

Diese Tests überprüfen die grundlegenden Funktionen der Implementierung der OSC-Anbieterschnittstellen im Hinblick auf die Funktionen, die Sie für den OSC-Anbieter angeben. Auch wenn OSC ein Feature ist, das von mehreren Office-Clientanwendungen gemeinsam verwendet wird, verwenden diese Tests Outlook als Client, um die grundlegenden Funktionen zu testen. Sie sollten bestimmen, ob andere Tests für für Ihren anbieterspezifische Funktionen erforderlich sind.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Testen der Bereitstellung](testing-deployment.md): Beschreibt Szenarien, die Sie bei der Installation und Deinstallation eines osc-Anbieters testen sollten.
    
- [Testen von Funktionen, Authentifizierung und Konfiguration](testing-capabilities-authentication-and-configuration.md): Beschreibt Tests für das erhalten von Funktionen und Szenarios zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk.
    
- [TestIng folgende und Stop-folgende Personen](testing-following-and-stop-following-persons.md): Beschreibt Szenarien zum Testen des osc-Anbieters zum Hinzufügen einer Person als Freund oder zum Entfernen eines Freundes aus dem sozialen Netzwerk. 
    
- [Testen von Freunden](testing-friends.md): Beschreibt Tests und Szenarien, um zu überprüfen, ob der osc-Anbieter entsprechend der vom Anbieter unterstützten Synchronisierungsmodus Daten von Freunden und nicht-Freunden zurückgibt.
    
- [Testaktivitäten](testing-activities.md): Beschreibt Tests und Szenarien, um zu überprüfen, ob der osc-Anbieter ordnungsgemäß Aktivitäten von Freunden und nicht-Freunden, je nach dem vom Anbieter unterstützten Synchronisierungsmodus, zurückgibt.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  

