---
title: XML-Beispiel für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Social Connector (OSC) zurückgegeben wird, nachdem die ISocialProvider::GetCapabilities-Methode für ein soziales Netzwerk aufruft. Die XML zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für das OSC angibt.
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542261"
---
# <a name="capabilities-xml-example"></a>XML-Beispiel für „capabilities“

Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Social Connector (OSC) zurückgegeben wird, nachdem die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) für ein soziales Netzwerk aufruft. Die XML zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für das OSC angibt. 
  
## <a name="capabilities-for-friends"></a>Funktionen für Freunde

In diesem Beispiel gibt der OSC-Anbieter die folgenden Elemente an, um seine Funktionen bei der Unterstützung des Freundesfeatures zu zeigen:
  
- **getFriends** als **true,** um anzugeben, dass der OSC-Anbieter die [ISocialPerson::GetFriendsAndColleagues-Methode](isocialperson-getfriendsandcolleagues.md) unterstützt, um die Informationen von Freunden programmgesteuert zu erhalten. 
    
- **cacheFriends** als **true,** um das Zwischenspeichern von Informationen von Freunden in einem Outlook zu unterstützen. 
    
- **contactSyncRestartInterval** als 60, um anzugeben, dass das OSC bei einem Fehler alle 60 Minuten erneut versuchen sollte, den Cache zu aktualisieren. 
    
- **followPerson** als **true,** um die Möglichkeit anzugeben, Freunde im sozialen Netzwerk hinzuzufügen. 
    
- **doNotFollowPerson** als **false,** um anzugeben, dass der OSC-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt. 
    
- **dynamicContactsLookup** als **false,** um anzugeben, dass das OSC keine Freundesinformationen im Speicher speichern soll. 
    
## <a name="capabilities-for-activities"></a>Funktionen für Aktivitäten

Der OsC-Anbieter gibt die folgenden Elemente an, um seine Fähigkeit zur Unterstützung von Aktivitäten zu zeigen:
  
- **getActivities** as **true,** um anzugeben, dass der OSC-Anbieter die [ISocialProfile::GetActivitiesOfFriendsAndColleagues-Methode](isocialprofile-getactivitiesoffriendsandcolleagues.md) unterstützt, um die Aktivitäten von Freunden programmgesteuert zu erhalten. 
    
- **cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder. 
    
- **dynamicActivitiesLookupEx** als **true,** um anzugeben, dass das OSC die Aktivitäten von Freunden im Speicher speichern soll. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Funktionen für die Authentifizierung und Kontokonfiguration

Der OsC-Anbieter gibt die folgenden Elemente an, um seine Unterstützung für die Authentifizierung und Kontokonfiguration zu zeigen:
  
- **useLogonWebAuth** als **false,** um anzugeben, dass der OSC-Anbieter die Standardauthentifizierung unterstützt. 
    
- **supportsAutoConfigure** as **false,** um anzugeben, dass das OSC nicht automatisch konfigurieren und sich beim sozialen Netzwerk für den Benutzer anmelden sollte. 
    
- **useLogonCached** und **hideRememberMyPassword** als **false,** um anzugeben, dass das OSC jedes Mal ein Kennwort einfordern und keine zwischengespeicherten Anmeldeinformationen zum Anmelden verwenden sollte. 
    
- **displayUrl** als **false,** um anzugeben, dass die URL für das soziale Netzwerk im Dialogfeld Kontokonfiguration nicht angezeigt werden soll. 
    
- **hideHyperlinks** als **false,** um anzugeben, dass der OSC-Anbieter nur vorhandene Konten  mit bekannten Kennwörtern unterstützt, und das OSC sollte nicht die Hyperlinks Klicken Sie hier zum Erstellen eines Kontos und **Kennwort vergessen?** im Dialogfeld Kontokonfiguration anzeigen. 
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die **Funktionen-XML** eines OSC-Anbieters. 
  
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

- [OSC-Anbieter-XML-Beispiele](osc-provider-xml-examples.md)  
- [XML für Funktionen](xml-for-capabilities.md)  
- [Friends-XML-Beispiel](friends-xml-example.md)  
- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)  
- [Outlook XML-Schema des Anbieters für sozialen Connector](outlook-social-connector-provider-xml-schema.md)

