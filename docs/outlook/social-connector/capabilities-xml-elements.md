---
title: XML-Elemente für „capabilities“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: In den Tabellen in diesem Thema werden untergeordnete Elemente der Xml-Funktionen beschrieben und nach den von ihnen unterstützten Bereichen gruppieren.
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281192"
---
# <a name="capabilities-xml-elements"></a>XML-Elemente für „capabilities“

In den Tabellen in diesem  Thema werden untergeordnete Elemente der Xml-Funktionen beschrieben und nach den von ihnen unterstützten Bereichen gruppieren. Der Standardwert jedes **Capabilities-Elements** ist **false.** Wenn das Element nicht  in der von der [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) zurückgegebenen Funktionen-XML angegeben ist, ist der Wert des Elements gleich **false**.
  
Eine Übersicht über die Funktionen **von** XML finden Sie unter [XML for Capabilities](xml-for-capabilities.md). Ein Beispiel für **xml-Funktionen** finden Sie unter [Capabilities XML Example](capabilities-xml-example.md). Eine vollständige Definition des MICROSOFT Outlook Social Connector (OSC)-Anbieter-XML-Schemas, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Funktionen zur Unterstützung von Freunden

In der folgenden Tabelle sind Elemente aufgeführt, die für jede Form der Synchronisierung von Freunden oder Nicht-Freunden gelten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Gibt an, ob der Anbieter den [ISocialSession::UnFollowPerson-Methodenaufruf](isocialsession-unfollowperson.md) unterstützt.  <br/> **followPerson** und **doNotFollowPerson** sind unabhängige Features eines OSC-Anbieters. Ein OSC-Anbieter kann angeben, dass eine Person als Freund hinzugefügt werden kann (festlegen von **followPerson** auf **true**) oder in der Lage ist, eine Person als Freund in einem Konto des sozialen Netzwerks zu entfernen (festlegen **von doNotFollowPerson** auf **true**). Im Allgemeinen bedeutet die Möglichkeit, folgen zu können, nicht, dass sie nicht mehr folgen kann. **followPerson** ist eine Funktion und darf nicht als Aktion interpretiert werden, um einer bestimmten Person oder jeder Person im Konto des sozialen Netzwerks zu folgen. **followPerson** ist **true** bedeutet nicht, dass **doNotFollowPerson** false **ist.**  <br/> |
|**followPerson** <br/> |Gibt an, ob der Anbieter den [ISocialSession::FollowPerson-Methodenaufruf](isocialsession-followperson.md) unterstützt. Das OSC überprüft **followPerson,** wenn **cacheFriends** true **ist** (zwischengespeicherte Synchronisierung von Freunden), **dynamicContactsLookup** ist **true** (on-demand synchronization of friends and non-friends), oder **cacheFriends** und **dynamicContactsLookup** sind true (Hybridsynchronisierung von Freunden und Nicht-Freunden). Wenn der Anbieter **followPerson** als **true** festgelegt hat, zeigt das OSC im Personenbereich ein Netzwerkzeichen für Personen an, die der Benutzer folgt, und aktiviert den Befehl **on \< NetworkName \>** im Menü Hinzufügen **(+)** im Personenbereich. Wenn der Anbieter **followPerson** als **false** festgelegt hat, wird das Netzwerkabzeichen nicht angezeigt, und der **Befehl on \< NetworkName \>** ist ausgeblendet.  <br/> |
|**getFriends** <br/> |Gibt an, ob der Anbieter den [ISocialPerson::GetFriendsAndColleagues-](isocialperson-getfriendsandcolleagues.md) oder [ISocialSession2::GetPeopleDetails-Methodenaufruf](isocialsession2-getpeopledetails.md) unterstützt. Wenn vom Anbieter **getFriends** als **true** festgelegt wird, verwendet das OSC den Wert **von cacheFriends** oder **dynamicContactsLookup,** um zu bestimmen, ob das soziale Netzwerk das Speichern von Freunden als Outlook-Kontaktelemente oder im Arbeitsspeicher zulässt. Wenn der Anbieter **getFriends** als **false** legt, unterstützt das soziale Netzwerk keine Freunde und die **Methoden ISocialPerson::GetFriendsAndColleagues** und **ISocialSession2::GetPeopleDetails,** und das OSC ignoriert die Werte von **cacheFriends** und **dynamicContactsLookup**.  <br/> |
   
Die folgenden Elemente gelten nur für die zwischengespeicherte Synchronisierung von Freunden oder die Hybridsynchronisierung von Freunden und Nicht-Freunden. Weitere Informationen zum Synchronisieren von Freunden finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheFriends** <br/> |Gibt an, ob der OSC-Anbieter das Speichern von Freunden als Outlook-Kontaktelemente zulässt. Das OSC überprüft **cacheFriends** nur, wenn **getFriends** true **ist.** Wenn vom Anbieter **cacheFriends** als **true** festgelegt wird, synchronisiert das OSC Freunde durch Zwischenspeichern und erstellt einen netzwerkspezifischen Kontaktordner im Standardspeicher des Benutzers für Freundeskontakte. Der Name des netzwerkspezifischen Kontaktordners ist der Wert der [ISocialProvider::SocialNetworkName-Eigenschaft.](isocialprovider-socialnetworkname.md) Wenn vom Anbieter **cacheFriends** als **false** gesetzt wird, erstellt das OSC keinen netzwerkspezifischen Kontaktordner für Freundeskontakte zum Speichern von Freunden.  <br/> |
|**contactSyncRestartInterval** <br/> |Bestimmt das Wiederholungsintervall (in Minuten) zwischen versuchen, die Informationen von Freunden aus dem sozialen Netzwerk zu synchronisieren, wenn ein Synchronisierungsfehler auftritt. Das OSC verwendet dieses Element nur, wenn der OSC-Anbieter die zwischengespeicherte Synchronisierung oder Hybridsynchronisierung von Freunden mit einem ordnerspezifischen Kontaktordner für soziale Netzwerke unterstützt (**cacheFriends** ist **true**).  <br/> Das Standardintervall für wiederholungsversuche beträgt 30 Minuten, es sei denn, der Standardwert wird durch den  `ContactSyncRestartInterval` Schlüssel unter  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` überschrieben. Wenn der Anbieter **contactSyncRestartInterval festgelegt** hat, überschreibt der Anbieterwert das Standardmäßige Wiederholungsintervall von 30 Minuten oder den Registrierungsschlüsselwert.  <br/> Weitere Informationen zum Synchronisieren von Informationen zu Freunden und Nicht-Freunden bei Bedarf finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).  <br/> |
   
Die folgenden Elemente gelten nur für die On-Demand-Synchronisierung oder hybride Synchronisierung von Freunden und Nicht-Freunden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Gibt an, ob der #A0 den [Aufruf von ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) für die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt.  <br/> Das OSC überprüft **dynamicContactsLookup nur,** wenn **getFriends** true **ist.** Die Standardeinstellung für **dynamicContactsLookup** ist **false.**  <br/> Wenn der #A0 **dynamicContactsLookup** als **true** und **getFriends** als **true** angibt, ruft das OSC **ISocialSession2::GetPeopleDetails** jedes Mal auf, wenn der Personenbereich aktualisiert wird. Der Personenbereich wird aktualisiert, wenn der Benutzer einen anderen Benutzer im Personenbereich oder ein anderes Element im Outlook-Explorer-Fenster auswählt oder ein Outlook-Inspektorfenster öffnet. Die dynamische Kontakte-Suche stellt sicher, dass dem Benutzer immer die neuesten Benutzerbilder und Profilinformationen im Personenbereich angezeigt werden, aber die Anzahl der Anrufe vom Anbieter an das soziale Netzwerk erhöht wird.  <br/> Wenn vom Anbieter **dynamicContactsLookup** als **false** gesetzt wird, wird vom OSC **nicht ISocialSession2::GetPeopleDetails zum** Aktualisieren des Personenbereichs aufruft.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Gibt an, ob das OSC die On-Demand-Synchronisierung für Freunde und Nicht-Freunde durchführen soll, wenn der Personenbereich minimiert wird.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Funktionen zur Unterstützung von Aktivitäten

Das folgende Element gilt für jede Form der Synchronisierung von Aktivitäten, die vom OSC-Anbieter unterstützt werden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**getActivities** <br/> |Gibt an, ob der Anbieter die [ISocialSession2::GetActivitiesEx-](isocialsession2-getactivitiesex.md) oder [ISocialPerson::GetActivities-Methodenaufrufe](isocialperson-getactivities.md) unterstützt. Wenn vom Anbieter **getActivities** als **true** festgelegt wird, verwendet das OSC den Wert **cacheActivities** oder **dynamicActivitiesLookupEx,** um zu bestimmen, ob die Website des sozialen Netzwerks das Speichern von Aktivitäten als Outlook-RSS-Elemente oder als In-Memory-Aktivitäten zulässt. Wenn der Anbieter **getActivities** als **false** legt, unterstützt das soziale Netzwerk keine Aktivitäten und die **Methoden ISocialSession2::GetActivitiesEx** und **ISocialPerson::GetActivities,** und die OSC ignoriert die Werte **cacheActivities** und **dynamicActivitiesLookupEx**.  <br/> |
   
Das folgende Element gilt nur für die zwischengespeicherte Synchronisierung oder hybride Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheActivities** <br/> |Ab Outlook Social Connector 2013 ignoriert die OSC dieses Element, da Anbieter Aktivitäten nicht mehr synchronisieren können, indem sie sie in einem ausgeblendeten Ordner im Speicher des Benutzers zwischenspeichern.  <br/> Wenn der Anbieter Aktivitäten unterstützt, muss der Anbieter die Synchronisierung von Aktivitäten bei Bedarf unterstützen. Der Anbieter legt **cacheActivities** als **false** fest und **dynamicActivitesLookupEx als** **true**. Das OSC synchronisiert Aktivitäten bei Bedarf und speichert Aktivitäten im Arbeitsspeicher zwischen. Der Speichercache für Aktivitäten wird in einem Intervall von 30 Minuten aktualisiert.  <br/> |
   
Die folgenden Elemente gelten nur für die On-Demand-Synchronisierung oder hybride Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Veraltet in OSC 1.1.  <br/> Ab OSC 1.1 ruft das OSC nicht mehr [ISocialSession::GetActivities](isocialsession-getactivities.md) auf und ignoriert den Wert **von dynamicActivitiesLookup**. Um die Suche nach On-Demand-Aktivitäten zu unterstützen, legen Sie **cacheActivities** als **false** und **getActivities** und **dynamicActivitiesLookupEx** als **true** fest, und das OSC wird **ISocialSession2::GetActivitiesEx aufrufen.**  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Gibt an, ob der OSC-Anbieter den **ISocialSession2::GetActivitiesEx-Aufruf** für die On-Demand-Synchronisierung von Aktivitäten unterstützt.  <br/> Wenn der OSC-Anbieter die Synchronisierung von On-Demand-Aktivitäten unterstützt, werden **getActivities** und **dynamicActivitiesLookupEx** als **true** und **cacheActivities** als **false gesetzt.** Das OSC ruft **ISocialSession2::GetActivitiesEx** jedes Mal auf, wenn der Personenbereich aktualisiert wird. Der Personenbereich wird aktualisiert, wenn der Benutzer das ausgewählte Element im Outlook-Explorer-Fenster ändert oder ein Outlook-Inspektorfenster öffnet. Die Suche nach dynamischen Aktivitäten stellt sicher, dass dem Benutzer immer die neuesten Aktivitäten im Bereich Personen angezeigt werden, aber die Anzahl der Anrufe vom Anbieter an das soziale Netzwerk erhöht wird.  <br/> Wenn vom Anbieter **dynamicActivitiesLookupEx** als **false** gesetzt wird, wird **ISocialSession2::GetActivitiesEx** für Personen, die im Personenbereich angezeigt werden, vom OSC nicht aufruft.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Gibt an, ob das OSC die On-Demand-Synchronisierung für Aktivitäten durchführen soll, wenn der Personenbereich minimiert wird.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Allgemeine Funktionen zur Unterstützung der bedarfs- oder hybriden Synchronisierung von Freunden, Nicht-Freunden und Aktivitäten

|**Element**|**Beschreibung**|
|:-----|:-----|
|**hashFunction** <br/> | Gibt die Hashfunktion an, die vom #A0 unterstützt wird. Zum Schutz personenbezogener Informationen von Benutzern, die sich nicht im sozialen Netzwerk oder in der #A0 des Anbieters befinden, übergibt das OSC E-Mail-Adressen mit Hash an **ISocialSession2::GetPeopleDetails** und **ISocialSession2::GetActivitiesEx**.  <br/>  Wenn **dynamicContactsLookup** auf **true** oder **dynamicActivitiesLookupEx** auf **true** festgelegt ist, muss der Anbieter **hashFunction** auf einen der zulässigen Werte festlegen: **SHA1**, **MD5** oder **CRC32MD5**. Wenn **hashFunction** fehlt oder einen falschen Wert angibt, gibt das OSC einen Fehler zurück.  <br/> **SHA1** ist Internet Engineering Task Force (IETF) US Secure Hash Algorithm 1, definiert durch [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Beispielsweise ist der **SHA1-Hashwert** der E-Mail-Adresse melissa@contoso.com  `bb81577b567262a21a4df5f6e335c1250acd7b50` .  <br/> **MD5** ist Internet Engineering Task Force (IETF) MD5 Message-Digest Algorithmus definiert [durch [RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Beispielsweise ist der **MD5-Hashwert** der E-Mail-Adresse melissa@contoso.com  `c8c39e61ca1662477b39b83d7b0a0615` .  <br/> **CRC32MD5** ist eine Kombination aus **CRC32** und **MD5, die** wie folgt definiert sind:  <br/>  Normalisieren Sie die E-Mail-Adresse, indem Sie führende und nachgestellte Leerzeichen entfernen und alle Zeichen in Kleinbuchstaben konvertieren.  <br/>  Berechnen Sie **den CRC32-Wert** für die normalisierte E-Mail-Adresse, und verwenden Sie die dezimale ganzzahlige Darstellung dieses Werts. Wenn Ihre Implementierung signierte ganze Zahlen zurückgibt, müssen Sie die signierte ganze Zahl in eine ganze Zahl ohne Vorzeichen konvertieren.  <br/>  Berechnen Sie **den MD5-Wert** für die normalisierte E-Mail-Adresse, und verwenden Sie die Hexdarstellung dieses Werts (in Kleinbuchstaben für A bis F).  <br/>  Kombinieren Sie diese beiden Werte mit einem Unterstrich.  <br/>  Beispielsweise ist der **CRC32MD5-Hashwert** der E-Mail-Melissa@contoso.com  `2149665315_c8c39e61ca1662477b39b83d7b0a0615` .  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Funktionen zur Unterstützung der Authentifizierung und Kontokonfiguration

|**Element**|**Beschreibung**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Gibt an, ob das soziale Netzwerk es dem Benutzer ermöglicht, einstellungen für die automatische Konfiguration zu ändern, z. B. eine andere URL für die Anmeldung anzugeben.  <br/> |
|**createAccountUrl** <br/> |Wenn der Anbieter **hideHyperlinks** als **false** festgelegt  hat, wird die  von **createAccountUrl** angegebene URL im Standardbrowser geöffnet, wenn der Benutzer auf Klicken Sie hier klicken, um ein Konto im Dialogfeld Kontokonfiguration zu erstellen.  <br/> |
|**displayUrl** <br/> |Gibt an, ob das Betriebssystem das **Textfeld URL-Adresse** für das soziale Netzwerk im Dialogfeld Kontokonfiguration anzeigen soll.  <br/> |
|**forgotPasswordUrl** <br/> |Wenn vom Anbieter **hideHyperlinks** als **false** festgelegt wird, wenn der  Benutzer im Dialogfeld Kontokonfiguration auf Kennwort vergessen **klickt,** wird die von **forgotPasswordUrl** angegebene URL im Standardbrowser geöffnet.  <br/> |
|**hideHyperlinks** <br/> |Gibt an, ob das OSC die Hyperlinks Klicken Sie **hier** zum Erstellen eines Kontos und **Kennwort vergessen?** im Dialogfeld Kontokonfiguration ausblenden soll.  <br/> OSC 1.0 ignoriert diese Einstellung, und die Hyperlinks werden immer ausgeblendet. OSC 1.1 beobachtet den Wert dieser Einstellung.  <br/> |
|**hideRememberMyPassword** <br/> |Gibt an, ob das  Kontrollkästchen Mein Kennwort merken im Dialogfeld Kontokonfiguration ausgeblendet werden soll.  <br/> Wenn der Anbieter **hideRememberMyPassword** als **true** festlegen, wird  das Betriebssystem so tun, als ob das Feld Mein Kennwort merken deaktiviert ist und das Kennwort nicht gespeichert wird.  <br/> Wenn der Anbieter **hideRememberMyPassword** als **false** festgelegt  hat, wird im Dialogfeld Kontokonfiguration das Kontrollkästchen Kennwort merken angezeigt.  <br/> |
|**supportsAutoConfigure** <br/> |Gibt an, ob das OSC die **GetAutoConfiguredSession-Funktion** auf der **ISocialProvider-Schnittstelle** aufrufen soll, um die automatische Konfiguration zu versuchen und sich beim sozialen Netzwerk für den Benutzer zu anmelden.  <br/> |
|**useLogonCached** <br/> |Gibt an, ob der OSC-Anbieter den [ISocialSession2::LogonCached-Aufruf](isocialsession2-logoncached.md) zum Anmelden mit zwischengespeicherten Anmeldeinformationen unterstützt.  <br/> Wenn der Anbieter **useLogonCached** als **true** festlegen, ignoriert das OSC die Einstellung für **useLogonWebAuth,** und das OSC ruft **ISocialSession2::LogonCached** zur Authentifizierung auf.  <br/> Wenn vom Anbieter **dynamicActivitiesLookupEx** als **false** gesetzt wird, wird **ISocialSession2::LogonCached** vom OSC nicht zur Authentifizierung aufruft.  <br/> |
|**useLogonWebAuth** <br/> |Gibt an, ob das OSC die formularbasierte Authentifizierung und die [ISocialSession::LogonWeb-Methode verwenden](isocialsession-logonweb.md) soll. Wenn der Anbieter **useLogonWebAuth** als **false** fest legt, verwendet das OSC die Standardauthentifizierung und ruft die [ISocialSession::Logon-Methode](isocialsession-logon.md) auf. Wenn der Anbieter **useLogonWebAuth** als **true** fest legt, verwendet das OSC die formularbasierte Authentifizierung und ruft **ISocialSession::LogonWeb auf.**  <br/> |
   
Je nach den **Funktionen,** die der Anbieter in der **ISocialProvider::GetCapabilities-Methode** zurückgegeben hat, ändert sich das Dialogfeld Kontokonfiguration. Beispiel: Abbildung 1 zeigt das Dialogfeld Kontokonfiguration für ein TestProvider-Beispiel. 
  
**Abbildung 1. TestProvider-Beispiel im Dialogfeld Kontokonfiguration**

![TestProvider-Beispielkonfigurationsinformationen](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)

