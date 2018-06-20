---
title: Vorbereiten eines OSC-Providers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: In diesem Abschnitt wird die Tests, die Sie ausführen können, bevor Sie Ihren Outlook Social Connector (OSC)-Anbieter freigeben.
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795961"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Vorbereiten eines OSC-Providers

In diesem Abschnitt wird die Tests, die Sie ausführen können, bevor Sie Ihren Outlook Social Connector (OSC)-Anbieter freigeben. Können in Bezug auf die Themen in diesem Abschnitt starten und einige dieser Tests während der Entwicklungs- und Testphase Suchtool, aber Sie sollten diese Tests durch die Zeit, die Sie freigeben abgeschlossen haben. 

Diese Tests überprüfen, ob die grundlegende Funktionen der Implementierung der OSC-Anbieter Schnittstellen in Bezug auf die Funktionen, die Sie für den OSC-Anbieter angeben. Darüber hinaus, obwohl die OSC ein Feature von mehreren Office-Clientanwendungen gemeinsam genutzt wird, verwenden Sie diese Tests Outlook als Client zum Testen der grundlegenden Funktionalität. Sie sollten bestimmen, ob andere Tests an Ihren Anbieter für bestimmte Features erforderlich sind.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Testen der Bereitstellung](testing-deployment.md): Szenarien, die Sie für testen sollten, um die Installation und Deinstallation von einem OSC-Anbieter beschrieben.
    
- [Testen der Funktionen, Authentifizierung und Konfiguration](testing-capabilities-authentication-and-configuration.md): werden die Tests für das Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und Authentifizieren eines Benutzers für ein social Network beschrieben.
    
- [In der folgenden Tests und Stop-folgenden Personen](testing-following-and-stop-following-persons.md): Beschreibt Szenarien zum Testen, ob der OSC-Anbieter, um eine Person als Freund hinzuzufügen oder um einen Freund aus dem sozialen Netzwerk zu entfernen. 
    
- [Testen der Freunde](testing-friends.md): Beschreibt Tests und Szenarien zu überprüfen, ob der OSC-Anbieter entsprechend Daten Freunde und nicht-Freunde, sofern zutreffend, je nach den Synchronisierungsmodus zurückgibt, die vom Anbieter unterstützt.
    
- [Testen von Aktivitäten](testing-activities.md): Beschreibt Tests und Szenarien zu überprüfen, ob der OSC-Anbieter entsprechend Aktivitäten Freunde und nicht-Freunde, sofern zutreffend, je nach den Synchronisierungsmodus zurückgibt, die vom Anbieter unterstützt.
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  

