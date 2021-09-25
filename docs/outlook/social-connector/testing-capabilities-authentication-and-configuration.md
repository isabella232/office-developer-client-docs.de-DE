---
title: Testen der Funktionen, Authentifizierung und Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: In diesem Thema werden Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk beschrieben.
ms.openlocfilehash: 165ef53f2fc9a990f4f2ffc1acfcb61b51747bac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578340"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testen der Funktionen, Authentifizierung und Konfiguration

In diesem Thema werden Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk beschrieben.
  
## <a name="getting-capabilities"></a>Abrufen von Funktionen

Ein anbieter für Outlook Connector für soziale Netzwerke (OSC) implementiert [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md)und der OSC ruft **GetCapabilities auf,** um die vom Anbieter unterstützte Funktionalität abzurufen. Die Funktionen, die Ihr Anbieter für Ihr soziales Netzwerk unterstützt, sollten am Zeitpunkt der Implementierung bekannt sein und sollten nicht von einem Anruf an das soziale Netzwerk in Echtzeit abhängen. Beispielsweise können Outlook Benutzer Outlook offline starten, und **GetCapabilities** kann sich zum Zeitpunkt des Starts Outlook nicht auf die Netzwerkkonnektivität verlassen. 
  
Beim Testen des Anbieters sollten Sie überprüfen, ob der von **GetCapabilities** zurückgegebene _Ergebniszeichenfolgenparameter_ dem **Funktionselement** gemäß definition durch das OSC-Anbieter-XML-Schema entspricht. Weitere Informationen finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Konfigurieren eines Kontos

Wenn der OSC ein Konto konfiguriert, sollten Sie überprüfen, ob das Symbol und der Name des sozialen Netzwerks angezeigt werden und ob die Hyperlinks "Konto erstellen" und "Kennwort vergessen" im Dialogfeld "Kontokonfiguration" angezeigt werden, wie vom Anbieter angegeben.
  
### <a name="social-network-icon-and-name"></a>Symbol und Name des sozialen Netzwerks

Nach dem Abrufen von Funktionen kann der OSC fortfahren, um das Symbol und den Namen für das soziale Netzwerk abzurufen, indem [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) und [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)aufgerufen wird. Führen Sie die folgenden Tests aus, um sicherzustellen, dass diese Methodenaufrufe erfolgreich sind.
  
|**Zu testendes Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Symbol für soziale Netzwerke  <br/> | Das Symbol für das soziale Netzwerk wird an den folgenden Stellen im OSC korrekt angezeigt:  <br/>  Im Dialogfeld OSC für **Konten in sozialen Netzwerken**.  <br/>  In the drop-down menu when you attempt to add a person as a friend.  <br/>  Im Signal, wenn sie einem Freund folgen.  <br/> <br/>**HINWEIS:** Sie können auf das Dialogfeld für **Konten in sozialen Netzwerken** zugreifen, indem Sie in Outlook auf die Registerkarte Ansicht, in der Gruppe **"Personenbereich",** auf **"Personenbereich"** und dann auf **"Konto Einstellungen"** klicken.            |
|Name des sozialen Netzwerks  <br/> | Der Name des sozialen Netzwerks wird an den folgenden Stellen im OSC korrekt angezeigt:  <br/>  Im Dialogfeld OSC für **Konten in sozialen Netzwerken**.  <br/>  In the drop-down menu when you attempt to add a person as a friend.  <br/>  Als Titel des Kennwortdialogfelds, wenn Sie versuchen, das vorhandene Kennwort zu ändern.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Anzeigen von Hyperlinks im Konfigurationsdialogfeld

Nach dem Aufrufen von **ISocialProvider::GetCapabilities** verwendet osc den Wert des **hideHyperlinks-Elements** im  _Ergebnisparameter,_ um zu bestimmen, ob das Klicken hier ausgeblendet oder angezeigt werden **soll, um ein Konto zu erstellen** und Ihr Kennwort zu **vergessen?** Hyperlinks im Dialogfeld kontokonfiguration. Stellen Sie sicher, dass die Kontokonfiguration diese URLs anzeigt, wenn **hideHyperlinks** **auf "false"** festgelegt ist.
  
### <a name="support-to-create-account"></a>Unterstützung zum Erstellen eines Kontos

Stellen Sie sicher, dass beim Festlegen des  _Ergebnisparameters_ aus dem **ISocialProvider::GetCapabilities-Methodenaufruf** das **hideHyperlinks-Element** auf **"false"** und das **CreateAccountUrl-Element** auf **"true"** festgelegt ist, durch Klicken auf die URL die Seite im Standardwebbrowser geöffnet wird.
  
### <a name="support-for-forgotten-password"></a>Unterstützung für vergessenes Kennwort

Stellen Sie sicher, dass beim Festlegen des  _Ergebnisparameters_ aus dem **ISocialProvider::GetCapabilities-Methodenaufruf** das **HideHyperlinks-Element** auf **"false"** und das **"forgotPasswordUrl"-Element** auf **"true"** festgelegt ist, durch Klicken auf die URL die Seite im Standardwebbrowser geöffnet wird.
  
## <a name="authenticating-users"></a>Authentifizierung von Benutzern

Testen Sie die folgenden Szenarien, unabhängig davon, ob Ihr OSC-Anbieter die Standardauthentifizierung oder die formularbasierte Authentifizierung unterstützt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Zum ersten Mal anmelden.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden.  <br/> |
|Anmelden mit einem Kennwort, das aus einer Vielzahl von Zeichen besteht, einschließlich Interpunktionszeichen und Unicode-Zeichen.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden, unabhängig von der Art der im Kennwort verwendeten Zeichen.  <br/> |
|Das Dialogfeld für **Konten in sozialen Netzwerken,** in dem der Benutzername oder die ID angezeigt wird.  <br/> |Nachdem sich der Benutzer erfolgreich beim Netzwerk angemeldet hat, zeigt das Dialogfeld des OSC für Konten in **sozialen Netzwerken** den angemeldeten Benutzernamen oder die ID an.  <br/> |
|Die Authentifizierung schlägt fehl.  <br/> |Der OSC zeigt den Fehler **Ungültiger Benutzername oder Kennwort** an.  <br/> |
|Es kann keine Verbindung mit dem sozialen Netzwerk hergestellt werden.  <br/> |Osc displays the error **Server cannot be found**.  <br/> |
|In der Lage sein, Elemente abzurufen.  <br/> |Nachdem sich der Benutzer authentifiziert hat, sollte alle Aktivitäten zulässig sein. Es gibt keine Fehler beim Abrufen von Daten oder Aktivitäten von Freunden.  <br/> |
|Anmelden beim sozialen Netzwerk nach dem Neustart Outlook.  <br/> |Wenn der OSC-Anbieter das Zwischenspeichern des Kennworts zulässt, wird der Benutzer nach der ersten Authentifizierung nicht mehr zur Eingabe von Anmeldeinformationen aufgefordert, wenn der OSC versucht, Daten aus dem sozialen Netzwerk abzurufen.  <br/> |
   
Wenn Ihr OSC-Anbieter außerdem die formularbasierte Authentifizierung unterstützt, testen Sie auch das folgende Szenario.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Osc getting a URL to a form for the user to log on from calling [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |Der OSC öffnet die URL im Standardbrowser des Benutzers, und die Webseite ermöglicht es dem Benutzer, Anmeldeinformationen für die Anmeldung beim sozialen Netzwerk einzugeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CAPABILITIES-XML-Elemente](capabilities-xml-elements.md)  
- [Basic Authentication](basic-authentication.md) 
- [Formularbasierte Authentifizierung](forms-based-authentication.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

