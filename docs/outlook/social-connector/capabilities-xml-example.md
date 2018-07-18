---
title: XML-Beispiel für „capabilities“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: Das XML-Beispiel in diesem Thema wird eine XML-Zeichenfolge an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die ISocialProvider::GetCapabilities-Methode für ein social Network ruft. Der XML-Code zeigt, wie ein OSC-Anbieter die Funktionen und Anforderungen für das osc bilden angibt.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795958"
---
# <a name="capabilities-xml-example"></a>XML-Beispiel für „capabilities“

Das XML-Beispiel in diesem Thema wird eine XML-Zeichenfolge an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode für ein social Network ruft. Der XML-Code zeigt, wie ein OSC-Anbieter die Funktionen und Anforderungen für das osc bilden angibt. 
  
## <a name="capabilities-for-friends"></a>Funktionen für Freunde

In diesem Beispiel gibt den OSC-Anbieter seine Funktionen in die Unterstützung für des Features Freunde anzeigen, um die folgenden Elemente:
  
- **GetFriends** als **true** an, dass der OSC-Anbieter unterstützt die [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode zum programmgesteuerten Abrufen von Informationen von Freunden. 
    
- **CacheFriends** als **true** zur Unterstützung der Zwischenspeichern Freunde Informationen in einem Outlook-Kontakteordner. 
    
- **ContactSyncRestartInterval** als 60 bis auf um anzugeben, dass, sollte die OSC wiederholen Aktualisieren des Caches 60 Minuten. 
    
- **FollowPerson** als **true** an, dass die Möglichkeit, Freunde im sozialen Netzwerk hinzuzufügen. 
    
- das Ausschließen einer Person als Freund im sozialen Netzwerk **DoNotFollowPerson** als **false** an, dass der OSC-Anbieter nicht unterstützt. 
    
- **DynamicContactsLookup** als **false,** um anzugeben, dass die OSC keine Freunde im Arbeitsspeicher gespeichert werden soll. 
    
## <a name="capabilities-for-activities"></a>Funktionen für Aktivitäten

Der OSC-Anbieter gibt die folgenden Elemente, um die Funktion zur Unterstützung von Aktivitäten anzuzeigen:
  
- **GetActivities** als **true,** um anzugeben, dass der OSC-Anbieter die [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) -Methode zum programmgesteuerten Abrufen Freunde Aktivitäten unterstützt. 
    
- **CacheActivities** als **false** zur Unterstützung der Zwischenspeichern Aktivitäten Freunde in den ausgeblendeten Newsfeed Outlook-Ordner. 
    
- **DynamicActivitiesLookupEx** als **true,** um anzugeben, dass die OSC Freunde Aktivitäten im Arbeitsspeicher gespeichert werden sollte. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Funktionen für die Authentifizierung und Konto-Konfiguration

Der OSC-Anbieter gibt die folgenden Elemente, um die Unterstützung für die Authentifizierung und Kontokonfiguration anzuzeigen:
  
- **UseLogonWebAuth** als **false,** um anzugeben, dass der OSC-Anbieter Standardauthentifizierung unterstützt. 
    
- **SupportsAutoConfigure** als **false,** um anzugeben, dass die OSC nicht automatisch konfiguriert und melden Sie sich an dem sozialen Netzwerk für den Benutzer versuchen soll. 
    
- die zwischengespeicherten Anmeldeinformationen zur Anmeldung bei **UseLogonCached** und **HideRememberMyPassword** als **false** um anzugeben, dass die OSC Kennwort jedes Mal anfordern soll und nicht verwendet werden sollte. 
    
- **DisplayUrl** als **false,** um anzugeben, dass die URL für das soziale Netzwerk von der OSC nicht im Dialogfeld Konfiguration Konto angezeigt werden soll. 
    
- **HideHyperlinks** als **false,** um anzugeben, dass der OSC-Anbieter nur vorhandene Konten mit bekannten Kennwörter unterstützt und die OSC nicht angezeigt werden, **Klicken Sie hier, um ein Konto erstellen sollen** und **Kennwort vergessen?** Hyperlinks in der im Dialogfeld Konto-Konfiguration. 
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die **Funktionen** der XML-Daten des einem OSC-Anbieter. 
  
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Siehe auch

- [OSC-Anbieter XML-Beispielen](osc-provider-xml-examples.md)  
- [XML-Code für Funktionen](xml-for-capabilities.md)  
- [Freunde XML-Beispiel](friends-xml-example.md)  
- [Beispiel für eine Aktivität Feed XML](activity-feed-xml-example.md)  
- [Outlook Connector für soziale Netzwerke Anbieter XML-Schema](outlook-social-connector-provider-xml-schema.md)

