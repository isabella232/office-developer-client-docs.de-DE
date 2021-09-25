---
title: XML-Elemente für „capabilities“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Die Tabellen in diesem Thema beschreiben untergeordnete Elemente der Funktionen-XML und sind nach den unterstützten Bereichen gruppiert.
ms.openlocfilehash: f7ffd29afdbe1afda0d189a01d7978e2382b7b8e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616243"
---
# <a name="capabilities-xml-elements"></a>XML-Elemente für „capabilities“

Die Tabellen in diesem Thema beschreiben untergeordnete Elemente der **Funktionen-XML** und sind nach den unterstützten Bereichen gruppiert. Der Standardwert jedes **Capabilities-Elements** ist **"false".** Wenn das Element nicht in der von der [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebenen **Capabilities-XML** angegeben ist, ist der Wert des Elements gleich **false**.
  
Eine Übersichtsbeschreibung der **Funktionen-XML** finden Sie unter [XML für Funktionen.](xml-for-capabilities.md) Ein Beispiel für **funktions-XML** finden Sie unter [Capabilities XML Example](capabilities-xml-example.md). Eine vollständige Definition des OSC-Anbieter-XML-Schemas (Microsoft Outlook Connector für soziale Netzwerke), einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook XML-Schema](outlook-social-connector-provider-xml-schema.md)des Connector für soziale Netzwerke.
  
## <a name="capabilities-for-supporting-friends"></a>Funktionen für die Unterstützung von Freunden

In der folgenden Tabelle sind Elemente aufgeführt, die für jede Synchronisierung von Freunden oder Nicht-Freunden gelten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Gibt an, ob der Anbieter den Aufruf der [ISocialSession::UnFollowPerson-Methode](isocialsession-unfollowperson.md) unterstützt.  <br/> **followPerson** und **doNotFollowPerson** sind unabhängige Features eines OSC-Anbieters. Ein OSC-Anbieter kann angeben, ob es möglich ist, eine Person als Freund hinzuzufügen **(followPerson** auf **"true"** festlegen) oder eine Person als Freund in einem Konto in einem sozialen Netzwerk entfernen zu können (doNotFollowPerson auf  **"true"** festlegen). Im Allgemeinen bedeutet die Möglichkeit, folgen zu können, nicht, dass sie nicht mehr folgen kann. **followPerson** ist eine Funktion und sollte nicht als Aktion interpretiert werden, um einer bestimmten Person oder jeder Person im Konto des sozialen Netzwerks zu folgen. **followPerson** being **true** does not implizieren **doNotFollowPerson** is **false**.  <br/> |
|**followPerson** <br/> |Gibt an, ob der Anbieter den Aufruf der [ISocialSession::FollowPerson-Methode](isocialsession-followperson.md) unterstützt. Der OSC überprüft **followPerson,** ob **cacheFriends** **wahr** ist (zwischengespeicherte Synchronisierung von Freunden), **dynamicContactsLookup** **wahr** ist (On-Demand-Synchronisierung von Freunden und Nicht-Freunden), oder beide **Cache-Freunde** und **dynamicContactsLookup** sind wahr (hybride Synchronisierung von Freunden und Nicht-Freunden). Wenn der Anbieter **followPerson** auf **"true"** festlegt, zeigt osc ein Netzwerksignal im Personenbereich für Personen an, denen der Benutzer folgt, und aktiviert den Befehl **"On" \<NetworkName\>** im Menü **"Hinzufügen" (+)** im Personenbereich. Wenn der Anbieter **followPerson** als **"false"** festlegt, wird das Netzwerksignal nicht angezeigt, und der **\<NetworkName\> "On"-Befehl** ist ausgeblendet.  <br/> |
|**getFriends** <br/> |Gibt an, ob der Anbieter den [ISocialPerson::GetFriendsAndColleagues-](isocialperson-getfriendsandcolleagues.md) oder [ISocialSession2::GetPeopleDetails-Methodenaufruf](isocialsession2-getpeopledetails.md) unterstützt. Wenn der Anbieter **getFriends** auf **"true"** festlegt, verwendet osc den Wert von **cacheFriends** oder **dynamicContactsLookup,** um zu bestimmen, ob das soziale Netzwerk das Speichern von Freunden als Outlook Kontaktelementen oder im Speicher zulässt. Wenn der Anbieter **"getFriends"** als **"false"** festlegt, unterstützt das soziale Netzwerk keine Freunde und die Methoden **ISocialPerson::GetFriendsAndColleagues** und **ISocialSession2::GetPeopleDetails,** und der OSC ignoriert die Werte von **cacheFriends** und **dynamicContactsLookup.**  <br/> |
   
Die folgenden Elemente gelten nur für die zwischengespeicherte Synchronisierung von Freunden oder die Hybridsynchronisierung von Freunden und Nicht-Freunden. Weitere Informationen zum Synchronisieren von Freunden finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheFriends** <br/> |Gibt an, ob der OSC-Anbieter das Speichern von Freunden als Outlook Kontaktelemente zulässt. Der OSC überprüft **cacheFriends** nur, wenn **getFriends** **"true"** ist. Wenn der Anbieter **cacheFriends** auf **"true"** festlegt, synchronisiert osc Freunde durch Zwischenspeichern und erstellt einen netzwerkspezifischen Kontaktordner im Standardspeicher des Benutzers für Freundeskontakte. Der Name des netzwerkspezifischen Kontaktordners ist der Wert der [ISocialProvider::SocialNetworkName-Eigenschaft.](isocialprovider-socialnetworkname.md) Wenn der Anbieter **cacheFriends** auf **"false"** festlegt, erstellt osc keinen netzwerkspezifischen Kontaktordner für Freundekontakte, um Freunde zu speichern.  <br/> |
|**contactSyncRestartInterval** <br/> |Bestimmt das Wiederholungsintervall in Minuten zwischen den Versuchen, die Informationen von Freunden aus dem sozialen Netzwerk zu synchronisieren, wenn ein Synchronisierungsfehler auftritt. Das OSC verwendet dieses Element nur, wenn der OSC-Anbieter die zwischengespeicherte Synchronisierung oder hybride Synchronisierung von Freunden mit einem kontaktspezifischen Kontaktordner für soziale Netzwerke unterstützt **(CacheFriends** ist **wahr).**  <br/> Das standardmäßige Wiederholungsintervall beträgt 30 Minuten, es sei denn, der Standardwert wird durch den  `ContactSyncRestartInterval` Schlüssel unter  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` überschrieben. Wenn der Anbieter **contactSyncRestartInterval** festlegt, überschreibt der Anbieterwert das standardmäßige Wiederholungsintervall von 30 Minuten oder den Registrierungsschlüsselwert.  <br/> Weitere Informationen zum Synchronisieren von Informationen zu Freunden und Nicht-Freunden bei Bedarf finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)  <br/> |
   
Die folgenden Elemente gelten nur für die On-Demand-Synchronisierung oder hybride Synchronisierung von Freunden und Nicht-Freunden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Gibt an, ob der OSC-Anbieter den [ISocialSession2::GetPeopleDetails-Aufruf](isocialsession2-getpeopledetails.md) für die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt.  <br/> Der OSC überprüft **dynamicContactsLookup** nur, wenn **getFriends** **"true"** ist. Die Standardeinstellung für **dynamicContactsLookup** ist **"false".**  <br/> Wenn der OSC-Anbieter **dynamicContactsLookup** als **"true"** und **"getFriends"** als **"true"** angibt, ruft der OSC bei jeder Aktualisierung des Personenbereichs **ISocialSession2::GetPeopleDetails** auf. Der Personenbereich wird aktualisiert, wenn der Benutzer einen anderen Benutzer im Personenbereich oder ein anderes Element im Outlook Explorer-Fenster auswählt oder ein Outlook Inspektorfenster öffnet. Die dynamische Kontaktsuche stellt sicher, dass dem Benutzer immer die neuesten Benutzerbilder und Profilinformationen im Personenbereich angezeigt werden, erhöht jedoch die Anzahl der Anrufe vom Anbieter an das soziale Netzwerk.  <br/> Wenn der Anbieter **dynamicContactsLookup** auf **"false"** festlegt, ruft OSC **ISocialSession2::GetPeopleDetails** nicht auf, um den Personenbereich zu aktualisieren.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Gibt an, ob der OSC bei Bedarf eine Synchronisierung für Freunde und Nicht-Freunde ausführen soll, wenn der Personenbereich minimiert wird.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Funktionen zur Unterstützung von Aktivitäten

Das folgende Element gilt für jede Art der Synchronisierung von Aktivitäten, die vom OSC-Anbieter unterstützt werden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**getActivities** <br/> |Gibt an, ob der Anbieter die Aufrufe der [ISocialSession2::GetActivitiesEx-](isocialsession2-getactivitiesex.md) oder [ISocialPerson::GetActivities-Methode](isocialperson-getactivities.md) unterstützt. Wenn der Anbieter **getActivities** auf **"true"** festlegt, verwendet osc den Wert von **"cacheActivities"** oder **"dynamicActivitiesLookupEx",** um zu bestimmen, ob die Website des sozialen Netzwerks das Speichern von Aktivitäten als Outlook RSS-Elemente oder als Speicheraktivitäten zulässt. Wenn der Anbieter **"getActivities"** als **"false"** festlegt, unterstützt das soziale Netzwerk keine Aktivitäten und die Methoden **ISocialSession2::GetActivitiesEx** und **ISocialPerson::GetActivities,** und der OSC ignoriert die Werte von **"cacheActivities"** und **"dynamicActivitiesLookupEx".**  <br/> |
   
Das folgende Element gilt nur für die zwischengespeicherte Synchronisierung oder hybride Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheActivities** <br/> |Ab Outlook Connector für soziale Netzwerke 2013 ignoriert osc dieses Element, da Anbieter Aktivitäten nicht mehr synchronisieren können, indem sie sie in einem ausgeblendeten Ordner im Speicher des Benutzers zwischenspeichern.  <br/> Wenn der Anbieter Aktivitäten unterstützt, muss der Anbieter die Synchronisierung von Aktivitäten bei Bedarf unterstützen. Der Anbieter legt **cacheActivities** auf **"false"** und **"dynamicActivitesLookupEx"** auf **"true"** fest. Der OSC synchronisiert Aktivitäten bei Bedarf und speichert Aktivitäten im Arbeitsspeicher zwischen. Der Speichercache der Aktivitäten wird in einem Intervall von 30 Minuten aktualisiert.  <br/> |
   
Die folgenden Elemente gelten nur für die On-Demand-Synchronisierung oder hybride Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Veraltet in OSC 1.1.  <br/> Ab OSC 1.1 ruft der OSC [ISocialSession::GetActivities](isocialsession-getactivities.md) nicht mehr auf und ignoriert den Wert von **dynamicActivitiesLookup.** Um die Suche nach Bedarfsaktivitäten zu unterstützen, legen Sie **"cacheActivities"** als **"false"** und **"getActivities"** und **"dynamicActivitiesLookupEx"** als **"true"** fest, und der OSC ruft **ISocialSession2::GetActivitiesEx** auf.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Gibt an, ob der OSC-Anbieter den **ISocialSession2::GetActivitiesEx-Aufruf** für die On-Demand-Synchronisierung von Aktivitäten unterstützt.  <br/> Wenn der OSC-Anbieter die Synchronisierung von Aktivitäten bei Bedarf unterstützt, legt er **"getActivities"** und **"dynamicActivitiesLookupEx"** auf **"true"** und **"cacheActivities"** auf **"false"** fest. Der OSC ruft **ISocialSession2::GetActivitiesEx** jedes Mal auf, wenn der Personenbereich aktualisiert wird. Der Personenbereich wird aktualisiert, wenn der Benutzer das ausgewählte Element im Outlook Explorer-Fenster ändert oder ein Outlook Inspektorfenster öffnet. Bei der Suche nach dynamischen Aktivitäten wird sichergestellt, dass dem Benutzer immer die neuesten Aktivitäten im Personenbereich angezeigt werden, aber die Anzahl der Anrufe vom Anbieter an das soziale Netzwerk wird erhöht.  <br/> Wenn der Anbieter **dynamicActivitiesLookupEx** auf **"false"** festlegt, ruft OSC **ISocialSession2::GetActivitiesEx** nicht für Personen auf, die im Personenbereich angezeigt werden.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Gibt an, ob der OSC bei Bedarf eine Synchronisierung für Aktivitäten ausführen soll, wenn der Personenbereich minimiert wird.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Allgemeine Funktionen zur Unterstützung der On-Demand- oder Hybridsynchronisierung von Freunden, Nicht-Freunden und Aktivitäten

|**Element**|**Beschreibung**|
|:-----|:-----|
|**hashFunction** <br/> | Gibt die Hashfunktion an, die vom OSC-Anbieter unterstützt wird. Um personenbezogene Informationen von Benutzern zu schützen, die sich nicht im sozialen Netzwerk oder in der Branchenanwendung des Anbieters befinden, übergibt der OSC Hash-E-Mail-Adressen an **ISocialSession2::GetPeopleDetails** und **ISocialSession2::GetActivitiesEx**.  <br/>  Wenn **dynamicContactsLookup** auf **"true"** oder **"dynamicActivitiesLookupEx"** auf **"true"** festgelegt ist, muss der Anbieter **hashFunction** auf einen der zulässigen Werte festlegen: **SHA1**, **MD5** oder **CRC32MD5**. Wenn **hashFunction** fehlt oder einen falschen Wert angibt, gibt osc einen Fehler zurück.  <br/> **SHA1** ist Internet Engineering Task Force (IETF) US Secure Hash Algorithm 1, definiert durch [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Beispielsweise ist der **SHA1-Hashwert** der E-Mail-Adresse melissa@contoso.com  `bb81577b567262a21a4df5f6e335c1250acd7b50` .  <br/> **MD5** ist Internet Engineering Task Force (IETF) MD5 Message-Digest Algorithmus, der von [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt)definiert wird. Beispielsweise ist der **MD5-Hashwert** der E-Mail-Adresse melissa@contoso.com  `c8c39e61ca1662477b39b83d7b0a0615` .  <br/> **CRC32MD5** ist eine Kombination aus **CRC32** und **MD5,** die wie folgt definiert ist:  <br/>  Normalisieren Sie die E-Mail-Adresse, indem Sie führende und nachfolgende Leerzeichen entfernen und alle Zeichen in Kleinbuchstaben konvertieren.  <br/>  Berechnen Sie den **CRC32-Wert** für die normalisierte E-Mail-Adresse, und verwenden Sie die ganzzahlige Dezimaldarstellung dieses Werts. Wenn Ihre Implementierung vorzeichenlose ganze Zahlen zurückgibt, müssen Sie die vorzeichenlose ganze Zahl in eine ganze Zahl ohne Vorzeichen konvertieren.  <br/>  Berechnen Sie den **MD5-Wert** für die normalisierte E-Mail-Adresse, und verwenden Sie die Hexadezimaldarstellung dieses Werts (unter Verwendung von Kleinbuchstaben für A bis F).  <br/>  Kombinieren Sie diese beiden Werte mit einem Unterstrich.  <br/>  Beispielsweise ist der **CRC32MD5-Hashwert** der E-Mail-Adresse melissa@contoso.com  `2149665315_c8c39e61ca1662477b39b83d7b0a0615` .  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Funktionen zur Unterstützung der Authentifizierung und Kontokonfiguration

|**Element**|**Beschreibung**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Gibt an, ob das soziale Netzwerk es dem Benutzer ermöglicht, Einstellungen für die automatische Konfiguration zu ändern, z. B. eine andere URL für die Anmeldung anzugeben.  <br/> |
|**createAccountUrl** <br/> |Wenn der Anbieter **hideHyperlinks** auf **"false"** festlegt, wird die von **createAccountUrl** angegebene URL im Standardbrowser geöffnet, wenn der Benutzer klickt, um ein Konto im Dialogfeld **"Kontokonfiguration"** **zu erstellen.**  <br/> |
|**displayUrl** <br/> |Gibt an, ob das OSC das **Textfeld "URL-Adresse"** für das soziale Netzwerk im Dialogfeld "Kontokonfiguration" anzeigen soll.  <br/> |
|**forgotPasswordUrl** <br/> |Wenn der Anbieter **hideHyperlinks** auf **"false"** festlegt, wird die von **"forgotPasswordUrl"** angegebene URL im Standardbrowser geöffnet, wenn der Benutzer im Dialogfeld **"Kontokonfiguration"** auf "Kennwort **vergessen"** klickt.  <br/> |
|**hideHyperlinks** <br/> |Gibt an, ob der OSC die Hyperlinks **"Hier klicken"** ausblenden soll, um ein Konto zu erstellen und Ihr Kennwort zu **vergessen?** Hyperlinks im Dialogfeld "Kontokonfiguration".  <br/> OSC 1.0 ignoriert diese Einstellung, und die Hyperlinks werden immer ausgeblendet. OSC 1.1 beobachtet den Wert dieser Einstellung.  <br/> |
|**hideRememberMyPassword** <br/> |Gibt an, ob der OSC das **Kontrollkästchen "Kennwort** merken" im Dialogfeld "Kontokonfiguration" ausblenden soll.  <br/> Wenn der Anbieter **hideRememberMyPassword** auf **"true"** festlegt, fungiert osc so, als ob das **Kontrollkästchen "Mein Kennwort** merken" deaktiviert ist und das Kennwort nicht gespeichert wird.  <br/> Wenn der Anbieter **hideRememberMyPassword** auf **"false"** festlegt, zeigt OSC das **Kontrollkästchen "Mein Kennwort** merken" im Dialogfeld "Kontokonfiguration" an.  <br/> |
|**supportsAutoConfigure** <br/> |Gibt an, ob der OSC die **GetAutoConfiguredSession-Funktion** auf der **ISocialProvider-Schnittstelle** aufrufen soll, um die automatische Konfiguration zu versuchen und sich für den Benutzer beim sozialen Netzwerk anzumelden.  <br/> |
|**useLogonCached** <br/> |Gibt an, ob der OSC-Anbieter den [ISocialSession2::LogonCached-Aufruf](isocialsession2-logoncached.md) zur Anmeldung mit zwischengespeicherten Anmeldeinformationen unterstützt.  <br/> Wenn der Anbieter **"useLogonCached"** als **"true"** festlegt, ignoriert osc die Einstellung für **useLogonWebAuth,** und der OSC ruft **ISocialSession2::LogonCached** zur Authentifizierung auf.  <br/> Wenn der Anbieter **dynamicActivitiesLookupEx** auf **"false"** festlegt, ruft osc **ISocialSession2::LogonCached** nicht zur Authentifizierung auf.  <br/> |
|**useLogonWebAuth** <br/> |Gibt an, ob der OSC die formularbasierte Authentifizierung und die [ISocialSession::LogonWeb-Methode](isocialsession-logonweb.md) verwenden soll. Wenn die Anbietersätze **"logonWebAuth"** als **"false"** verwenden, verwendet OSC die Standardauthentifizierung und ruft die [ISocialSession::Logon-Methode auf.](isocialsession-logon.md) Wenn die Anbietersätze **UseLogonWebAuth** als **"true"** festlegen, verwendet osc die formularbasierte Authentifizierung und ruft **ISocialSession::LogonWeb auf.**  <br/> |
   
Abhängig von den vom Anbieter in der **ISocialProvider::GetCapabilities-Methode zurückgegebenen** **Funktionen** ändert sich das Dialogfeld für die Kontokonfiguration. Abbildung 1 zeigt beispielsweise das Dialogfeld "Kontokonfiguration" für ein TestProvider-Beispiel. 
  
**Abbildung 1. TestProvider-Beispiel im Dialogfeld "Kontokonfiguration"**

![TestProvider-Beispielkonfigurationsinformationen](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)

