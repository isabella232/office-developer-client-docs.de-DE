---
title: XML-Beispiel für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an die Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem Sie die ISocialProvider:: getCapabilities-Methode für ein soziales Netzwerk aufgerufen hat. Der XML-Code zeigt, wie ein osc-Anbieter seine Funktionen und Anforderungen für die osc angibt.'
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542261"
---
# <a name="capabilities-xml-example"></a>XML-Beispiel für „capabilities“

Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an die Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem Sie die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode für ein soziales Netzwerk aufgerufen hat. Der XML-Code zeigt, wie ein osc-Anbieter seine Funktionen und Anforderungen für die osc angibt. 
  
## <a name="capabilities-for-friends"></a>Funktionen für Freunde

In diesem Beispiel gibt der osc-Anbieter die folgenden Elemente an, um seine Funktionen zur Unterstützung der Funktion "Friends" anzuzeigen:
  
- **getfriends** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode unterstützt, um Freundes Informationen programmgesteuert abzurufen. 
    
- **cacheFriends** als **true** , um die Zwischenspeicherung von Freunden-Informationen in einem Outlook-Kontaktordner zu unterstützen. 
    
- **contactSyncRestartInterval** als 60, um anzugeben, dass der osc bei einem Fehler alle 60 Minuten wiederholen sollte, um den Cache zu aktualisieren. 
    
- **followPerson** als **true** , um anzugeben, dass Freunde im sozialen Netzwerk hinzugefügt werden können. 
    
- **doNotFollowPerson** als **false** , um anzugeben, dass der osc-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt. 
    
- **dynamicContactsLookup** als **false** , um anzugeben, dass der osc keine Freundes Informationen im Arbeitsspeicher speichern soll. 
    
## <a name="capabilities-for-activities"></a>Funktionen für Aktivitäten

Der osc-Anbieter gibt die folgenden Elemente an, die seine Fähigkeit zur Unterstützung von Aktivitäten zeigen:
  
- **GetActivities** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) -Methode unterstützt, um Aktivitäten von friends programmgesteuert abzurufen. 
    
- **cacheActivities** als **false** , um zwischen Speicherungs Aktivitäten von Freunden im verborgenen Outlook-Nachrichten Feed-Ordner zu unterstützen. 
    
- **dynamicActivitiesLookupEx** als **true** , um anzugeben, dass der osc Aktivitäten von Freunden im Arbeitsspeicher speichern soll. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Funktionen für Authentifizierung und Kontokonfiguration

Der osc-Anbieter gibt die folgenden Elemente an, die seine Unterstützung für Authentifizierung und Kontokonfiguration anzeigen:
  
- **useLogonWebAuth** als **false** , um anzugeben, dass der osc-Anbieter die Standardauthentifizierung unterstützt. 
    
- **supportsAutoConfigure** als **false** , um anzugeben, dass der osc nicht versuchen sollte, sich automatisch beim sozialen Netzwerk für den Benutzer zu konfigurieren und sich anzumelden. 
    
- **useLogonCached** und **hideRememberMyPassword** als **false** , um anzugeben, dass der osc jedes Mal nach einem Kennwort gefragt werden soll und keine zwischengespeicherten Anmeldeinformationen für die Anmeldung verwendet werden soll. 
    
- **displayUrl** als **false** , um anzugeben, dass der osc die URL für das soziale Netzwerk im Dialogfeld Kontokonfiguration nicht anzeigen soll. 
    
- **hideHyperlinks** als **false** , um anzugeben, dass der osc-Anbieter nur vorhandene Konten mit bekannten Kennwörtern unterstützt, und die osc sollte nicht die **Klicken Sie hier, um ein Konto zu erstellen** und **Ihr Kennwort vergessen angezeigt?** Hyperlinks in der Dialogfeld Kontokonfiguration. 
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die XML- **Funktionen** eines osc-Anbieters. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [XML-Beispiele für osc-Anbieter](osc-provider-xml-examples.md)  
- [XML für Funktionen](xml-for-capabilities.md)  
- [XML-Beispiel für Freunde](friends-xml-example.md)  
- [XML-Beispiel für Aktivitätsfeeds](activity-feed-xml-example.md)  
- [Connector für soziale Netzwerke Anbieter-XML-Schema](outlook-social-connector-provider-xml-schema.md)

