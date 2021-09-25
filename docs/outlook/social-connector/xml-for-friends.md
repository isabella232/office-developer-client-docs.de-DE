---
title: XML für „friends“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Das Friends-Element im XML-Schema des Microsoft Outlook Connector für soziale Netzwerke (OSC) ermöglicht es einem OSC-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook Benutzer im sozialen Netzwerk zugeordnet sind.
ms.openlocfilehash: a6d8dbe78e40f94ea5fe30e7361b37ef05c46a02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590345"
---
# <a name="xml-for-friends"></a>XML für „friends“

Das **Friends-Element** im XML-Schema des Microsoft Outlook Connector für soziale Netzwerke (OSC) ermöglicht es einem OSC-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook Benutzer im sozialen Netzwerk zugeordnet sind. Wenn der OSC-Anbieter die zwischengespeicherte Synchronisierung unterstützt, enthält diese Liste nur Freunde des Outlook Benutzers im sozialen Netzwerk. Wenn das OSC die On-Demand- oder Hybridsynchronisierung unterstützt, kann diese Liste sowohl Freunde als auch Nicht-Freunde des Outlook Benutzers enthalten. 

Jede Person in der Liste wird als **Personenelement** im XML-Schema dargestellt, das Details wie Vornamen, Nachnamen und E-Mail-Adressen unterstützt. OSC-Anbieter verwenden die **Elemente "Freunde"** und **"Person",** unabhängig davon, wie sie möchten, dass der OSC Freundesinformationen aus dem sozialen Netzwerk synchronisiert. Beachten Sie, dass die untergeordneten Elemente einer **Person** mit einigen eigenschaften eines Outlook Kontakts vergleichbar sind, was das Speichern von Freunden in einem Outlook Kontaktordner speziell für das soziale Netzwerk erleichtert, wenn das soziale Netzwerk die zwischengespeicherte oder hybride Synchronisierung von Freunden mit einem Outlook Kontaktordner unterstützt. 

## <a name="example-scenarios"></a>Beispielszenarien

Die folgenden Beispielszenarien zeigen die OSC-Anbietererweiterungs-API-Aufrufe, die von einem OSC-Anbieter implementiert werden, und die OSC zum Abrufen von Friend-Informationen. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
  
Ein Beispiel für den XML-Code für Freunde finden Sie unter ["Friends XML-Beispiel".](friends-xml-example.md) Weitere Informationen zum Synchronisieren der Informationen von Freunden finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md)

### <a name="scenario-1-get-a-list-of-friends"></a>Szenario 1: Abrufen einer Liste von Freunden

Szenario 1: OSC ruft eine Liste von Freunden sowie ein [ISocialPerson-Objekt](isocialpersoniunknown.md) und ein Bild für jeden Freund ab: 
    
1. Ein OSC-Anbieter, der das Anzeigen von Freunden von der Website des sozialen Netzwerks unterstützt und es dem OSC ermöglicht, Freundesinformationen zwischenzuspeichern, weist darauf hin, dass der OSC die **Elemente "getFriends"** und **"cacheFriends"** verwendet, bei denen es sich um untergeordnete Elemente des **Capabilities-Elements** handelt. 
    
2. Der OSC-Anbieter implementiert auch die Methoden [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)und [ISocialPerson::GetPicture.](isocialperson-getpicture.md) 
    
3. Der OSC ruft **ISocialProvider::GetCapabilities** auf, um den Wert der folgenden Elemente zu überprüfen: **getFriends,** um zu überprüfen, ob der OSC-Anbieter das Anzeigen von Freunden aus dem sozialen Netzwerk unterstützt, und **cacheFriends,** um zu überprüfen, ob der Anbieter das Zwischenspeichern von Freunden unterstützt. 
    
4. Der OSC ruft **ISocialSession::GetPerson** auf, um ein **ISocialPerson-Objekt** für den Outlook Benutzer abzurufen. 
    
5. Der OSC ruft **ISocialPerson::GetFriendsAndColleagues** auf, um die Outlook Freundesliste des Benutzers in der _Parameterzeichenfolge "personCollection"_ zurückzugeben. Die  _personCollection-Zeichenfolge_ entspricht der XML-Schemadefinition für das **Friends-Element** im XML-Schema. 
    
6. Für jeden Friend  in der personCollection-XML-Zeichenfolge ruft der OSC den Wert des **userID-Elements** ab, um **ISocialSession::GetPerson** aufzurufen, um ein **ISocialPerson-Objekt** für diesen Freund abzurufen. 
    
7. Für jeden Freund  in der personCollection-XML-Zeichenfolge ruft der OSC [ISocialPerson::GetPicture](isocialperson-getpicture.md) auf, um eine Bildressource für diesen Freund abzurufen. 
    
   Der OSC kann weitere Aufrufe des **ISocialPerson-Objekts** ausführen, um Aktivitäten und Details (z. B. E-Mail-Adressen) für diesen Freund abzurufen. 
    
### <a name="scenario-2-synchronize-friends"></a>Szenario 2: Synchronisieren von Freunden 

Szenario 2: OSC synchronisiert Freunde dynamisch:
    
1. Ein OSC-Anbieter, der die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt, gibt dies für osc mithilfe der **getFriends-** und **dynamicContactsLookup-Elemente** an. Der OSC-Anbieter legt auch das **hashFunction-Element** fest. Alle drei Elemente sind untergeordnete Elemente von **Funktionen.** 
    
2. Der OSC-Anbieter implementiert auch die [ISocialSession2::GetPeopleDetails-Methode.](isocialsession2-getpeopledetails.md) 
    
3. Der OSC ruft **ISocialProvider::GetCapabilities** auf, um die Werte von **getFriends** und **dynamicContactsLookup** zu überprüfen, um sicherzustellen, dass der OSC-Anbieter Freunde und die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt. Der OSC notiert auch den Wert der **hashFunction,** die vom OSC-Anbieter unterstützt wird. 
    
4. Für jeden Benutzer, der im Personenbereich angezeigt wird, erfasst osc die E-Mail-Adresse des Benutzers und verschlüsselt sie mithilfe der in **hashFunction** angegebenen Hashfunktion. Dies bildet eine XML-Zeichenfolge, die der XML-Schemadefinition für das **HashedAddresses-Element** entspricht. 
    
5. Der OSC ruft **ISocialSession2::GetPeopleDetails** auf und stellt diese XML-Zeichenfolge mit Hashadressen als  _personAddresses-Parameter_ bereit, um dynamisch aktualisierte Details für Personen im  _Parameter "personsCollection"_ abzurufen. Die Zeichenfolge des  _personsCollection-Parameters_ entspricht der XML-Schemadefinition für das **Friends-Element** im XML-Schema. 

## <a name="parent-and-child-elements"></a>Übergeordnete und untergeordnete Elemente

Es folgen die beiden Elemente auf  oberster Ebene im Freundesschema. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**Freunde** <br/> |Stellt das Stammelement einer Liste von **Personenelementen** dar. Die **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)und **ISocialSession2::GetPeopleDetails** geben XML-Zeichenfolgen zurück, die der Schemadefinition des **Friends-Elements** entsprechen.  <br/> |
|**person** <br/> |Stellt eine Person in einer Liste von **Personenelementen** dar. Die [ISocialPerson::GetDetails-Methode](isocialperson-getdetails.md) gibt eine XML-Zeichenfolge zurück, die der Schemadefinition des **Personenelements** entspricht.  <br/> |
   
In der folgenden Tabelle werden die einzelnen untergeordneten Elemente des **Personenelements** im OSC-Anbieter-XML-Schema beschrieben. 
  
Eine vollständige Definition des OSC-Anbieter-XML-Schemas, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook XML-Schema](outlook-social-connector-provider-xml-schema.md)des Connector für soziale Netzwerke.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**address** <br/> |Physische Anschrift der Person.  <br/> |
|**Jahrestag** <br/> |Fälligkeitsdatum für ein Ereignis für die Person.  <br/> |
|**askmeabout** <br/> |Themen, die von Interesse oder Fachwissen der Person sind.  <br/> |
|**birthday** <br/> |Geburtsdatum der Person.  <br/> |
|**businessAddress** <br/> |Physische Anschrift des Arbeitsplatzes der Person.  <br/> |
|**businessCity** <br/> |Ort für den Arbeitsplatz der Person.  <br/> |
|**businessCountryOrRegion** <br/> |Land oder Region des Arbeitsplatzes der Person.  <br/> |
|**businessState** <br/> |Bundesland oder Kanton des Arbeitsplatzes der Person.  <br/> |
|**businessZip** <br/> |Postleitzahl des Arbeitsplatzes der Person.  <br/> |
|**Zelle** <br/> |Mobiltelefonnummer für die Person.  <br/> |
|**Stadt** <br/> |Ort der physischen Adresse der Person.  <br/> |
|**company** <br/> |Name des Unternehmens, das der Person zugeordnet ist.  <br/> |
|**countryOrRegion** <br/> |Land oder Region der physischen Adresse der Person.  <br/> |
|**Creationtime** <br/> |Erstellungszeit des Profils der Person im sozialen Netzwerk.  <br/> |
|**emailAddress** <br/> |Primäre E-Mail-Adresse der Person.  <br/> |
|**emailAddress2** <br/> |Sekundäre E-Mail-Adresse der Person.  <br/> |
|**emailAddress3** <br/> |Empfänger-E-Mail-Adresse der Person.  <br/> |
|**expirationTime** <br/> |Zeit, zu der die Profildaten der Person im sozialen Netzwerk ablaufen.  <br/> |
|**fileAs** <br/> |Zeichenfolge, mit der die Person als Kontakt in einer Outlook Kontaktdatei abgelegt werden soll.  <br/> |
|**firstName** <br/> |Vorname oder Vorname der Person.  <br/> |
|**friendStatus** <br/> |Friend-Status dieser Person mit dem angemeldeten Benutzer im sozialen Netzwerk. Muss einer der folgenden Werte sein: **friend**, **nonfriend**, **pending**, **pendingin**, **pendingout**.  <br/> |
|**Fullname** <br/> |Vollständiger Name der Person.  <br/> |
|**Geschlecht** <br/> |Geschlecht der Person. Muss einer der folgenden Werte sein: **male**, **female**, **unpecified**.  <br/> |
|**homePhone** <br/> |Privattelefonnummer für die Person.  <br/> |
|**Index** <br/> |Speicherort der gehashten Adresse der Person im  _Zeichenfolgenparameter "personsAddresses",_ der an einen Aufruf der **ISocialSession2::GetPeopleDetails-Methode** übergeben wird. Es gibt auch den  Personen-XML-Code der Person in der von **GetPeopleDetails** zurückgegebenen _Personensammlungszeichenfolge_ an.  <br/> |
|**Industrien** <br/> |Branchen, in denen die Person tätig ist.  <br/> |
|**interests** <br/> |Interessen oder Hobbys der Person.  <br/> |
|**lastModificationTime** <br/> |Zeitpunkt, zu dem das Profil der Person zuletzt im sozialen Netzwerk geändert wurde.  <br/> |
|**lastName** <br/> |Nachname oder Nachname der Person.  <br/> |
|**location** <br/> |Der Speicherort der Person.  <br/> |
|**Spitzname** <br/> |Ein kürzerer Name oder Name der Person.  <br/> |
|**otherAddress** <br/> |Alternative Anschrift der Person.  <br/> |
|**otherCity** <br/> |Ort der alternativen Adresse der Person.  <br/> |
|**otherCountryOrRegion** <br/> |Land oder Region der alternativen Adresse der Person.  <br/> |
|**otherState** <br/> |Bundesland oder Kanton der alternativen Adresse der Person.  <br/> |
|**otherZip** <br/> |Postleitzahl der alternativen Adresse der Person.  <br/> |
|**Telefon** <br/> |Primäre Kontakttelefonnummer für die Person.  <br/> |
|**pictureUrl** <br/> |URL für ein Profilbild der Person.  <br/> |
|**Beziehung** <br/> |Beziehung dieser Person zum angemeldeten Benutzer.  <br/> |
|**schools** <br/> |Die Schulen, zu denen die Person geht oder zu der sie gegangen ist.  <br/> |
|**skills** <br/> |Persönliche Fähigkeiten der Person.  <br/> |
|**state** <br/> |Bundesland oder Kanton der physischen Adresse der Person.  <br/> |
|**title** <br/> |Bezeichnung, die dem Namen der Person hinzugefügt wurde.  <br/> |
|**Userid** <br/> |ID, um die Person im sozialen Netzwerk zu identifizieren.  <br/> |
|**webProfilePage** <br/> |Webseitenadresse, die ein Profil der Person enthält.  <br/> |
|**Website** <br/> |Die Website der Person.  <br/> |
|**workPhone** <br/> |Geschäftliche Telefonnummer für die Person.  <br/> |
|**Zip** <br/> |Postleitzahl oder Postleitzahl der physischen Adresse der Person.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Xml-Beispiel für Freunde](friends-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Funktionen](xml-for-capabilities.md) 
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

