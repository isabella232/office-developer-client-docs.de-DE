---
title: XML-Elemente für „capabilities“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: In den Tabellen in diesem Thema wird beschrieben, untergeordnete Elemente über die XML-Funktionen und durch die Bereiche, die sie unterstützen gruppiert.
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795951"
---
# <a name="capabilities-xml-elements"></a>XML-Elemente für „capabilities“

In den Tabellen in diesem Thema wird beschrieben, untergeordnete Elemente des **Funktionen** XML und durch die Bereiche, die sie unterstützen gruppiert. Der Standardwert der einzelnen **Capabilities** -Element ist **false**. Wenn das Element nicht in die **Funktionen** von der [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode zurückgegebenen XML-Daten angegeben wird, ist der Wert des Elements gleich **false**.
  
Eine Übersicht über die Beschreibung über XML- **Funktionen** finden Sie unter [XML-Code für Funktionen](xml-for-capabilities.md). Ein Beispiel für XML- **Funktionen** finden Sie unter [Funktionen XML-Beispiel](capabilities-xml-example.md). Eine vollständige Definition des Microsoft Outlook Social Connector (OSC) Anbieter XML-Schemas, einschließlich, welche Elemente erforderlich oder optional sind finden Sie unter [Outlook Social Connector Provider XML-Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Funktionen zur Unterstützung von Freunden

In der folgenden Tabelle werden die Elemente, die für ein Formular der Synchronisierung von Freunde oder nicht Freunde übernehmen veranschaulicht.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Gibt an, ob der Anbieter Methodenaufruf [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) unterstützt.  <br/> **FollowPerson** und **DoNotFollowPerson** sind unabhängige Features ein OSC-Anbieter. Die Möglichkeit, Anwendungen oder Bildschirme hinzufügen eine Person als Friend (Einstellung **FollowPerson** auf **true**) oder eine Person als Freund auf ein Konto für soziale Netzwerke (Einstellung **DoNotFollowPerson** auf **true**) entfernen können Sie ein OSC-Anbieter angeben. Im Allgemeinen wird, denen Sie folgen können nicht impliziert, Anwendungen oder Bildschirme nach Beenden. **FollowPerson** spielt, und es ist nicht als Aktion zu einer bestimmten Person oder jede Person auf das Konto für soziale Netzwerke folgen falsch interpretiert werden. **FollowPerson** **true** wird impliziert nicht, dass **DoNotFollowPerson** auf **false festgelegt**ist.  <br/> |
|**followPerson** <br/> |Gibt an, ob der Anbieter Methodenaufruf [ISocialSession::FollowPerson](isocialsession-followperson.md) unterstützt. Die OSC **FollowPerson** überprüft, wenn **CacheFriends** **true** (zwischengespeicherte Synchronisierung Freunde) ist, **DynamicContactsLookup** ist **"true"** (bedarfsgesteuerten Synchronisierung von Freunde und nicht Freunde) oder beide **cacheFriends **und **DynamicContactsLookup** sind true (Hybrid Synchronisierung von Freunde und nicht Freunde). Wenn der Anbieter **FollowPerson** als **true**festgelegt wird, zeigt das osc bilden eine Netzwerk-Logo im Bereich Personen für Personen, die der Benutzer folgt, und ermöglicht die **auf \<Netzwerkname\> ** Befehl im Menü **Hinzufügen (+)** im Personen Bereich. Wenn der Anbieter **FollowPerson** als **false**legt fest, das Netzwerk-Logo wird nicht angezeigt, und die **auf \<Netzwerkname\> ** Befehl ist ausgeblendet.  <br/> |
|**getFriends** <br/> |Gibt an, ob der Anbieter Methodenaufruf [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) oder [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) unterstützt. Wenn der Anbieter **GetFriends** als **true**festgelegt wird, wird das osc bilden den Wert **CacheFriends** oder **DynamicContactsLookup** ermittelt, ob für soziale Netzwerke Freunde als Outlook-Kontaktelemente oder im Arbeitsspeicher gespeichert kann. Wenn der Anbieter **GetFriends** als **false**legt fest, für soziale Netzwerke Freunde und die **ISocialPerson::GetFriendsAndColleagues** und **ISocialSession2::GetPeopleDetails** Methoden nicht unterstützt, und die OSC werden die Werte der ignoriert **CacheFriends** und **DynamicContactsLookup**.  <br/> |
   
Die folgenden Elemente gelten nur für zwischengespeicherte Synchronisierung von Freunde oder Hybrid Synchronisierung von Freunde und nicht-Freunde. Weitere Informationen zum Synchronisieren von Freunden finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheFriends** <br/> |Gibt an, ob der OSC-Anbieter ermöglicht das Speichern von Freunden als Outlook-Kontaktelemente. Die OSC überprüft **CacheFriends** nur, wenn **GetFriends** auf **true**festgelegt ist. Wenn der Anbieter **CacheFriends** als **true**festgelegt wird, die OSC synchronisiert Freunde durch caching und erstellt einen Kontakteordner Netzwerk-spezifischen im Standardspeicher für Friend Kontakte des Benutzers. Der Name des Kontaktordners von Netzwerk-spezifische ist der Wert der Eigenschaft [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Wenn der Anbieter **CacheFriends** als **false**legt fest, erstellt das osc bilden keinen Netzwerk-spezifische Kontakteordner für Friend Kontakte Freunde gespeichert.  <br/> |
|**contactSyncRestartInterval** <br/> |Bestimmt das Wiederholungsintervall in Minuten zwischen Versuche, Freunde Informationen aus dem sozialen Netzwerk, synchronisieren, wenn ein Synchronisierungsfehler auftritt. Die OSC verwendet dieses Element nur, wenn der OSC-Anbieter unterstützt die zwischengespeicherten Synchronisierung oder Hybrid Synchronisierung von Freunde zu einem sozialen Netzwerk-bestimmten Kontakteordner (**CacheFriends** ist **true**).  <br/> Das Standard-Wiederholungsintervall ist 30 Minuten, es sei denn, der Standardwert von überschrieben wird die `ContactSyncRestartInterval` Schlüssel unter `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Wenn der Anbieter **ContactSyncRestartInterval**legt fest, wird der Wert der Anbieter das Standard-Wiederholungsintervall 30 Minuten oder den Wert des Registrierungsschlüssels außer Kraft setzen.  <br/> Weitere Informationen zum Synchronisieren von Freunde und nicht Freunde Informationen bei Bedarf finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).  <br/> |
   
Die folgenden Elemente gelten nur bedarfsgesteuerten Synchronisierung oder Hybrid Synchronisierung von Freunde und nicht-Freunde.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Gibt an, ob der OSC-Anbieter den Anruf [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) für bedarfsgesteuerten Synchronisierung von Freunde und Freunde-nicht unterstützt.  <br/> Die OSC überprüft **DynamicContactsLookup** nur, wenn **GetFriends** auf **true**festgelegt ist. Die Standardeinstellung für **DynamicContactsLookup** ist **false**.  <br/> Wenn der OSC-Anbieter **DynamicContactsLookup** als **true** und **GetFriends** als **true**angegeben wird, ruft der OSC **ISocialSession2::GetPeopleDetails** jedes Mal, wenn der Bereich Personen aktualisiert wird. Der Personenbereich wird aktualisiert, wenn der Benutzer einen anderen Benutzer im Bereich Personen oder einem anderen Element im Outlook Explorer-Fenster wählt oder ein Outlook-Inspektor-Fenster geöffnet. Nachschlagen von dynamischen wird sichergestellt, dass der Benutzer immer die neuesten Benutzerbilder und Profilinformationen im Bereich Personen sieht, jedoch die Anzahl der Aufrufe vom Anbieter für soziale Netzwerke erhöht.  <br/> Wenn der Anbieter **DynamicContactsLookup** als **"false"** festgelegt wird, wird die OSC **ISocialSession2::GetPeopleDetails** , um den Personenbereich aktualisieren nicht aufgerufen.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Gibt an, ob der bedarfsgesteuerten Synchronisierung für Freunde und nicht Freunde beim Bereich Personen minimiert wird die OSC ausführen soll.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Funktionen zur Unterstützung von Aktivitäten

Das folgende Element gilt für jede Form von Synchronisierung von Aktivitäten, die von der OSC-Anbieter unterstützt werden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**getActivities** <br/> |Gibt an, ob der Anbieter die Methode ruft [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) oder [ISocialPerson::GetActivities](isocialperson-getactivities.md) unterstützt. Wenn der Anbieter **GetActivities** als **true**festgelegt wird, verwendet das osc bilden den Wert der **CacheActivities** oder **DynamicActivitiesLookupEx** um festzustellen, ob die Website für soziale Netzwerke ermöglicht das Speichern von Aktivitäten als Outlook-RSS-Elemente oder als Aktivitäten im Arbeitsspeicher. Wenn der Anbieter **GetActivities** als **false**legt fest, das soziale Netzwerk unterstützt keine Aktivitäten sowie die **ISocialSession2::GetActivitiesEx** und **ISocialPerson::GetActivities** Methoden und die OSC ignoriert die Werte der ** CacheActivities** und **DynamicActivitiesLookupEx**.  <br/> |
   
Das folgende Element betrifft nur zwischengespeicherte Synchronisierung oder Hybrid Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**cacheActivities** <br/> |Ab Outlook Social Connector 2013, ignoriert die OSC dieses Element aus, da der Anbieter nicht mehr Aktivitäten synchronisieren können, indem sie in einem ausgeblendeten Ordner im Speicher des Benutzers Zwischenspeichern.  <br/> Wenn die Anbieter unterstützt die Aktivitäten des Anbieters unterstützen müssen synchronisieren Sie Aktivitäten auf Abruf. Der Anbieter **CacheActivities** als **"false"** festgelegt und **DynamicActivitesLookupEx** als **true**festgelegt. Die OSC Aktivitäten auf Abruf synchronisiert und Aktivitäten im Arbeitsspeicher zwischengespeichert. Die Aktivitäten Cachespeicher wird in einem 30-minütigen Intervall aktualisiert.  <br/> |
   
Die folgenden Elemente gelten nur bedarfsgesteuerten Synchronisierung oder Hybrid Synchronisierung von Aktivitäten.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Veraltet in OSC 1.1.  <br/> OSC 1.1 ab, der OSC nicht mehr [ISocialSession::GetActivities](isocialsession-getactivities.md) aufruft und ignoriert den Wert der **DynamicActivitiesLookup**. Legen Sie zur Unterstützung der Aktivitäten auf Abruf Lookup **CacheActivities** , wie **false** und **GetActivities** und **DynamicActivitiesLookupEx** als **true**und die OSC **ISocialSession2::GetActivitiesEx**aufgerufen werden.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Gibt an, ob der OSC-Anbieter den Anruf **ISocialSession2::GetActivitiesEx** für bedarfsgesteuerten Synchronisierung von Aktivitäten unterstützt.  <br/> Wenn der OSC-Anbieter Aktivitäten bedarfsgesteuerten Synchronisierung unterstützt, werden **GetActivities** und **DynamicActivitiesLookupEx** als **true**und **CacheActivities** als **"false"** festgelegt. Die OSC ruft **ISocialSession2::GetActivitiesEx** jedes Mal, wenn der Bereich Personen aktualisiert wird. Der Personenbereich wird aktualisiert, wenn der Benutzer das ausgewählte Element im Outlook Explorer-Fenster ändert oder ein Outlook-Inspektor-Fenster geöffnet. Dynamische Aktivitäten Lookup wird sichergestellt, dass der Benutzer wird stets die neuesten Aktivitäten im Bereich Personen angezeigt, jedoch wird die Anzahl der Aufrufe vom Anbieter für soziale Netzwerke erhöht.  <br/> Wenn der Anbieter **DynamicActivitiesLookupEx** als **"false"** festgelegt wird, wird die OSC **ISocialSession2::GetActivitiesEx** nicht für Personen, die Sie im Bereich Personen angezeigt aufgerufen.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Gibt an, ob bedarfsgesteuerten Synchronisierung für Aktivitäten beim Bereich Personen minimiert wird die OSC ausführen soll.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Allgemeine Funktionen zur Unterstützung bei Bedarf oder Hybriden Synchronisierung von Freunden, nicht Freunde und Aktivitäten

|**Element**|**Beschreibung**|
|:-----|:-----|
|**hashFunction** <br/> | Gibt die Hashfunktion, die der OSC-Anbieter unterstützt. Um personenbezogene Informationen von Benutzern zu schützen, die nicht auf des Anbieters für soziale Netzwerke oder LOB Anwendung sind, übergibt die OSC Hash e-Mail-Adressen an **ISocialSession2::GetPeopleDetails** und **ISocialSession2:: GetActivitiesEx**.  <br/>  Wenn **DynamicContactsLookup** auf **true** festgelegt ist, oder **DynamicActivitiesLookupEx** auf **true**festgelegt ist, muss der Anbieter **HashFunction** auf einen der zulässigen Werte festgelegt: **SHA1**, **MD5**oder **CRC32MD5**. **HashFunction** ist nicht vorhanden, oder gibt einen falschen Wert, gibt die OSC einen Fehler zurück.  <br/> **SHA1** ist Internet Engineering Task Force (IETF) US sicheren Hashalgorithmus 1 durch [[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt)definiert. Beispielsweise ist der **SHA1** Hash-Wert, der e-Mail-Adresse melissa@contoso.com `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** ist Internet Engineering Task Force (IETF) MD5 Message-Digest-Algorithmus von [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt)definiert. Beispielsweise ist der **MD5** Hash-Wert, der e-Mail-Adresse melissa@contoso.com `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** ist eine Kombination aus **CRC32** und **MD5** wie folgt definiert:  <br/>  Normalisieren der e-Mail-Adresse durch Entfernen von führende und nachfolgende Leerzeichen und konvertiert alle Zeichen in Kleinbuchstaben an.  <br/>  Berechnen des **CRC32** -Werts für die normalisierte e-Mail-Adresse, und verwenden Sie die decimal ganzzahlige Darstellung dieses Werts. Wenn die Implementierung ganze Zahlen mit Vorzeichen zurückgibt, müssen Sie die ganze Zahl mit Vorzeichen Ganzzahl ohne Vorzeichen konvertieren.  <br/>  Berechnen Sie den **MD5** -Wert für die normalisierte e-Mail-Adresse, und verwenden Sie die hex-Darstellung dieses Werts (mit Kleinbuchstaben A bis F).  <br/>  Kombinieren Sie diese beiden Werte mit einem Unterstrich an.  <br/>  Beispielsweise ist der **CRC32MD5** Hash-Wert, der e-Mail-Adresse melissa@contoso.com `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Funktionen zur Unterstützung von Authentifizierung und Kontokonfiguration

|**Element**|**Beschreibung**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Gibt an, ob das soziale Netzwerk der Benutzer so ändern Sie die automatische Konfiguration von Einstellungen wie eine andere URL zur Anmeldung bei bereitstellen kann.  <br/> |
|**createAccountUrl** <br/> |Wenn der Anbieter legt **HideHyperlinks** als **false**fest, wenn der Benutzer, **Klicken Sie hier, um ein Konto erstellen** , in das Feld der **Kontokonfiguration** -Dialogfeld klickt, wird die URL durch **CreateAccountUrl** angegebenen im Standardbrowser geöffnet.  <br/> |
|**displayUrl** <br/> |Gibt an, ob die OSC im Textfeld **URL-Adresse** für das soziale Netzwerk im Dialogfeld Konfiguration Konto angezeigt werden soll.  <br/> |
|**forgotPasswordUrl** <br/> |Wenn der Anbieter **HideHyperlinks** als **"false"** festgelegt, wenn der Benutzer klickt **Kennwort vergessen?** im Dialogfeld **Kontokonfiguration** die vom **ForgotPasswordUrl** angegebene URL im Standardbrowser wird geöffnet.  <br/> |
|**hideHyperlinks** <br/> |Gibt an, ob die OSC **Klicken Sie hier, um ein Konto erstellen** sollten ausblenden und **Kennwort vergessen?** Hyperlinks im Dialogfeld Konto-Konfiguration.  <br/> OSC-1.0 ignoriert diese Einstellung, und die Hyperlinks werden immer ausgeblendet. OSC-1.1 verwendet den Wert dieser Einstellung wird.  <br/> |
|**hideRememberMyPassword** <br/> |Gibt an, ob die OSC das Kontrollkästchen **Kennwort speichern** im Dialogfeld Konto Konfiguration ausblenden sollten.  <br/> Wenn der Anbieter **HideRememberMyPassword** als **true**festgelegt wird, fungiert der OSC wie, wenn das Feld **Kennwort speichern** deaktiviert ist und das Kennwort werden nicht gespeichert.  <br/> Wenn der Anbieter **HideRememberMyPassword** als **"false"** festgelegt wird, wird die OSC das Kontrollkästchen **Kennwort speichern** im Dialogfeld Konfiguration Konto angezeigt.  <br/> |
|**supportsAutoConfigure** <br/> |Gibt an, ob die OSC die **GetAutoConfiguredSession** -Funktion Sie für die **ISocialProvider** -Schnittstelle rufen sollte auf automatische Konfiguration versuchen, und melden Sie sich an dem sozialen Netzwerk für den Benutzer.  <br/> |
|**useLogonCached** <br/> |Gibt an, ob der OSC-Anbieter den Anruf [ISocialSession2::LogonCached](isocialsession2-logoncached.md) mit zwischengespeicherten Anmeldeinformationen anzumelden unterstützt.  <br/> Wenn der Anbieter **UseLogonCached** als **true**festgelegt wird, das osc bilden die Einstellung für **UseLogonWebAuth** ignoriert, und die OSC ruft **ISocialSession2::LogonCached** für die Authentifizierung.  <br/> Wenn der Anbieter **DynamicActivitiesLookupEx** als **"false"** festgelegt wird, wird die OSC **ISocialSession2::LogonCached** für die Authentifizierung nicht aufgerufen.  <br/> |
|**useLogonWebAuth** <br/> |Gibt an, ob die OSC formularbasierte Authentifizierung und die [ISocialSession::LogonWeb](isocialsession-logonweb.md) -Methode verwendet werden soll. Wenn der Anbieter **UseLogonWebAuth** als **false**legt fest, die OSC wird die Standardauthentifizierung verwendet und die [ISocialSession::Logon](isocialsession-logon.md) -Methode aufgerufen. Wenn der Anbieter **UseLogonWebAuth** als **true**festgelegt wird, die OSC formularbasierte Authentifizierung verwendet wird und **ISocialSession::LogonWeb**aufruft.  <br/> |
   
Je nach den **Funktionen** XML der vom Anbieter zurückgegebene in der **ISocialProvider::GetCapabilities** -Methode, die Kontokonfiguration Dialogfeldes wechselt. Abbildung 1 wird beispielsweise ein Beispiel für das TestProvider im Dialogfeld Konfiguration Konto angezeigt. 
  
**Abbildung 1. TestProvider-Beispiel im Dialogfeld Konto-Konfiguration**

![TestProvider-Beispielkonfigurationsinformationen](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)

