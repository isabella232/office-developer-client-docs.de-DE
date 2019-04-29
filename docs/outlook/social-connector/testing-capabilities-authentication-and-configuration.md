---
title: Testen der Funktionen, Authentifizierung und Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: In diesem Thema werden Tests zum Aufrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk beschrieben.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423503"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testen der Funktionen, Authentifizierung und Konfiguration

In diesem Thema werden Tests zum Aufrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und zum Authentifizieren eines Benutzers für ein soziales Netzwerk beschrieben.
  
## <a name="getting-capabilities"></a>Aufrufen von Funktionen

Ein OSC-Anbieter (Outlook Social Connector) implementiert [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md), und der osc ruft getCapabilities auf, um die vom Anbieter unterstützten Funktionen abzurufen. **** Die Funktionen, die Ihr Anbieter für Ihr soziales Netzwerk unterstützt, sollten zum Zeitpunkt der Implementierung bekannt sein und sollten nicht in Echtzeit von einem Anruf an das soziale Netzwerk abhängen. Beispielsweise können Outlook-Benutzer Outlook offline starten, und **getCapabilities** kann beim Start von Outlook nicht auf die Netzwerkkonnektivität zurückgreifen. 
  
Beim Testen des Anbieters sollten Sie überprüfen, ob der von getCapabilities **** zurückgegebene _Ergebnis_ Zeichenfolgen-Parameter dem **Capabilities** -Element entspricht, wie vom osc-Anbieter-XML-Schema definiert. Weitere Informationen finden Sie unter [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Konfigurieren eines Kontos

Wenn der OSC ein Konto konfiguriert, sollten Sie überprüfen, ob das Symbol und der Name des sozialen Netzwerks angezeigt werden und dass die Hyperlinks Create-Account und Forgot-Password im Dialogfeld Kontokonfiguration, wie vom Anbieter angegeben, angezeigt werden.
  
### <a name="social-network-icon-and-name"></a>Soziales Netzwerksymbol und Name

Nachdem Sie die Funktionen abgerufen haben, kann OSC fortfahren, das Symbol und den Namen für das soziale Netzwerk abzurufen, indem Sie [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) und [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md)aufrufen. Führen Sie die folgenden Tests aus, um sicherzustellen, dass diese Methodenaufrufe erfolgreich ausgeführt werden.
  
|**Zu testendes Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Symbol für soziale Netzwerke  <br/> | Das Symbol für soziale Netzwerke wird an den folgenden Stellen im OSC korrekt angezeigt:  <br/>  Im Dialogfeld OSC für **Konten für soziale Netzwerke**.  <br/>  Im Dropdownmenü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  In der Plakette, wenn Sie einem Freund folgen.  <br/> <br/>**Hinweis**: Sie können auf das Dialogfeld für **Konten für soziale Netzwerke** zugreifen, indem Sie auf die Registerkarte **Ansicht** in Outlook, in der Gruppe **Personen Bereich** , auf **Personen Bereich**und dann auf **Kontoeinstellungen**klicken.           |
|Name des sozialen Netzwerks  <br/> | Der Name des sozialen Netzwerks wird an den folgenden Stellen im OSC korrekt angezeigt:  <br/>  Im Dialogfeld OSC für **Konten für soziale Netzwerke**.  <br/>  Im Dropdownmenü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  Als Titel des Dialogfelds Kennwort, wenn Sie versuchen, das vorhandene Kennwort zu ändern.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Anzeigen von Hyperlinks im Konfigurationsdialogfeld

Nach dem Aufruf von **ISocialProvider:: getCapabilities**verwendet der osc den Wert des **hideHyperlinks** -Elements im _results_ -Parameter, um zu bestimmen, ob das Feld **Klicken Sie hier, um ein Konto zu erstellen** und **Ihre Kennwort?** Hyperlinks im Dialogfeld Kontokonfiguration. Stellen Sie sicher, dass die Kontokonfiguration diese URLs anzeigt, wenn **hideHyperlinks** auf **false festgelegt**ist.
  
### <a name="support-to-create-account"></a>Unterstützung zum Erstellen eines Kontos

Stellen Sie sicher, dass der Parameter _results_ des **ISocialProvider:: getCapabilities** -Methodenaufrufs das **hideHyperlinks** -Element auf **false** festgelegt ist und das **createAccountUrl** -Element auf **true**festgelegt ist, indem Sie auf die URL Öffnet die Seite im Standardwebbrowser.
  
### <a name="support-for-forgotten-password"></a>Unterstützung für vergessenes Kennwort

Stellen Sie sicher, dass der Parameter _results_ des **ISocialProvider:: getCapabilities** -Methodenaufrufs das **hideHyperlinks** -Element auf **false** festgelegt ist und das **forgotPasswordUrl** -Element auf **true**festgelegt ist, indem Sie auf die URL Öffnet die Seite im Standardwebbrowser.
  
## <a name="authenticating-users"></a>Authentifizierung von Benutzern

Testen Sie die folgenden Szenarien, unabhängig davon, ob Ihr OSC-Anbieter die Standardauthentifizierung oder die formularbasierte Authentifizierung unterstützt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Anmeldung zum ersten Mal.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden.  <br/> |
|Anmelden mit einem Kennwort aus einer Vielzahl von Zeichen, einschließlich Interpunktions-und Unicode-Zeichen.  <br/> |Der Benutzer kann sich erfolgreich beim sozialen Netzwerk anmelden, unabhängig von der Art der im Kennwort verwendeten Zeichen.  <br/> |
|Das Dialogfeld für **Konten für soziale Netzwerke** , in dem der Benutzername oder die ID angezeigt wird.  <br/> |Nachdem der Benutzer sich erfolgreich beim Netzwerk angemeldet hat, zeigt das Dialogfeld des OSC für **soziale Netzwerke** den angemeldeten Benutzernamen oder die ID an.  <br/> |
|Authentifizierung schlägt fehl.  <br/> |OSC zeigt den Fehler unGültiger **Benutzername oder Kennwort**an.  <br/> |
|Es kann keine Verbindung mit dem sozialen Netzwerk hergestellt werden.  <br/> |OSC zeigt an, dass der Fehler **Server nicht gefunden wurde**.  <br/> |
|In der Lage, Elemente abzurufen.  <br/> |Sobald der Benutzer authentifiziert wurde, sollten alle Aktivitäten zugelassen werden. Es gibt keine Fehler beim Einholen von Daten oder Aktivitäten von Freunden.  <br/> |
|Anmelden beim sozialen Netzwerk nach einem Neustart von Outlook.  <br/> |Wenn der OSC-Anbieter das Zwischenspeichern des Kennworts zulässt, wird der Benutzer nach dem ersten Authentifizieren des Benutzers nicht mehr zur Eingabe von Anmeldeinformationen aufgefordert, wenn der OSC versucht, Daten aus dem sozialen Netzwerk abzurufen.  <br/> |
   
Wenn Ihr OSC-Anbieter die formularbasierte Authentifizierung unterstützt, testen Sie darüber hinaus auch das folgende Szenario.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|OSC Ruft eine URL zu einem Formular ab, über das der Benutzer sich beim Aufrufen von [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md)anmelden muss.  <br/> |OSC öffnet die URL im Standardbrowser des Benutzers, und auf der Webseite kann der Benutzeranmeldeinformationen eingeben, um sich beim sozialen Netzwerk anzumelden.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Capabilities-XML-Elemente](capabilities-xml-elements.md)  
- [Basic Authentication](basic-authentication.md) 
- [Formularbasierte Authentifizierung](forms-based-authentication.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

