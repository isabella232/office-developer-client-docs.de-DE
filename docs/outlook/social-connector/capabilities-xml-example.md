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
# <a name="capabilities-xml-example"></a><span data-ttu-id="ad655-104">XML-Beispiel für „capabilities“</span><span class="sxs-lookup"><span data-stu-id="ad655-104">Capabilities XML example</span></span>

<span data-ttu-id="ad655-105">Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode für ein soziales Netzwerk aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ad655-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="ad655-106">Der XML-Code zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für den OSC angibt.</span><span class="sxs-lookup"><span data-stu-id="ad655-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="ad655-107">Funktionen für Freunde</span><span class="sxs-lookup"><span data-stu-id="ad655-107">Capabilities for friends</span></span>

<span data-ttu-id="ad655-108">In diesem Beispiel gibt der OSC-Anbieter die folgenden Elemente an, um die Funktionen für die Unterstützung des Freundes Features anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="ad655-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="ad655-109">**getfriends** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode unterstützt, um die Informationen von Freunden programmgesteuert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad655-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="ad655-110">**cacheFriends** als **true** , um die Informationen Zwischenspeichern von Freunden in einem Outlook-Kontakteordner zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ad655-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="ad655-111">**contactSyncRestartInterval** as 60 um anzugeben, dass bei Fehler, sollte der osc den cache alle 60 Minuten wiederholen.</span><span class="sxs-lookup"><span data-stu-id="ad655-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="ad655-112">**followPerson** als **true** , um anzugeben, dass Freunde im sozialen Netzwerk hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="ad655-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="ad655-113">**doNotFollowPerson** als **false** , um anzugeben, dass der osc-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad655-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="ad655-114">**dynamicContactsLookup** als **false** , um anzugeben, dass osc keine Freundes Informationen im Arbeitsspeicher speichern soll.</span><span class="sxs-lookup"><span data-stu-id="ad655-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="ad655-115">Funktionen für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="ad655-115">Capabilities for activities</span></span>

<span data-ttu-id="ad655-116">Der OSC-Anbieter gibt die folgenden Elemente an, um die Fähigkeit zur Unterstützung von Aktivitäten anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="ad655-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="ad655-117">**GetActivities** als **true** , um anzugeben, dass der osc-Anbieter die [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) -Methode unterstützt, um die Aktivitäten von Freunden programmgesteuert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad655-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="ad655-118">**cacheActivities** als **false** , um die zwischen Speicherungs Aktivitäten von Freunden im ausgeblendeten Outlook News Feed-Ordner zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ad655-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="ad655-119">**dynamicActivitiesLookupEx** als **true** , um anzugeben, dass osc Aktivitäten von Freunden im Arbeitsspeicher speichern soll.</span><span class="sxs-lookup"><span data-stu-id="ad655-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="ad655-120">Funktionen für Authentifizierung und Kontokonfiguration</span><span class="sxs-lookup"><span data-stu-id="ad655-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="ad655-121">Der OSC-Anbieter gibt die folgenden Elemente an, um die Authentifizierungs-und Kontokonfiguration zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="ad655-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="ad655-122">**useLogonWebAuth** als **false** , um anzugeben, dass der osc-Anbieter die Standardauthentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad655-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="ad655-123">**supportsAutoConfigure** als **false** , um anzugeben, dass osc nicht versuchen soll, das soziale Netzwerk für den Benutzer automatisch zu konfigurieren und sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="ad655-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="ad655-124">**useLogonCached** und **hideRememberMyPassword** als **false** , um anzugeben, dass der osc jedes Mal zur Eingabe eines Kennworts aufgefordert werden soll und keine zwischengespeicherten Anmeldeinformationen zum Anmelden verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad655-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="ad655-125">**displayUrl** als **false** , um anzugeben, dass osc im Dialogfeld Kontokonfiguration nicht die URL für das soziale Netzwerk anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="ad655-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="ad655-126">**hideHyperlinks** als **false** , um anzugeben, dass der osc-Anbieter nur vorhandene Konten mit bekannten Kennwörtern unterstützt, und der osc nicht das **Klicken Sie hier, um ein Konto zu erstellen** und **Ihr Kennwort zu vergessen?** Hyperlinks in der Dialogfeld Kontokonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad655-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="ad655-127">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad655-127">XML example</span></span>

<span data-ttu-id="ad655-128">Das folgende Beispiel zeigt die XML- **Funktionen** eines osc-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="ad655-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ad655-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad655-129">See also</span></span>

- [<span data-ttu-id="ad655-130">OSC-Anbieter-XML-Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad655-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="ad655-131">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad655-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="ad655-132">XML-Beispiel für Freunde</span><span class="sxs-lookup"><span data-stu-id="ad655-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="ad655-133">XML-Beispiel für Aktivitätsfeeds</span><span class="sxs-lookup"><span data-stu-id="ad655-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="ad655-134">XML-Schema des Anbieters für soziale Netzwerke in Outlook</span><span class="sxs-lookup"><span data-stu-id="ad655-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

