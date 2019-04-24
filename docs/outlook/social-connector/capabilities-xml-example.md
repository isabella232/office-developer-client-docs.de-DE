---
title: XML-Beispiel für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die ISocialProvider:: getCapabilities-Methode für ein soziales Netzwerk aufgerufen wurde. Der XML-Code zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für den OSC angibt.'
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281230"
---
# <a name="capabilities-xml-example"></a>XML-Beispiel für „capabilities“

Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode für ein soziales Netzwerk aufgerufen wurde. Der XML-Code zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für den OSC angibt. 
  
## <a name="capabilities-for-friends"></a>Funktionen für Freunde

In diesem Beispiel gibt der OSC-Anbieter die folgenden Elemente an, um die Funktionen für die Unterstützung des Freundes Features anzuzeigen:
  
- **getfriends** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode unterstützt, um die Informationen von Freunden programmgesteuert abzurufen. 
    
- **cacheFriends** als **true** , um die Informationen Zwischenspeichern von Freunden in einem Outlook-Kontakteordner zu unterstützen. 
    
- **contactSyncRestartInterval** as 60 um anzugeben, dass bei Fehler, sollte der osc den cache alle 60 Minuten wiederholen. 
    
- **followPerson** als **true** , um anzugeben, dass Freunde im sozialen Netzwerk hinzugefügt werden können. 
    
- **doNotFollowPerson** als **false** , um anzugeben, dass der osc-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt. 
    
- **dynamicContactsLookup** als **false** , um anzugeben, dass osc keine Freundes Informationen im Arbeitsspeicher speichern soll. 
    
## <a name="capabilities-for-activities"></a>Funktionen für Aktivitäten

Der OSC-Anbieter gibt die folgenden Elemente an, um die Fähigkeit zur Unterstützung von Aktivitäten anzuzeigen:
  
- **GetActivities** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) -Methode unterstützt, um die Aktivitäten von Freunden programmgesteuert abzurufen. 
    
- **cacheActivities** als **false** , um die zwischen Speicherungs Aktivitäten von Freunden im ausgeblendeten Outlook News Feed-Ordner zu unterstützen. 
    
- **dynamicActivitiesLookupEx** als **true** , um anzugeben, dass osc Aktivitäten von Freunden im Arbeitsspeicher speichern soll. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Funktionen für Authentifizierung und Kontokonfiguration

Der OSC-Anbieter gibt die folgenden Elemente an, um die Authentifizierungs-und Kontokonfiguration zu unterstützen:
  
- **useLogonWebAuth** als **false** , um anzugeben, dass der osc-Anbieter die Standardauthentifizierung unterstützt. 
    
- **supportsAutoConfigure** als **false** , um anzugeben, dass osc nicht versuchen soll, das soziale Netzwerk für den Benutzer automatisch zu konfigurieren und sich anzumelden. 
    
- **useLogonCached** und **hideRememberMyPassword** als **false** , um anzugeben, dass der osc jedes Mal zur Eingabe eines Kennworts aufgefordert werden soll und keine zwischengespeicherten Anmeldeinformationen zum Anmelden verwendet werden soll. 
    
- **displayUrl** als **false** , um anzugeben, dass osc im Dialogfeld Kontokonfiguration nicht die URL für das soziale Netzwerk anzeigen soll. 
    
- **hideHyperlinks** als **false** , um anzugeben, dass der osc-Anbieter nur vorhandene Konten mit bekannten Kennwörtern unterstützt, und der osc nicht das **Klicken Sie hier, um ein Konto zu erstellen** und **Ihr Kennwort zu vergessen?** Hyperlinks in der Dialogfeld Kontokonfiguration. 
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die XML- **Funktionen** eines osc-Anbieters. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Siehe auch

- [OSC-Anbieter-XML-Beispiele](osc-provider-xml-examples.md)  
- [XML für Funktionen](xml-for-capabilities.md)  
- [XML-Beispiel für Freunde](friends-xml-example.md)  
- [XML-Beispiel für Aktivitätsfeeds](activity-feed-xml-example.md)  
- [XML-Schema des Anbieters für soziale Netzwerke in Outlook](outlook-social-connector-provider-xml-schema.md)

