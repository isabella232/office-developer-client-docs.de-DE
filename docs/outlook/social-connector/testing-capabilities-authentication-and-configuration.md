---
title: Testen der Funktionen, Authentifizierung und Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: In diesem Thema werden Tests zum Abrufen von Funktionen sowie Szenarien zum Konfigurieren eines Kontos und zur Authentifizierung eines Benutzers für ein soziales Netzwerk beschrieben.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423503"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testen der Funktionen, Authentifizierung und Konfiguration

In diesem Thema werden Tests zum Abrufen von Funktionen sowie Szenarien zum Konfigurieren eines Kontos und zur Authentifizierung eines Benutzers für ein soziales Netzwerk beschrieben.
  
## <a name="getting-capabilities"></a>Abrufen von Funktionen

Ein Outlook Social Connector (OSC)-Anbieter implementiert [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md)und das OSC ruft **GetCapabilities** auf, um die vom Anbieter unterstützte Funktionalität zu erhalten. Die Funktionen, die Ihr Anbieter für Ihr soziales Netzwerk unterstützt, sollten am Zeitpunkt der Implementierung bekannt sein und sollten nicht von einem Aufruf an das soziale Netzwerk in Echtzeit abhängen. Beispielsweise können Outlook Benutzer offline Outlook starten, und **GetCapabilities** kann sich zum Zeitpunkt des Startstarts nicht auf netzwerkkonnektivität Outlook verlassen. 
  
Beim Testen des Anbieters sollten  Sie überprüfen, ob der von **GetCapabilities** zurückgegebene Ergebniszeichenfolgenparameter dem Capabilities-Element entspricht, das durch das XML-Schema des OSC-Anbieters definiert ist.  Weitere Informationen finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Konfigurieren eines Kontos

Wenn die OSC ein Konto konfiguriert, sollten Sie überprüfen, ob das Symbol und der Name des sozialen Netzwerks angezeigt werden und ob die Hyperlinks create-account und forgot-password im Dialogfeld Kontokonfiguration angezeigt werden, wie vom Anbieter angegeben.
  
### <a name="social-network-icon-and-name"></a>Symbol und Name des sozialen Netzwerks

Nach dem Abrufen von Funktionen kann das OSC fortfahren, das Symbol und den Namen für das soziale Netzwerk durch Aufrufen von [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) und [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)zu erhalten. Gehen Sie wie folgt vor, um zu überprüfen, ob diese Methodenaufrufe erfolgreich sind.
  
|**Zu testende Elemente**|**Erwartetes Verhalten**|
|:-----|:-----|
|Symbol für soziale Netzwerke  <br/> | Das Symbol für soziale Netzwerke wird an den folgenden Stellen im OSC ordnungsgemäß angezeigt:  <br/>  Im Dialogfeld OSC für Konten **des sozialen Netzwerks**.  <br/>  Im Dropdownmenü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  Im Signal beim Folgen eines Freundes.  <br/> <br/>**HINWEIS**: Sie können auf  das Dialogfeld für Konten des sozialen Netzwerks zugreifen,  indem Sie in Outlook auf die Registerkarte Ansicht klicken, in der Gruppe Personenbereich auf Personenbereich und dann auf Konto **Einstellungen**.            |
|Name des sozialen Netzwerks  <br/> | Der Name des sozialen Netzwerks wird an den folgenden Stellen im Betriebssystem korrekt angezeigt:  <br/>  Im Dialogfeld OSC für Konten **des sozialen Netzwerks**.  <br/>  Im Dropdownmenü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  Als Titel des Kennwortdialogfelds, wenn Sie versuchen, das vorhandene Kennwort zu ändern.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Anzeigen von Hyperlinks im Konfigurationsdialogfeld

Nach dem Aufruf von **ISocialProvider::GetCapabilities** verwendet das OSC den Wert des **hideHyperlinks-Elements** im _Results-Parameter,_ um zu bestimmen, ob die Hyperlinks Klicken Sie hier zum Erstellen eines Kontos und Vergessen Ihres Kennworts im Dialogfeld Kontokonfiguration ausgeblendet oder angezeigt werden sollen.   Stellen Sie sicher, dass diese URLs in der Kontokonfiguration angezeigt werden, wenn **hideHyperlinks** false ist. 
  
### <a name="support-to-create-account"></a>Unterstützung zum Erstellen eines Kontos

Überprüfen Sie,  ob beim Ergebnisparameter aus dem **ISocialProvider::GetCapabilities-Methodenaufruf** das **hideHyperlinks-Element** auf **false** und das **createAccountUrl-Element** auf **true** festgelegt ist, durch Klicken auf die URL die Seite im Standardwebbrowser geöffnet wird.
  
### <a name="support-for-forgotten-password"></a>Unterstützung für vergessene Kennwörter

Stellen Sie sicher, dass, wenn der  _Results-Parameter_ aus dem **ISocialProvider::GetCapabilities-Methodenaufruf** das **hideHyperlinks-Element** auf **false** und das **forgotPasswordUrl-Element** auf **true** festgelegt ist, durch Klicken auf die URL die Seite im Standardwebbrowser geöffnet wird.
  
## <a name="authenticating-users"></a>Authentifizierung von Benutzern

Testen Sie für die folgenden Szenarien, unabhängig davon, ob Ihr OSC-Anbieter die Standardauthentifizierung oder die formularbasierte Authentifizierung unterstützt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Anmeldung zum ersten Mal.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden.  <br/> |
|Anmelden mit einem Kennwort, das aus einer Vielzahl von Zeichen besteht, einschließlich Interpunktion und Unicode-Zeichen.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden, unabhängig von der Art von Zeichen, die im Kennwort verwendet werden.  <br/> |
|Das Dialogfeld für Konten des sozialen **Netzwerks,** in dem der Benutzername oder die ID angezeigt werden.  <br/> |Nachdem sich der Benutzer erfolgreich am Netzwerk angemeldet hat, zeigt  das Dialogfeld des Betriebssystems für Konten des sozialen Netzwerks den angemeldeten Benutzernamen oder die ID an.  <br/> |
|Fehler bei der Authentifizierung.  <br/> |Das Betriebssystem zeigt den Fehler **Ungültiger Benutzername oder Kennwort an.**  <br/> |
|Es kann keine Verbindung mit dem sozialen Netzwerk hergestellt werden.  <br/> |Das OSC zeigt den Fehler **Server nicht gefunden an.**  <br/> |
|Die Möglichkeit, Elemente abzurufen.  <br/> |Nachdem sich der Benutzer authentifiziert hat, sollten alle Aktivitäten zulässig sein. Es gibt keine Fehler beim Abrufen der Daten oder Aktivitäten von Freunden.  <br/> |
|Anmelden beim sozialen Netzwerk nach dem Neustart Outlook.  <br/> |Wenn der OSC-Anbieter die Zwischenspeicherung des Kennworts zulässt, wird der Benutzer nach der ersten Authentifizierung des Benutzers nicht später zur Eingabe von Anmeldeinformationen aufgefordert, wenn das OSC versucht, Daten aus dem sozialen Netzwerk zu erhalten.  <br/> |
   
Wenn Ihr OSC-Anbieter die formularbasierte Authentifizierung unterstützt, testen Sie außerdem für das folgende Szenario.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Das OSC ruft eine URL zu einem Formular ab, in dem sich der Benutzer beim Aufrufen von [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)anmelden kann.  <br/> |Das OSC öffnet die URL im Standardbrowser des Benutzers, und auf der Webseite können Benutzer Anmeldeinformationen eingeben, um sich beim sozialen Netzwerk zu anmelden.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Funktionen XML-Elemente](capabilities-xml-elements.md)  
- [Basic Authentication](basic-authentication.md) 
- [Formularbasierte Authentifizierung](forms-based-authentication.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

