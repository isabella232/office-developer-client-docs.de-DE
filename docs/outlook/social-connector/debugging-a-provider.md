---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Sie haben verschiedene Möglichkeiten, die Sie einen Anbieter für Outlook Social Connector (OSC) debuggen können:'
ms.openlocfilehash: ada439ca3b038ca9a0e849b47ff6a5f54e5016f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795960"
---
# <a name="debugging-a-provider"></a>Debuggen eines Providers

Sie haben verschiedene Möglichkeiten, die Sie einen Anbieter für Outlook Social Connector (OSC) debuggen können: 
  
- Mithilfe von Debug-Befehle in der Menübandkomponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung, die dazu führen, dass die OSC verschiedene Aktionen ausführen.
    
- Mithilfe von Fiddler Trace-API-Aufrufe und XML, die zwischen einem sozialen Netzwerk und den OSC-Anbieter gesendet
    
## <a name="debug-buttons"></a>Debuggen von Schaltflächen

Die Erweiterbarkeit des OSC-Providers bietet die Möglichkeit zum Debuggen eines OSC-Providers. Um einen Anbieter zu debuggen, Erstellen einer `DebugProviders` Wert des Typs DWORD-Wert in der Windows-Registrierung unter der `SocialConnector` wichtige (wie in der folgenden Zeile dargestellt), und legen Sie die `DebugProviders` Wert auf 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Standardmäßig ist das Debuggen Anbieter deaktiviert. Wenn die `DebugProviders` Wert ist nicht vorhanden, oder es vorhanden ist und auf einen Wert von 0 Anbieter Debuggen festgelegt ist deaktiviert. 
  
Wenn der Anbieter das Debuggen aktiviert ist, zeigt die OSC ein Warnungsdialogfeld mit ausführlichen Fehlerinformationen, wenn ein Fehler tritt auf, und alle OSC-Anbieter XML für das OSC-Anbieter XML-Schema überprüft. Basierend auf den Namespace für eine XML-Zeichenfolge angegeben, wird der OSC 1.0-Schemadatei OutlookSocialProvider.xsd ein OSC-Anbieters mit OSC 1.0 entwickelt überprüft. Ein OSC-Anbieters mithilfe von OSC 1.1 entwickelt oder später anhand der Schemadatei OutlookSocialProvider_1.1.xsd überprüft wird. Bei Verwendung der `DebugProviders` -Wert, die Debug-Benachrichtigung wird für alle geladenen Anbieter anstelle eines bestimmten Anbieters angezeigt. 
  
Um Debug Schaltflächen anzuzeigen, die beim Debuggen eines Providers helfen kann, Erstellen einer `ShowDebugButtons` Wert des Typs DWORD-Wert in der Windows-Registrierung unter der `SocialConnector` -Taste, und legen Sie die `ShowDebugButtons` Wert auf 1. Legen Sie zum Ausblenden der Befehlsleisten-Schaltflächen Debuggen die `ShowDebugButtons` Wert auf 0. 
  
Für Outlook 2010 und Clientanwendungen gegenüber Office 2013 werden die Debug-Schaltflächen auf der Registerkarte ' **Add-Ins** ' des Menübands Explorer angezeigt. Für Outlook 2007 und Outlook 2003 werden die Debug-Schaltflächen auf der standard-Befehlsleiste für das Outlook Explorer-Fenster angezeigt. 
  
Die folgende Tabelle beschreibt die Debug-Schaltflächen.
  
|**Schaltfläche Debuggen**|**Funktion**|
|:-----|:-----|
|Kontakte synchronisieren  <br/> |Bewirkt, dass das osc bilden den OSC-Anbieter zur zwischengespeicherten Kontakte nur aufgefordert.  <br/> |
|Synchronisierung der globalen Adressliste  <br/> |Bewirkt, dass die OSC zum Auffüllen von Daten aus der globalen Adressliste von Exchange zu Outlook-Kontakten.  <br/> |
|Kategorie Cache ungültig  <br/> |Bewirkt, dass das osc bilden, die Kategorieliste für jeden Speicher erneut zu laden, wenn die Aktivitätsfeed aktualisiert wird.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler ist ein Tool zum Debuggen von über das Netzwerk, die API-Aufrufe, die von Ihrem Dienstanbieter in sozialen Netzwerken gesendet und dem sozialen Netzwerk an Ihren Anbieter gesendeten XML überprüfen. Fiddler steht unter [Fiddler Web Debugging Proxy](http://www.fiddler2.com/fiddler2/version.asp)zum Download zur Verfügung.
  
## <a name="see-also"></a>Siehe auch

- [QuickSteps für Informationen zum Entwickeln eines Providers](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md) 
- [Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

