---
title: XML-Code für Freunde
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Das Freunde-Element im XML-Schema von Microsoft Outlook Social Connector (OSC) Anbieter ermöglicht ein OSC-Anbieters zum Angeben von Informationen für eine Liste der Personen, die ein Outlook-Benutzer im sozialen Netzwerk zugeordnet.
ms.openlocfilehash: 07f1bb77e7912e3973fd2af8a70275642b72039c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796108"
---
# <a name="xml-for-friends"></a>XML-Code für Freunde

Das **Freunde** -Element im XML-Schema von Microsoft Outlook Social Connector (OSC) Anbieter ermöglicht ein OSC-Anbieters zum Angeben von Informationen für eine Liste der Personen, die ein Outlook-Benutzer im sozialen Netzwerk zugeordnet. Wenn der OSC-Anbieter zwischengespeicherten Synchronisierung unterstützt, enthält die Liste der Person nur Freunde des Outlook-Benutzers im sozialen Netzwerk. Wenn die OSC auf Abruf oder Hybriden Synchronisierung unterstützt, kann diese Liste Freunde und Familie des Outlook-Benutzers enthalten. 

Jede Person in der Liste wird als **Person** -Element im XML-Schema dargestellt, das Details wie Vorname, Nachname und e-Mail-Adressen unterstützt. OSC-Providers verwenden Sie die **Freunde** und **Person** Elemente unabhängig davon, wie sie die OSC Friend-Informationen aus dem sozialen Netzwerk synchronisieren möchten. Beachten Sie, dass die untergeordneten Elemente des **Person** einige der Eigenschaften des Outlook-Kontakte, die mit dem sozialen Netzwerk, das Speichern von Freunde in einem bestimmten Outlook-Kontakteordner erleichtert ähneln, wenn der sozialen Netzwerk unterstützt zwischengespeichert oder hybrid Synchronisierung von Freunde zu einem Outlook-Kontakteordner. 

## <a name="example-scenarios"></a>Beispielszenarien

Die folgenden Beispielszenarien Anzeigen der OSC-Anbieter Erweiterbarkeits-API-Aufrufe, die ein OSC-Anbieter implementiert und die OSC stellt Friend Informationen zu erhalten. Informationen wird in XML-Zeichenfolgen ausgedrückt, die das OSC-Anbieter-XML-Schema entsprechen.
  
Ein Beispiel dafür Freunde XML finden Sie unter [Freunde XML-Beispiel](friends-xml-example.md). Weitere Informationen zum Synchronisieren von Informationen von Freunden finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Szenario 1: Abrufen einer Liste von Freunden

Szenario 1 – OSC Ruft eine Liste mit Freunde, und ein [ISocialPerson](isocialpersoniunknown.md) -Objekt und ein Bild für jede Friend: 
    
1. Ein OSC-Anbieter unterstützt, Freunde von der Website für soziale Netzwerke angezeigt und ermöglicht es, dass die OSC Informationen zwischengespeichert werden Friend angibt, der an die OSC mithilfe der **GetFriends** und **CacheFriends** -Elemente, die untergeordnete Elemente des der **sind Funktionen** Element. 
    
2. Der OSC-Anbieter implementiert auch die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)und [ISocialPerson::GetPicture](isocialperson-getpicture.md) -Methoden. 
    
3. Die OSC-Anrufe **ISocialProvider::GetCapabilities** , um den Wert der folgenden Elemente überprüfen: **GetFriends** überprüfen, ob der OSC-Anbieter unterstützt Freunde aus dem sozialen Netzwerk und **CacheFriends** überprüfen, ob den Anbieter angezeigt. Zwischenspeichern Freunde unterstützt. 
    
4. Die OSC ruft **ISocialSession::GetPerson** zum Abrufen eines **ISocialPerson** -Objekts für den Outlook-Benutzer. 
    
5. Die OSC **ISocialPerson::GetFriendsAndColleagues** zum Abrufen des Outlook-Benutzers Ruft die Freunde-Liste in der _PersonCollection_ Parameterzeichenfolge zurückgegeben. Die Zeichenfolge _PersonCollection_ erfüllt die XML-Schemadefinition für das **Freunde** -Element im XML-Schema. 
    
6. Für jede Friend in der XML-Zeichenfolge _PersonCollection_ erhält der OSC Wert des Elements **UserID** **ISocialSession::GetPerson** zum Abrufen eines **ISocialPerson** -Objekts für diese Friend aufrufen. 
    
7. Für jede Friend in der XML-Zeichenfolge **PersonCollection** ruft der OSC [ISocialPerson::GetPicture](isocialperson-getpicture.md) um eine Bildressource für diese Friend abzurufen. 
    
   Die OSC kann weiter auf das Objekt **ISocialPerson** Aktivitäten und Details (beispielsweise e-Mail-Adressen) abzurufen für diese Freund anrufen. 
    
### <a name="scenario-2-synchronize-friends"></a>Szenario 2: Synchronisieren von Freunden 

Szenario 2 – OSC Freunde dynamisch synchronisiert:
    
1. Ein OSC-Anbieter, der unterstützt der bedarfsgesteuerten Synchronisierung von Freunde und nicht Freunde, angibt, der die OSC, mithilfe der **GetFriends** und **DynamicContactsLookup** Elemente. Der OSC-Anbieter wird auch das **HashFunction** -Element. Alle drei Elemente sind untergeordnete Elemente des **Funktionen**. 
    
2. Der OSC-Anbieter implementiert auch die [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) -Methode. 
    
3. Die OSC ruft **ISocialProvider::GetCapabilities** zum Überprüfen der Werte von **GetFriends** und **DynamicContactsLookup** , um sicherzustellen, dass der OSC-Anbieter Freunde und bedarfsgesteuerten Synchronisierung von Freunde und Freunde-nicht unterstützt. Die OSC können Sie auch den Wert des **HashFunction** von der OSC-Anbieter unterstützt werden. 
    
4. Für jeden Benutzer im Bereich Personen angezeigt die OSC sammelt e-Mail-Adresse des Benutzers und verschlüsselt sie mithilfe der Hashfunktion in **HashFunction**angegeben. Stellt eine XML-Zeichenfolge, die die XML-Schemadefinition für das **HashedAddresses** -Element entspricht. 
    
5. Die OSC ruft **ISocialSession2::GetPeopleDetails**, bietet diese XML-Zeichenfolge Hash-Adressen als _PersonAddresses_ -Parameter, um dynamisch aktualisierte Details für Personen, die im Parameter _PersonsCollection_ zu erhalten. Die Zeichenfolge für den _PersonsCollection_ -Parameter entspricht der XML-Schemadefinition für das **Freunde** -Element im XML-Schema. 

## <a name="parent-and-child-elements"></a>Übergeordnete und untergeordnete Elemente

Im folgenden werden die beiden auf oberster Ebene Elemente im Schema **Freunde** . 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**Freunde** <br/> |Stellt das Stammelement des eine Liste von Elementen der **Person** . Die **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)und **ISocialSession2::GetPeopleDetails** zurückgeben XML-Zeichenfolgen, die entsprechen der Schemadefinition des **Freunde** -Elements.  <br/> |
|**Person** <br/> |Stellt eine Person in einer Liste von Elementen der **Person** . Die [ISocialPerson::GetDetails](isocialperson-getdetails.md) -Methode gibt eine XML-Zeichenfolge gemäß der Schemadefinition des Elements **Person** zurück.  <br/> |
   
In der folgenden Tabelle wird jede untergeordnete Element des Elements **Person** im Schema XML OSC-Anbieter beschrieben. 
  
Eine vollständige Definition des OSC-Anbieter XML-Schema, welche Elemente sind, erforderlich oder optional, einschließlich finden Sie unter [Outlook Social Connector Provider XML-Schema](outlook-social-connector-provider-xml-schema.md).
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**Adresse** <br/> |Physische Straße der Person ein.  <br/> |
|**Jahrestag** <br/> |Jahrestag für ein Ereignis für die Person.  <br/> |
|**askmeabout** <br/> |Die Themen der Interessen oder Kompetenzen der Person ein.  <br/> |
|**Geburtsdatum** <br/> |Geburtsdatum der Person ein.  <br/> |
|**businessAddress** <br/> |Physische Straße Jahrestag der Person.  <br/> |
|**businessCity** <br/> |Ort für die Person Jahrestag.  <br/> |
|**businessCountryOrRegion** <br/> |Land oder Region des Jahrestag der Person.  <br/> |
|**businessState** <br/> |Bundesland oder den Kanton des Jahrestag der Person.  <br/> |
|**businessZip** <br/> |Postleitzahl der Jahrestag der Person.  <br/> |
|**Zelle** <br/> |Die Mobiltelefonnummer für die Person.  <br/> |
|**Ort** <br/> |Der Ort für die physische Adresse der Person ein.  <br/> |
|**Unternehmen** <br/> |Name der Firma, mit der Person.  <br/> |
|**countryOrRegion** <br/> |Land oder Region, der die physische Adresse der Person ein.  <br/> |
|**creationTime** <br/> |Zeitpunkt der Erstellung des Profils im sozialen Netzwerk der Person.  <br/> |
|**emailAddress** <br/> |Primäre e-Mail-Adresse der Person ein.  <br/> |
|**emailAddress2** <br/> |Sekundäre e-Mail-Adresse der Person ein.  <br/> |
|**emailAddress3** <br/> |Dritten e-Mail-Adresse der Person ein.  <br/> |
|**expirationTime** <br/> |Die Zeit, die der Person Profildaten im sozialen Netzwerk läuft ab.  <br/> |
|**fileAs** <br/> |Zeichenfolge, durch die die Person eingereicht werden, wie Sie ein Kontakt in einer Outlook Datei kontaktiert.  <br/> |
|**firstName** <br/> |Vor- oder angegebenen Namen der Person ein.  <br/> |
|**friendStatus** <br/> |Friend-Status dieser Person mit der angemeldete Benutzer auf dem sozialen Netzwerk. Muss einer der folgenden Werte sein: **Freund**, **Nonfriend**, **ausstehende**, **Pendingin**, **Pendingout**.  <br/> |
|**fullName** <br/> |Vollständigen Namen der Person ein.  <br/> |
|**Geschlecht** <br/> |Geschlecht der Person ein. Muss einer der folgenden Werte sein: **Männlich**, **Weiblich**, **nicht angegeben**.  <br/> |
|**homePhone** <br/> |Private Telefonnummer der Person ein.  <br/> |
|**Index** <br/> |Speicherort der Hash-Adresse der Person in der _PersonsAddresses_ -Parameter, die an einen Aufruf der **ISocialSession2::GetPeopleDetails** -Methode übergeben werden. Es gibt auch die Person **Person** XML in die von **GetPeopleDetails**zurückgegebene _PersonsCollection_ -Zeichenfolge an.  <br/> |
|**Branchen** <br/> |Branchen, denen an die Person beteiligt ist.  <br/> |
|**Interessen** <br/> |Interessen oder Hobbys der Person ein.  <br/> |
|**lastModificationTime** <br/> |Zeitpunkt der letzten Änderung der Person Profil für das soziale Netzwerk.  <br/> |
|**lastName** <br/> |Nachname oder Nachnamen der Person ein.  <br/> |
|**location** <br/> |Die Position der Person ein.  <br/> |
|**Spitzname** <br/> |Einen kürzeren Namen oder erfundenen Namen der Person ein.  <br/> |
|**otherAddress** <br/> |Alternative Straße der Person ein.  <br/> |
|**otherCity** <br/> |Ort der alternativen Adresse der Person.  <br/> |
|**otherCountryOrRegion** <br/> |Land oder Region der alternativen Adresse der Person.  <br/> |
|**otherState** <br/> |Bundesland oder Kanton der alternativen Adresse der Person.  <br/> |
|**otherZip** <br/> |Postleitzahl der alternativen Adresse der Person.  <br/> |
|**Telefon** <br/> |Primäre Telefonnummer der Person ein.  <br/> |
|**Bild-URL** <br/> |URL für ein Profilbild der Person ein.  <br/> |
|**Beziehung** <br/> |Beziehung zwischen dieser Person mit angemeldeten Benutzers.  <br/> |
|**Schulen** <br/> |Die Schulen, die die Person wechselt oder war.  <br/> |
|**Fähigkeiten** <br/> |Persönliche Fachkenntnisse der Person.  <br/> |
|**state** <br/> |Bundesland / Kanton, der die physische Adresse der Person ein.  <br/> |
|**title** <br/> |Bezeichnung den Namen der Person hinzugefügt.  <br/> |
|**Benutzer-ID** <br/> |ID die Person im sozialen Netzwerk identifiziert.  <br/> |
|**webProfilePage** <br/> |Webseite-Adresse, die ein Profil der Person enthält.  <br/> |
|**Website** <br/> |Website der Person.  <br/> |
|**workPhone** <br/> |Geschäftliche Telefonnummer der Person ein.  <br/> |
|**ZIP** <br/> |Postleitzahl oder die Postleitzahl der physischen Adresse der Person ein.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Freunde XML-Beispiel](friends-xml-example.md)  
- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML-Code für Funktionen](xml-for-capabilities.md) 
- [XML-Code für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

