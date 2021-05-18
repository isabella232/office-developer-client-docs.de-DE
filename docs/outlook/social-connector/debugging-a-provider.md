---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Es gibt verschiedene Möglichkeiten, einen Outlook Social Connector (OSC)-Anbieter zu debuggen:'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281069"
---
# <a name="debugging-a-provider"></a>Debuggen eines Providers

Es gibt verschiedene Möglichkeiten, einen Outlook Social Connector (OSC)-Anbieter zu debuggen: 
  
- Durch Die Verwendung von Debugbefehlen in der Menübandkomponente der Office Fluent-Benutzeroberfläche in Outlook oder der unterstützenden Office-Clientanwendung kann die OSC verschiedene Aktionen ausführen.
    
- Verwenden von Fiddler zum Verfolgen von API-Aufrufen und XML, die zwischen einem sozialen Netzwerk und seinem OSC-Anbieter gesendet werden
    
## <a name="debug-buttons"></a>Debugschaltflächen

Die Erweiterbarkeit des OSC-Anbieters bietet die Möglichkeit, einen OSC-Anbieter zu debuggen. Erstellen Sie zum Debuggen eines Anbieters einen Wert vom Typ DWORD in der Windows-Registrierung unter dem Schlüssel (wie in der folgenden Zeile gezeigt), und legen Sie den Wert auf  `DebugProviders`  `SocialConnector`  `DebugProviders` 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Standardmäßig ist das Anbieterdebubugen deaktiviert. Wenn der Wert nicht vorhanden oder vorhanden ist und auf den Wert 0 festgelegt ist, ist das  `DebugProviders` Anbieterdebuding deaktiviert. 
  
Wenn das Anbieterdebuding aktiviert ist, zeigt die OSC ein Benachrichtigungsdialogfeld mit ausführlichen Fehlerinformationen an, wenn ein Fehler auftritt, und überprüft alle XML-Daten des OSC-Anbieters mit dem XML-Schema des OSC-Anbieters. Basierend auf dem für eine XML-Zeichenfolge angegebenen Namespace wird ein mit OSC 1.0 entwickelter OSC-Anbieter mit der OSC 1.0-Schemadatei OutlookSocialProvider.xsd überprüft. Ein mit OSC 1.1 oder höher entwickelter OSC-Anbieter wird anhand der Schemadatei OutlookSocialProvider_1.1.xsd überprüft. Wenn Sie den Wert verwenden, wird die Debugwarnung für alle geladenen Anbieter anstelle  `DebugProviders` eines bestimmten Anbieters angezeigt. 
  
Um Debugschaltflächen anzuzeigen, mit deren Hilfe Sie einen Anbieter debuggen können, erstellen Sie in der Windows-Registrierung unter dem Schlüssel einen Wert vom Typ DWORD, und legen Sie den Wert auf  `ShowDebugButtons`  `SocialConnector`  `ShowDebugButtons` 1 fest. Um die Schaltflächen für die Debugbefehlsleiste auszublenden, legen Sie  `ShowDebugButtons` den Wert auf 0. 
  
Für Outlook 2010 und Clientanwendungen seit Office 2013 werden die Debugschaltflächen auf der Registerkarte **Add-Ins** des Explorer-Menübands angezeigt. Für Outlook 2007 und Outlook 2003 werden die Debugschaltflächen in der Standardbefehlsleiste des Outlook-Explorer-Fensters angezeigt. 
  
In der folgenden Tabelle werden die Debugschaltflächen beschrieben.
  
|**Schaltfläche "Debuggen"**|**Funktion**|
|:-----|:-----|
|Synchronisieren von Kontakten  <br/> |Bewirkt, dass das OSC den OSC-Anbieter nur nach zwischengespeicherten Kontakten fragt.  <br/> |
|GAL-Synchronisierung  <br/> |Bewirkt, dass die OSC Daten aus der globalen Exchange-Adressliste in Outlook-Kontakte auffüllt.  <br/> |
|Ungültiger Kategoriecache  <br/> |Bewirkt, dass das OSC die Kategorieliste für jeden Speicher neu lädt, wenn der Aktivitätsfeed aktualisiert wird.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler ist ein out-the-Wire-Debugging-Tool, um die API-Aufrufe zu überprüfen, die von Ihrem Anbieter an das soziale Netzwerk gesendet werden, und XML, das vom sozialen Netzwerk an Ihren Anbieter gesendet wird. Fiddler steht unter [Fiddler Web Debugging Proxy zum Download zur Verfügung.](https://www.fiddler2.com/fiddler2/version.asp)
  
## <a name="see-also"></a>Siehe auch

- [Schnelle Schritte zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

