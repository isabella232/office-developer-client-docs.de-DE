---
title: Debuggen eines Providers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Es gibt verschiedene Möglichkeiten zum Debuggen eines anbieters für den Outlook Connector für soziale Netzwerke (SOCIAL Connector, OSC):'
ms.openlocfilehash: 60856866359521923c225a41a5399b8e20093b1a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608921"
---
# <a name="debugging-a-provider"></a>Debuggen eines Providers

Es gibt verschiedene Möglichkeiten zum Debuggen eines anbieters für den Outlook Connector für soziale Netzwerke (SOCIAL Connector, OSC): 
  
- Mithilfe von Debugbefehlen in der Menübandkomponente der Office Fluent Benutzeroberfläche in Outlook oder der unterstützenden Office Clientanwendung bewirkt, dass osc verschiedene Aktionen ausführt.
    
- Mithilfe von Fiddler zum Nachverfolgen von API-Aufrufen und XML, die zwischen einem sozialen Netzwerk und dessen OSC-Anbieter gesendet werden
    
## <a name="debug-buttons"></a>Debugschaltflächen

Die OSC-Anbietererweiterung bietet die Möglichkeit zum Debuggen eines OSC-Anbieters. Um einen Anbieter zu debuggen, erstellen Sie `DebugProviders` einen Wert vom Typ DWORD in der Windows Registrierung unter dem Schlüssel `SocialConnector` (wie in der folgenden Zeile dargestellt), und legen Sie den `DebugProviders` Wert auf 1 fest. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
Standardmäßig ist das Anbieterdebugging deaktiviert. Wenn der  `DebugProviders` Wert nicht vorhanden oder vorhanden ist und auf den Wert 0 festgelegt ist, wird das Anbieterdebugging deaktiviert. 
  
Wenn das Anbieterdebugging aktiviert ist, zeigt OSC beim Auftreten eines Fehlers ein Warnungsdialogfeld mit ausführlichen Fehlerinformationen an und überprüft alle OSC-Anbieter-XML-Daten anhand des OSC-Anbieter-XML-Schemas. Basierend auf dem für eine XML-Zeichenfolge angegebenen Namespace wird ein osc-Anbieter, der mit OSC 1.0 entwickelt wurde, anhand der OSC 1.0-Schemadatei OutlookSocialProvider.xsd überprüft. Ein OSC-Anbieter, der mit OSC 1.1 oder höher entwickelt wurde, wird anhand der Schemadatei OutlookSocialProvider_1.1.xsd überprüft. Wenn Sie den  `DebugProviders` Wert verwenden, wird die Debugwarnung für alle geladenen Anbieter anstelle eines bestimmten Anbieters angezeigt. 
  
Um Debugschaltflächen anzuzeigen, die Ihnen beim Debuggen eines Anbieters helfen können, erstellen Sie `ShowDebugButtons` einen Wert vom Typ DWORD in der Windows Registrierung unter dem `SocialConnector` Schlüssel, und legen Sie den Wert auf `ShowDebugButtons` 1 fest. Um die Schaltflächen der Debugbefehlsleiste auszublenden, legen Sie den  `ShowDebugButtons` Wert auf 0 fest. 
  
Für Outlook 2010 und Clientanwendungen seit Office 2013 werden die Debugschaltflächen auf der Registerkarte **"Add-Ins" des Explorer-Menübands** angezeigt. For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window. 
  
In der folgenden Tabelle werden die Debugschaltflächen beschrieben.
  
|**Schaltfläche "Debuggen"**|**Funktion**|
|:-----|:-----|
|Kontakte synchronisieren  <br/> |Bewirkt, dass der OSC den OSC-Anbieter nur nach zwischengespeicherten Kontakten fragt.  <br/> |
|GAL-Synchronisierung  <br/> |Bewirkt, dass der OSC Daten aus der Exchange globalen Adressliste auf Outlook Kontakte auffüllt.  <br/> |
|Ungültiger Kategoriecache  <br/> |Bewirkt, dass der OSC die Kategorieliste für jeden Speicher neu lädt, wenn der Aktivitätsfeed aktualisiert wird.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler ist ein Über-Kabel-Debugging-Tool zum Überprüfen der API-Aufrufe, die von Ihrem Anbieter an das soziale Netzwerk gesendet werden, und XML, die vom sozialen Netzwerk an Ihren Anbieter gesendet werden. Fiddler steht zum Download unter [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp)zur Verfügung.
  
## <a name="see-also"></a>Siehe auch

- [Schnelle Schritte für Learning zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)  
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)  
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

