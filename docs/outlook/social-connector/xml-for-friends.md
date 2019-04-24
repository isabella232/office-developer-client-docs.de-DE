---
title: XML für „friends“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Das Friends-Element im XML-Schema des Microsoft Outlook Social Connector (OSC)-Anbieters ermöglicht es einem OSC-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook-Benutzer im sozialen Netzwerk zugeordnet sind.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361159"
---
# <a name="xml-for-friends"></a>XML für „friends“

Das **friends** -Element im XML-Schema des Microsoft Outlook Social Connector (OSC)-Anbieters ermöglicht es einem osc-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook-Benutzer im sozialen Netzwerk zugeordnet sind. Wenn der OSC-Anbieter die zwischengespeicherte Synchronisierung unterstützt, enthält diese Liste der Personen nur Freunde des Outlook-Benutzers im sozialen Netzwerk. Wenn der OSC die on-Demand-oder Hybrid Synchronisierung unterstützt, kann diese Liste sowohl Freunde als auch nicht-Freunde des Outlook-Benutzers enthalten. 

Jede Person in der Liste wird als **Person** -Element im XML-Schema dargestellt, das Details wie Vorname, Nachname und e-Mail-Adressen unterstützt. OSC-Anbieter verwenden die Elemente **friends** und **Person** , unabhängig davon, wie Sie möchten, dass der osc Friend-Informationen aus dem sozialen Netzwerk synchronisiert. Beachten Sie, dass die untergeordneten Elemente von **Person** mit einigen der Eigenschaften eines Outlook-Kontakts vergleichbar sind, wodurch das Speichern von Freunden in einem Outlook-Kontakteordner für das soziale Netzwerk erleichtert wird, wenn das soziale Netzwerk zwischengespeichert oder Hybrid unterstützt. Synchronisierung von Freunden mit einem Outlook-Kontaktordner. 

## <a name="example-scenarios"></a>Beispielszenarien

Die folgenden Beispielszenarien zeigen die OSC-Anbieter-Erweiterbarkeits-API-Aufrufe, die ein OSC-Anbieter implementiert, und der OSC zum Abrufen von Friend-Informationen. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem OSC-Anbieter-XML-Schema entsprechen.
  
Ein Beispiel für Freundes-XML finden Sie unter [friends XML example](friends-xml-example.md). Weitere Informationen zum Synchronisieren von Freundes Informationen finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Szenario 1: Abrufen einer Liste von Freunden

Szenario 1 – OSC Ruft eine Liste von Freunden und ein [ISocialPerson](isocialpersoniunknown.md) -Objekt und ein Bild für jeden Freund ab: 
    
1. Ein OSC-Anbieter, der die Anzeige von Freunden vom sozialen Netzwerkstandort unterstützt und dem OSC das Zwischenspeichern von Friend-Informationen ermöglicht, **** weist darauf hin, dass der osc mithilfe der getfriends-und **cacheFriends** -Elemente, die untergeordnete Elemente des ** Capabilities** -Element. 
    
2. Der OSC-Anbieter implementiert auch die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md)-, [ISocialSession:: GetPerson](isocialsession-getperson.md)-, [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)-und [ISocialPerson:: GetPicture](isocialperson-getpicture.md) -Methoden. 
    
3. OSC ruft **ISocialProvider:: getCapabilities** auf, um den Wert der folgenden Elemente zu überprüfen: getfriends, um zu überprüfen, ob der osc-Anbieter unterstützt, Freunde aus dem sozialen Netzwerk anzuzeigen, und **** **cacheFriends** , um zu überprüfen, ob der Anbieter unterstützt das Zwischenspeichern von Freunden. 
    
4. OSC ruft **ISocialSession:: GetPerson** auf, um ein **ISocialPerson** -Objekt für den Outlook-Benutzer abzurufen. 
    
5. OSC ruft **ISocialPerson:: GetFriendsAndColleagues** auf, um die Freundesliste des Outlook-Benutzers in __ der personcollection-Parameterzeichenfolge zurückzugeben. Die _personCOLLECTION_ -Zeichenfolge entspricht der XML-Schema Definition für das **friends** -Element im XML-Schema. 
    
6. Für jeden Freund in der _personcollection_ -XML-Zeichenfolge ruft osc den Wert des **UserID** -Elements ab, um **ISocialSession:: GetPerson** aufzurufen, um ein **ISocialPerson** -Objekt für diesen Freund abzurufen. 
    
7. Für jeden Freund in der **personcollection** -XML-Zeichenfolge ruft osc [ISocialPerson:: GetPicture](isocialperson-getpicture.md) auf, um eine Bildressource für diesen Freund abzurufen. 
    
   OSC kann weitere Aufrufe für das **ISocialPerson** -Objekt durchführen, um Aktivitäten und Details (beispielsweise e-Mail-Adressen) für diesen Freund abzurufen. 
    
### <a name="scenario-2-synchronize-friends"></a>Szenario 2: Synchronisieren von Freunden 

Szenario 2 – OSC synchronisiert Freunde dynamisch:
    
1. Ein OSC-Anbieter, der die on-Demand-Synchronisierung von Freunden und nicht-Freunden unterstützt, weist darauf **** hin, dass der osc mithilfe der Elemente getfriends und **dynamicContactsLookup** . Der OSC-Anbieter legt auch das **hashFunction** -Element fest. Alle drei Elemente sind untergeordnete Elemente der **Funktionen**. 
    
2. Der OSC-Anbieter implementiert auch die [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) -Methode. 
    
3. OSC ruft **ISocialProvider:: getCapabilities** auf, um die Werte von **getfriends** und **dynamicContactsLookup** zu überprüfen, um zu überprüfen, ob der osc-Anbieter Freunde und bedarfsgesteuerte Synchronisierung von Freunden und nicht-Freunden unterstützt. Der OSC nimmt auch den Wert von **hashFunction** zur Kenntnis, der vom osc-Anbieter unterstützt wird. 
    
4. Für jeden Benutzer, der im Personen Bereich angezeigt wird, sammelt der OSC die e-Mail-Adresse des Benutzers und verschlüsselt ihn mithilfe der in **hashFunction**angegebenen Hashfunktion. Hierbei handelt es sich um eine XML-Zeichenfolge, die der XML-Schema Definition für das **HASHEDADDRESSES** -Element entspricht. 
    
5. OSC ruft **ISocialSession2:: GetPeopleDetails**auf, wobei diese XML-Zeichenfolge von Hash-Adressen als _personAddresses_ -Parameter bereitgestellt wird, um dynamisch aktualisierte Details für Personen im persons-Parameter abzurufen. __ Die __ Strings-Parameter der personcollection entsprechen der XML-Schema Definition für das **friends** -Element im XML-Schema. 

## <a name="parent-and-child-elements"></a>Übergeordnete und untergeordnete Elemente

Nachfolgend finden Sie die beiden Elemente der obersten Ebene im **friends** -Schema. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**Freunde** <br/> |Stellt das Stammelement einer Liste von **Person** -Elementen dar. Die **ISocialPerson:: GetFriendsAndColleagues**, [ISocialSession:: FindPerson](isocialsession-findperson.md)und **ISOCIALSESSION2:: GetPeopleDetails** XML-Zeichenfolgen zurückgeben, die der Schema Definition des **friends** -Elements entsprechen.  <br/> |
|**Person** <br/> |Stellt eine Person in einer Liste von **Person** -Elementen dar. Die [ISocialPerson:: getDetails](isocialperson-getdetails.md) -Methode gibt eine XML-Zeichenfolge zurück, die der Schema Definition des **Person** -Elements entspricht.  <br/> |
   
In der folgenden Tabelle werden die einzelnen untergeordneten Elemente des **Person** -Elements im XML-Schema des osc-Anbieters beschrieben. 
  
Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**address** <br/> |Physikalische Adresse der Person.  <br/> |
|**Jahrestag** <br/> |Jubiläumsdatum für ein Ereignis für die Person.  <br/> |
|**askmeabout** <br/> |Themen von Interesse oder Fachwissen der Person.  <br/> |
|**birthday** <br/> |Geburtsdatum der Person.  <br/> |
|**businessAddress** <br/> |Physikalische Adresse des Arbeitsplatzes der Person.  <br/> |
|**businessCity** <br/> |Ort für den Arbeitsplatz der Person.  <br/> |
|**businessCountryOrRegion** <br/> |Das Land oder die Region des Arbeitsplatzes der Person.  <br/> |
|**businessState** <br/> |Bundesland oder Kanton des Arbeitsplatzes der Person.  <br/> |
|**businessZip** <br/> |Postleitzahl des Arbeitsplatzes der Person.  <br/> |
|**Zelle** <br/> |Mobiltelefonnummer für die Person.  <br/> |
|**city** <br/> |Ort der physischen Adresse der Person.  <br/> |
|**company** <br/> |Name des Unternehmens, das der Person zugeordnet ist.  <br/> |
|**countryOrRegion** <br/> |Land oder Region der physischen Adresse der Person.  <br/> |
|**creationTime** <br/> |Erstellungszeit des Profils der Person im sozialen Netzwerk.  <br/> |
|**emailAddress** <br/> |Primäre e-Mail-Adresse der Person.  <br/> |
|**emailAddress2** <br/> |Sekundäre e-Mail-Adresse der Person.  <br/> |
|**emailAddress3** <br/> |Tertiäre e-Mail-Adresse der Person.  <br/> |
|**expirationTime** <br/> |Zeitpunkt, zu dem die Profildaten der Person im sozialen Netzwerk ablaufen.  <br/> |
|**fileAs** <br/> |Zeichenfolge, mit der die Person als Kontakt in einer Outlook-Kontaktdatei gespeichert werden soll.  <br/> |
|**firstName** <br/> |Vorname oder Vorname der Person.  <br/> |
|**friendStatus** <br/> |Friend Status dieser Person mit dem angemeldeten Benutzer im sozialen Netzwerk. Muss einer der folgenden Werte sein: **Friend**, nonfriend, **Pending**, pendingin, **Pending**. **** ****  <br/> |
|**fullName** <br/> |Vollständiger Name der Person.  <br/> |
|**Geschlecht** <br/> |Geschlecht der Person. Muss einer der folgenden Werte sein: **männlich**, **weiblich**, nicht **angegeben**.  <br/> |
|**homePhone** <br/> |Private Telefonnummer für die Person.  <br/> |
|**Index** <br/> |Speicherort der gehashten Adresse der Person im _personsAddresses_ -Zeichenfolgenparameter, der an einen Aufruf der **ISocialSession2:: GetPeopleDetails** -Methode übergeben wird. Außerdem wird der Person-XML **** -Code in der __ persons-Zeichenfolge angegeben, die von **GetPeopleDetails**zurückgegeben wird.  <br/> |
|**Branchen** <br/> |Branchen, in denen die Person beschäftigt ist.  <br/> |
|**interests** <br/> |Interessen oder Hobbies der Person.  <br/> |
|**lastModificationTime** <br/> |Zeitpunkt, zu dem das Profil der Person zuletzt im sozialen Netzwerk geändert wurde.  <br/> |
|**lastName** <br/> |Nachname oder Nachname der Person.  <br/> |
|**location** <br/> |Der Speicherort der Person.  <br/> |
|**Spitzname** <br/> |Ein kürzerer oder erfunder Name der Person.  <br/> |
|**otherAddress** <br/> |Alternative Adresse der Person.  <br/> |
|**otherCity** <br/> |Stadt der alternativen Adresse der Person.  <br/> |
|**otherCountryOrRegion** <br/> |Land oder Region der alternativen Adresse der Person.  <br/> |
|**otherState** <br/> |Bundesland oder Kanton der alternativen Adresse der Person.  <br/> |
|**otherZip** <br/> |Postleitzahl der alternativen Adresse der Person.  <br/> |
|**Telefon** <br/> |Primäre Telefonnummer des Kontakts für die Person.  <br/> |
|**pictureUrl** <br/> |URL für ein Profilbild der Person.  <br/> |
|**Beziehung** <br/> |Beziehung dieser Person mit dem angemeldeten Benutzer.  <br/> |
|**Schulen** <br/> |Die Schulen, die die Person besucht oder besucht hat.  <br/> |
|**skills** <br/> |Persönliche Fähigkeiten der Person.  <br/> |
|**state** <br/> |Bundesland oder Kanton der physischen Adresse der Person.  <br/> |
|**title** <br/> |Die Bezeichnung wurde dem Namen der Person hinzugefügt.  <br/> |
|**userID** <br/> |ID, um die Person im sozialen Netzwerk zu identifizieren.  <br/> |
|**webProfilePage** <br/> |Die Webseitenadresse, die ein Profil der Person enthält.  <br/> |
|**Website** <br/> |Die Website der Person.  <br/> |
|**workPhone** <br/> |Geschäftliche Telefonnummer für die Person.  <br/> |
|**ZIP** <br/> |Postleitzahl der physischen Adresse der Person.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [XML-Beispiel für Freunde](friends-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Funktionen](xml-for-capabilities.md) 
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

