---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Es gibt mehrere Möglichkeiten zum Debuggen eines OSC-Anbieters (Outlook Social Connector):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281069"
---
# <a name="debugging-a-provider"></a>Debuggen eines Providers

Es gibt mehrere Möglichkeiten zum Debuggen eines OSC-Anbieters (Outlook Social Connector): 
  
- Durch Verwenden von Debug-Befehlen in der Menüband-Komponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung, damit OSC verschiedene Aktionen ausführen kann.
    
- Durch die Verwendung von Fiddler zum Nachverfolgen von API-aufrufen und XML, die zwischen einem sozialen Netzwerk und seinem OSC-Anbieter gesendet werden
    
## <a name="debug-buttons"></a>Debug-Schaltflächen

Die OSC-Anbieter Erweiterbarkeit bietet die Möglichkeit zum Debuggen eines OSC-Anbieters. Erstellen Sie zum Debuggen eines Anbieters `DebugProviders` in der Windows-Registrierung unter dem `SocialConnector` Schlüssel einen Wert vom Typ DWORD (wie in der folgenden Abbildung dargestellt), und `DebugProviders` legen Sie den Wert auf 1 fest. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Standardmäßig ist das Anbieter Debugging deaktiviert. Wenn der `DebugProviders` Wert nicht vorhanden ist, oder er vorhanden ist und auf den Wert 0 festgelegt ist, wird das Anbieter Debugging deaktiviert. 
  
Wenn das Anbieter Debugging aktiviert ist, zeigt der OSC ein Warnungsdialogfeld mit ausführlichen Fehlerinformationen an, wenn ein Fehler auftritt, und überprüft alle OSC-Anbieter-XML-Daten anhand des OSC-Anbieter-XML-Schemas. Basierend auf dem für eine XML-Zeichenfolge angegebenen Namespace wird ein mit OSC 1,0 entwickelter OSC-Anbieter anhand der OSC 1,0-Schemadatei OutlookSocialProvider. xsd validiert. Ein OSC-Anbieter, der mit OSC 1,1 oder höher entwickelt wurde, wird anhand der Schemadatei OutlookSocialProvider_ 1.1. xsd validiert. Wenn Sie den `DebugProviders` Wert verwenden, wird die Debug-Warnung für alle geladenen Anbieter anstelle eines bestimmten Anbieters angezeigt. 
  
Zum Anzeigen von Debug-Schaltflächen, die Ihnen beim Debuggen eines Anbieters helfen können, erstellen Sie in der Windows- `SocialConnector` Registrierung unter dem Schlüssel einen `ShowDebugButtons` `ShowDebugButtons` Wert vom Typ DWORD, und legen Sie den Wert auf 1 fest. Um die Debug-Befehlsleistenschaltflächen auszublenden, `ShowDebugButtons` legen Sie den Wert auf 0 fest. 
  
Für Outlook 2010-und Clientanwendungen seit Office 2013 werden die Debug-Schaltflächen auf der Registerkarte **Add-ins** des Explorer-Menübands angezeigt. Für Outlook 2007 und Outlook 2003 werden die Debug-Schaltflächen in der Standardbefehls Leiste des Outlook-Explorer-Fensters angezeigt. 
  
In der folgenden Tabelle werden die Debug-Schaltflächen beschrieben.
  
|**Debug-Schaltfläche**|**Funktion**|
|:-----|:-----|
|Kontakte synchronisieren  <br/> |Veranlasst OSC, den OSC-Anbieter nur für zwischengespeicherte Kontakte zu Fragen.  <br/> |
|GAL-Synchronisierung  <br/> |Veranlasst OSC, Daten aus der globalen Exchange-Adressliste in Outlook-Kontakte aufzufüllen.  <br/> |
|Ungültiger Category-Cache  <br/> |Veranlasst OSC, die Kategorienliste für jeden Speicher neu zu laden, wenn der Aktivitätsfeed aktualisiert wird.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler ist ein Over-The-Wire-Debugging-Tool zum Überprüfen der API-Aufrufe, die von Ihrem Anbieter an das soziale Netzwerk gesendet werden, und XML, die vom sozialen Netzwerk an Ihren Anbieter gesendet werden. Fiddler kann unter [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp)heruntergeladen werden.
  
## <a name="see-also"></a>Siehe auch

- [Schnelle Schritte für die Entwicklung eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

