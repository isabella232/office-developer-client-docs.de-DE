---
title: XML für „friends“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Das Friends-Element im MICROSOFT Outlook Social Connector (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook-Benutzer im sozialen Netzwerk zugeordnet sind.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361159"
---
# <a name="xml-for-friends"></a>XML für „friends“

Das **Friends-Element** im MICROSOFT Outlook Social Connector (OSC)-Anbieter-XML-Schema ermöglicht es einem OSC-Anbieter, Informationen für eine Liste von Personen anzugeben, die einem Outlook-Benutzer im sozialen Netzwerk zugeordnet sind. Wenn der OSC-Anbieter die zwischengespeicherte Synchronisierung unterstützt, enthält diese Personenliste nur Freunde Outlook Benutzer im sozialen Netzwerk. Wenn das OSC die On-Demand- oder Hybridsynchronisierung unterstützt, kann diese Liste sowohl Freunde als auch Nicht-Freunde des benutzers Outlook enthalten. 

Jede Person in der Liste  wird im XML-Schema als Personelement dargestellt, das Details wie Vorname, Nachname und E-Mail-Adressen unterstützt. OsC-Anbieter verwenden die **Elemente "Freunde"** und **"Person",** unabhängig davon, wie das OSC Freundesinformationen aus dem sozialen Netzwerk synchronisieren soll. Beachten Sie, dass  die untergeordneten Elemente einer Person einigen Eigenschaften eines Outlook-Kontakts ähneln, wodurch das Speichern von Freunden in einem Outlook-Kontaktordner für das soziale Netzwerk erleichtert wird, wenn das soziale Netzwerk zwischengespeicherte oder hybride Synchronisierung von Freunden mit einem Outlook-Kontaktordner unterstützt. 

## <a name="example-scenarios"></a>Beispielszenarien

Die folgenden Beispielszenarien zeigen die OsC-Anbieter-Erweiterungs-API-Aufrufe, die von einem OSC-Anbieter implementiert werden, und die OSC macht, um Freundesinformationen zu erhalten. Informationen werden in XML-Zeichenfolgen ausgedrückt, die dem XML-Schema des OSC-Anbieters entsprechen.
  
Ein Beispiel für friends XML finden Sie unter [Friends XML Example](friends-xml-example.md). Weitere Informationen zum Synchronisieren von Informationen zu Freunden finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Szenario 1: Erhalten einer Liste von Freunden

Szenario 1: OSC ruft eine Liste von Freunden sowie ein [ISocialPerson-Objekt](isocialpersoniunknown.md) und ein Bild für jeden Freund ab: 
    
1. Ein OSC-Anbieter, der das Anzeigen von Freunden vom Standort des sozialen Netzwerks unterstützt und dem OSC das Zwischenspeichern von Freundesinformationen ermöglicht, weist darauf hin, dass dem OSC die **GetFriends-** und **cacheFriends-Elemente** verwendet werden, die untergeordnete Elemente des **Capabilities-Elements** sind. 
    
2. Der OSC-Anbieter implementiert außerdem die [Methoden ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)und [ISocialPerson::GetPicture.](isocialperson-getpicture.md) 
    
3. Das OSC ruft **ISocialProvider::GetCapabilities** auf, um den Wert der folgenden Elemente zu überprüfen: **getFriends,** um zu überprüfen, ob der OSC-Anbieter das Anzeigen von Freunden aus dem sozialen Netzwerk unterstützt, und **cacheFriends,** um zu überprüfen, ob der Anbieter das Zwischenspeichern von Freunden unterstützt. 
    
4. Das OSC ruft **ISocialSession::GetPerson auf,** um ein **ISocialPerson-Objekt** für den benutzer Outlook erhalten. 
    
5. Das OSC ruft **ISocialPerson::GetFriendsAndColleagues** auf, um die Freundesliste des Outlook-Benutzers in der _parameterzeichenfolge personCollection_ zurück zu erhalten. Die  _personCollection-Zeichenfolge_ entspricht der XML-Schemadefinition für das **friends-Element** im XML-Schema. 
    
6. Für jeden Freund  in der personCollection-XML-Zeichenfolge ruft das OSC den Wert des **userID-Elements** ab, um **ISocialSession::GetPerson** auf aufruft, um ein **ISocialPerson-Objekt** für diesen Freund zu erhalten. 
    
7. Für jeden Freund  in der personCollection-XML-Zeichenfolge ruft das OSC [ISocialPerson::GetPicture](isocialperson-getpicture.md) auf, um eine Bildressource für diesen Freund zu erhalten. 
    
   Das OSC kann weitere Aufrufe an das **ISocialPerson-Objekt** senden, um Aktivitäten und Details (z. B. E-Mail-Adressen) für diesen Freund zu erhalten. 
    
### <a name="scenario-2-synchronize-friends"></a>Szenario 2: Synchronisieren von Freunden 

Szenario 2: OSC synchronisiert Freunde dynamisch:
    
1. Ein OSC-Anbieter, der die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt, gibt dies mithilfe der **Elemente getFriends** und **dynamicContactsLookup** an das OSC an. Der #A0 legt auch das **hashFunction-Element** fest. Alle drei Elemente sind untergeordnete Elemente von **Funktionen.** 
    
2. Der #A0 implementiert auch die [ISocialSession2::GetPeopleDetails-Methode.](isocialsession2-getpeopledetails.md) 
    
3. Das OSC ruft **ISocialProvider::GetCapabilities** auf, um die Werte von **getFriends** und **dynamicContactsLookup** zu überprüfen, um sicherzustellen, dass der OSC-Anbieter Freunde und die on-demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt. Das OSC notieren auch den Wert der **hashFunction,** die vom #A0 unterstützt wird. 
    
4. Für jeden Benutzer, der im Personenbereich angezeigt wird, erfasst das OSC die E-Mail-Adresse des Benutzers und verschlüsselt sie mithilfe der hash-Funktion, die in **hashFunction angegeben ist.** Dadurch wird eine #A0 erstellt, die der #A1 für das **HashedAddresses-Element** entspricht. 
    
5. Das OSC ruft **ISocialSession2::GetPeopleDetails auf** und stellt diese #A0 mit Hashadressen als  _personAddresses-Parameter_ zur verfügung, um dynamisch aktualisierte Details für Personen im  _parameter personsCollection zu_ erhalten. Die  _Zeichenfolge des personsCollection-Parameters_ entspricht der XML-Schemadefinition für das **friends-Element** im XML-Schema. 

## <a name="parent-and-child-elements"></a>Übergeordnete und untergeordnete Elemente

Im Folgenden finden Sie die beiden Elemente auf oberster Ebene im **Freundesschema.** 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**friends** <br/> |Stellt das Stammelement einer Liste von **Personenelementen** dar. Die **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)und **ISocialSession2::GetPeopleDetails** geben #A0 zurück, die der Schemadefinition des **friends-Elements** entsprechen.  <br/> |
|**Person** <br/> |Stellt eine Person in einer Liste von **Personenelementen** dar. Die [ISocialPerson::GetDetails-Methode](isocialperson-getdetails.md) gibt eine #A0 zurück, die der Schemadefinition des **Person-Elements** entspricht.  <br/> |
   
In der folgenden Tabelle werden alle untergeordneten Elemente des **Person-Elements** im XML-Schema des OSC-Anbieters beschrieben. 
  
Eine vollständige Definition des XML-Schemas des OSC-Anbieters, einschließlich der erforderlichen oder optionalen Elemente, finden Sie unter [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**address** <br/> |Physische Straßenadresse der Person.  <br/> |
|**anniversary** <br/> |Jubiläumsdatum für ein Ereignis für die Person.  <br/> |
|**askmeabout** <br/> |Themen von Interesse oder Fachwissen der Person.  <br/> |
|**birthday** <br/> |Geburtsdatum der Person.  <br/> |
|**businessAddress** <br/> |Physische Straßenadresse des Arbeitsplatzes der Person.  <br/> |
|**businessCity** <br/> |Ort für den Arbeitsplatz der Person.  <br/> |
|**businessCountryOrRegion** <br/> |Land oder Region des Arbeitsplatzes der Person.  <br/> |
|**businessState** <br/> |Bundesland oder Kanton des Arbeitsplatzes der Person.  <br/> |
|**businessZip** <br/> |Postleitzahl oder Postleitzahl des Arbeitsplatzes der Person.  <br/> |
|**Zelle** <br/> |Mobiltelefonnummer für die Person.  <br/> |
|**Ort** <br/> |Ort der physischen Adresse für die Person.  <br/> |
|**company** <br/> |Name des Unternehmens, das der Person zugeordnet ist.  <br/> |
|**countryOrRegion** <br/> |Land oder Region der physischen Adresse der Person.  <br/> |
|**creationTime** <br/> |Erstellungszeit des Profils der Person im sozialen Netzwerk.  <br/> |
|**emailAddress** <br/> |Primäre E-Mail-Adresse der Person.  <br/> |
|**emailAddress2** <br/> |Sekundäre E-Mail-Adresse der Person.  <br/> |
|**emailAddress3** <br/> |Tertiäre E-Mail-Adresse der Person.  <br/> |
|**expirationTime** <br/> |Zeit, zu der die Profildaten der Person im sozialen Netzwerk ablaufen.  <br/> |
|**fileAs** <br/> |Zeichenfolge, mit der die Person als Kontakt in einer Kontaktdatei Outlook werden soll.  <br/> |
|**firstName** <br/> |Vorname oder Vorname der Person.  <br/> |
|**friendStatus** <br/> |Der Freundesstatus dieser Person mit dem angemeldeten Benutzer im sozialen Netzwerk. Muss einer der folgenden Werte sein: **friend**, **nonfriend**, **pending**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Vollständiger Name der Person.  <br/> |
|**gender** <br/> |Geschlecht der Person. Muss einer der folgenden Werte sein: **männlich**, **weiblich**, **nicht angegeben.**  <br/> |
|**homePhone** <br/> |Privattelefonnummer für die Person.  <br/> |
|**Index** <br/> |Speicherort der Hashadresse der Person im  _zeichenfolgenparameter personsAddresses,_ der an einen Aufruf der **ISocialSession2::GetPeopleDetails-Methode übergeben** wird. Außerdem wird der #A0 der Person in der _personCollection-Zeichenfolge_ angegeben, die von **GetPeopleDetails zurückgegeben wird.**   <br/> |
|**branchen** <br/> |Branchen, in die die Person tätig ist.  <br/> |
|**interests** <br/> |Interessen oder Hobbys der Person.  <br/> |
|**lastModificationTime** <br/> |Zeitpunkt, zu dem das Profil der Person zuletzt im sozialen Netzwerk geändert wurde.  <br/> |
|**lastName** <br/> |Nachname oder Nachname der Person.  <br/> |
|**location** <br/> |Der Ort der Person.  <br/> |
|**nickname** <br/> |Ein kürzerer Name oder der Name der Person.  <br/> |
|**otherAddress** <br/> |Alternative Straßenadresse der Person.  <br/> |
|**otherCity** <br/> |Ort der alternativen Adresse der Person.  <br/> |
|**otherCountryOrRegion** <br/> |Land oder Region der alternativen Adresse der Person.  <br/> |
|**otherState** <br/> |Bundesland oder Kanton der alternativen Adresse der Person.  <br/> |
|**otherZip** <br/> |Postleitzahl oder Postleitzahl der alternativen Adresse der Person.  <br/> |
|**phone** <br/> |Primäre Kontakttelefonnummer für die Person.  <br/> |
|**pictureUrl** <br/> |URL für ein Profilbild der Person.  <br/> |
|**beziehung** <br/> |Beziehung dieser Person mit dem angemeldeten Benutzer.  <br/> |
|**schools** <br/> |Die Schulen, in die die Person geht oder zu der sie gegangen ist.  <br/> |
|**skills** <br/> |Persönliche Fähigkeiten der Person.  <br/> |
|**state** <br/> |Bundesland oder Kanton der physischen Adresse der Person.  <br/> |
|**title** <br/> |Bezeichnung, die dem Namen der Person hinzugefügt wurde.  <br/> |
|**userID** <br/> |ID, um die Person im sozialen Netzwerk zu identifizieren.  <br/> |
|**webProfilePage** <br/> |Webseite-Adresse, die ein Profil der Person enthält.  <br/> |
|**website** <br/> |Die Website der Person.  <br/> |
|**workPhone** <br/> |Geschäftstelefonnummer für die Person.  <br/> |
|**zip** <br/> |Postleitzahl oder Postleitzahl der physischen Adresse der Person.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Friends-XML-Beispiel](friends-xml-example.md)  
- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md)  
- [XML für Funktionen](xml-for-capabilities.md) 
- [XML für Aktivitäten](xml-for-activities.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

