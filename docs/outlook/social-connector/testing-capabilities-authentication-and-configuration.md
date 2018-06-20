---
title: Testen von Funktionen, Authentifizierung und Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: In diesem Thema werden die Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und Authentifizieren eines Benutzers für ein social Network beschrieben.
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796087"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Testen von Funktionen, Authentifizierung und Konfiguration

In diesem Thema werden die Tests zum Abrufen von Funktionen und Szenarien zum Konfigurieren eines Kontos und Authentifizieren eines Benutzers für ein social Network beschrieben.
  
## <a name="getting-capabilities"></a>Abrufen von Funktionen

Outlook Social Connector (OSC)-Anbieter implementiert [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)und die OSC-Aufrufe **GetCapabilities** an die vom Anbieter unterstützten Funktionalität zu erhalten. Die von Ihrem Anbieter für das soziale Netzwerk unterstützten Funktionen zum Zeitpunkt der Implementierung bekannt sein sollten, und sollte nicht abhängen, einen Anruf an die für soziale Netzwerke in Echtzeit. Beispielsweise Outlook-Benutzer können Outlook offline starten, und kann nicht **GetCapabilities** Netzwerkkonnektivität zur Zeit beim Starten von Outlook abhängig. 
  
Wenn Sie den Anbieter zu testen, sollten Sie sicherstellen, dass durch das OSC-Anbieter-XML-Schema definierten **GetCapabilities** zurückgegebene _Ergebnisse_ Zeichenfolgenparameter **Capabilities** -Element entspricht. Weitere Informationen finden Sie unter [Funktionen XML-Elemente](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Konfigurieren eines Kontos

Wenn die OSC ein Konto konfiguriert werden, sollten Sie überprüfen, ob der Symbol für soziale Netzwerke und der Name angezeigt werden und dass die Create-Konto und Kennwort vergessen gemäß den Anbieter im Dialogfeld Konfiguration Konto angezeigt.
  
### <a name="social-network-icon-and-name"></a>Symbol für soziale Netzwerke und Namen

Nach der erste Funktionen, kann die OSC fortfahren, und das Symbol und den Namen für das soziale Netzwerk durch Aufrufen von [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) und [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)abrufen. Führen Sie die folgenden Tests durch, um sicherzustellen, dass diese Methodenanrufe können getätigt werden.
  
|**Zu überprüfende Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Symbol für soziale Netzwerke  <br/> | Das Symbol für soziale Netzwerke wird in den folgenden Stellen in der OSC ordnungsgemäß angezeigt:  <br/>  Im Dialogfeld OSC für das **Soziale Netzwerkkonten**.  <br/>  In der Dropdown-Menü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  In das Logo beim Freund folgen.  <br/> <br/>**Hinweis**: Sie können das Dialogfeld für das **Soziale Netzwerk-Konten** zugreifen, indem Sie durch Klicken auf die Registerkarte **Ansicht** in Outlook, in der Gruppe **Personenbereich** , auf **Personenbereich**, und klicken Sie dann auf **Kontoeinstellungen**.           |
|Name für soziale Netzwerke  <br/> | Der Name für soziale Netzwerke wird ordnungsgemäß an den folgenden Stellen in der OSC angezeigt:  <br/>  Im Dialogfeld OSC für das **Soziale Netzwerkkonten**.  <br/>  In der Dropdown-Menü, wenn Sie versuchen, eine Person als Freund hinzuzufügen.  <br/>  Als Titel des Dialogfelds Kennwort, wenn Sie versuchen, das bestehende Kennwort zu ändern.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Anzeige von Hyperlinks im Konfigurationsdialogfeld

Nach dem Aufruf von **ISocialProvider::GetCapabilities**, verwendet das osc bilden den Wert des **HideHyperlinks** -Elements in der _Results_ -Parameter um zu ermitteln, ob die **Klicken Sie hier, um ein Konto erstellen** und **vergessen anzeigen oder Ausblenden der Kennwort?** Links in im Dialogfeld Konfiguration Konto. Stellen Sie sicher, dass wenn **HideHyperlinks** auf **false festgelegt**ist, wird die Kontokonfiguration dieser URLs angezeigt.
  
### <a name="support-to-create-account"></a>Unterstützung für das Konto erstellen

Überprüfen Sie, ob der Parameter _Ergebnisse_ vom Methodenaufruf **ISocialProvider::GetCapabilities** hat das **HideHyperlinks** -Element auf **"false"** festgelegt und das **CreateAccountUrl** -Element auf **"true"**, klicken auf die URL festgelegt Öffnet die Seite im Standardwebbrowser.
  
### <a name="support-for-forgotten-password"></a>Unterstützung für Kennwort vergessen?

Überprüfen Sie, ob der Parameter _Ergebnisse_ vom Methodenaufruf **ISocialProvider::GetCapabilities** hat das **HideHyperlinks** -Element auf **"false"** festgelegt und das **ForgotPasswordUrl** -Element auf **"true"**, klicken auf die URL festgelegt Öffnet die Seite im Standardwebbrowser.
  
## <a name="authenticating-users"></a>Authentifizierung von Benutzern

Testen Sie die folgenden Szenarien unabhängig davon, ob Ihre OSC-Anbieter Standardauthentifizierung oder formularbasierte Authentifizierung unterstützt.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Zum ersten Mal anmelden.  <br/> |Der Benutzer kann sich erfolgreich in sozialen Netzwerken anmelden.  <br/> |
|Erstellen Sie eine Anmeldung mit einem Kennwort eine Vielzahl von Zeichen, Interpunktionszeichen und Unicode-Zeichen bestehen.  <br/> |Der Benutzer kann sich erfolgreich mit dem sozialen Netzwerk, unabhängig von der Art der Zeichen in den Feldern Kennwort anmelden.  <br/> |
|Das Dialogfeld für Anzeige der Benutzername oder das ID- **Konten für soziale Netzwerke**  <br/> |Nachdem der Benutzer erfolgreich mit dem Netzwerk angemeldet hat, zeigt die OSC-Dialogfeld für **Konten für soziale Netzwerke** , der angemeldete Benutzername oder die ID  <br/> |
|Authentifizierung ein Fehler auftritt.  <br/> |Die OSC wird der Fehler **Ungültiger Benutzername oder das Kennwort**angezeigt.  <br/> |
|Mit dem sozialen Netzwerk kann keine Verbindung hergestellt werden.  <br/> |Die OSC wird der Fehler **Server kann nicht gefunden werden**angezeigt.  <br/> |
|Die Fähigkeit zum Abrufen von Elementen.  <br/> |Nachdem der Benutzer authentifiziert wurde, sollte alle Aktivitäten zugelassen werden. Es gibt keine Fehler Abrufen von Daten oder Aktivitäten Freunde.  <br/> |
|Anmelden bei dem sozialen Netzwerk nach Outlook neu zu starten.  <br/> |Wenn der OSC-Anbieter ermöglicht das Zwischenspeichern des Kennworts, nachdem der Benutzer beim ersten authentifiziert wurde, wird der Benutzer nicht später für Anmeldeinformationen aufgefordert immer die OSC versucht, Daten aus dem sozialen Netzwerk erhalten.  <br/> |
   
Darüber hinaus Wenn Ihre OSC-Anbieter formularbasierte Authentifizierung unterstützt, test für die folgenden Szenario.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Die OSC erste eine URL zu einem Formular für den Benutzer aus dem Aufruf von [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)anmelden.  <br/> |Die OSC öffnet die URL im Standardbrowser des Benutzers ein, und die Webseite ermöglicht es dem Benutzer zur Eingabe der Anmeldeinformationen zur Anmeldung bei dem sozialen Netzwerk.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Funktionen XML-Elemente](capabilities-xml-elements.md)  
- [Standardauthentifizierung](basic-authentication.md) 
- [Formularbasierte Authentifizierung](forms-based-authentication.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

