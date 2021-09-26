---
title: XML-Beispiel für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die ISocialProvider::GetCapabilities-Methode für ein soziales Netzwerk aufgerufen wurde. Der XML-Code zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für osc angibt.
ms.openlocfilehash: 7ab0e08739e77964fcea4874e2422d12c65d753a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608914"
---
# <a name="capabilities-xml-example"></a>XML-Beispiel für „capabilities“

Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) für ein soziales Netzwerk aufgerufen wurde. Der XML-Code zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für osc angibt. 
  
## <a name="capabilities-for-friends"></a>Funktionen für Freunde

In diesem Beispiel gibt der OSC-Anbieter die folgenden Elemente an, um seine Funktionen zur Unterstützung des Freunde-Features anzuzeigen:
  
- **getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically. 
    
- **cacheFriends** as **true** to support caching friends's information in an Outlook contacts folder. 
    
- **contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes. 
    
- **followPerson** as **true** to indicate the ability to add friends on the social network. 
    
- **doNotFollowPerson** als **"false",** um anzugeben, dass der OSC-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt. 
    
- **dynamicContactsLookup** als **"false",** um anzugeben, dass der OSC die Informationen von Freunden nicht im Speicher speichern sollte. 
    
## <a name="capabilities-for-activities"></a>Funktionen für Aktivitäten

Der OSC-Anbieter gibt die folgenden Elemente an, um seine Fähigkeit zur Unterstützung von Aktivitäten anzuzeigen:
  
- **getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends'activities programmatically. 
    
- **cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder. 
    
- **dynamicActivitiesLookupEx** als **"true",** um anzugeben, dass der OSC die Aktivitäten von Freunden im Speicher speichern soll. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Funktionen für Authentifizierung und Kontokonfiguration

Der OSC-Anbieter gibt die folgenden Elemente an, um die Unterstützung für die Authentifizierung und Kontokonfiguration anzuzeigen:
  
- **useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication. 
    
- **supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on the social network for the user. 
    
- **useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on. 
    
- **displayUrl** als **"false",** um anzugeben, dass der OSC die URL für das soziale Netzwerk nicht im Dialogfeld "Kontokonfiguration" anzeigen soll. 
    
- **hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box. 
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die **Funktions-XML** eines OSC-Anbieters. 
  
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
- [Xml-Beispiel für Freunde](friends-xml-example.md)  
- [Beispiel für Aktivitätsfeed-XML](activity-feed-xml-example.md)  
- [Outlook XML-Schema des Connectoranbieters für soziale Netzwerke](outlook-social-connector-provider-xml-schema.md)

