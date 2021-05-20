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
# <a name="capabilities-xml-example"></a><span data-ttu-id="abc5a-104">XML-Beispiel für „capabilities“</span><span class="sxs-lookup"><span data-stu-id="abc5a-104">Capabilities XML example</span></span>

<span data-ttu-id="abc5a-105">Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge, die an den Outlook Social Connector (OSC) zurückgegeben wird, nachdem die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) für ein soziales Netzwerk aufruft.</span><span class="sxs-lookup"><span data-stu-id="abc5a-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="abc5a-106">Die XML zeigt, wie ein OSC-Anbieter seine Funktionen und Anforderungen für das OSC angibt.</span><span class="sxs-lookup"><span data-stu-id="abc5a-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="abc5a-107">Funktionen für Freunde</span><span class="sxs-lookup"><span data-stu-id="abc5a-107">Capabilities for friends</span></span>

<span data-ttu-id="abc5a-108">In diesem Beispiel gibt der OSC-Anbieter die folgenden Elemente an, um seine Funktionen bei der Unterstützung des Freundesfeatures zu zeigen:</span><span class="sxs-lookup"><span data-stu-id="abc5a-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="abc5a-109">**getFriends** als **true,** um anzugeben, dass der OSC-Anbieter die [ISocialPerson::GetFriendsAndColleagues-Methode](isocialperson-getfriendsandcolleagues.md) unterstützt, um die Informationen von Freunden programmgesteuert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="abc5a-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="abc5a-110">**cacheFriends** als **true,** um das Zwischenspeichern von Informationen von Freunden in einem Outlook zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abc5a-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="abc5a-111">**contactSyncRestartInterval** als 60, um anzugeben, dass das OSC bei einem Fehler alle 60 Minuten erneut versuchen sollte, den Cache zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abc5a-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="abc5a-112">**followPerson** als **true,** um die Möglichkeit anzugeben, Freunde im sozialen Netzwerk hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="abc5a-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="abc5a-113">**doNotFollowPerson** als **false,** um anzugeben, dass der OSC-Anbieter das Entfernen einer Person als Freund im sozialen Netzwerk nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abc5a-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="abc5a-114">**dynamicContactsLookup** als **false,** um anzugeben, dass das OSC keine Freundesinformationen im Speicher speichern soll.</span><span class="sxs-lookup"><span data-stu-id="abc5a-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="abc5a-115">Funktionen für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="abc5a-115">Capabilities for activities</span></span>

<span data-ttu-id="abc5a-116">Der OsC-Anbieter gibt die folgenden Elemente an, um seine Fähigkeit zur Unterstützung von Aktivitäten zu zeigen:</span><span class="sxs-lookup"><span data-stu-id="abc5a-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="abc5a-117">**getActivities** as **true,** um anzugeben, dass der OSC-Anbieter die [ISocialProfile::GetActivitiesOfFriendsAndColleagues-Methode](isocialprofile-getactivitiesoffriendsandcolleagues.md) unterstützt, um die Aktivitäten von Freunden programmgesteuert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="abc5a-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="abc5a-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span><span class="sxs-lookup"><span data-stu-id="abc5a-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="abc5a-119">**dynamicActivitiesLookupEx** als **true,** um anzugeben, dass das OSC die Aktivitäten von Freunden im Speicher speichern soll.</span><span class="sxs-lookup"><span data-stu-id="abc5a-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="abc5a-120">Funktionen für die Authentifizierung und Kontokonfiguration</span><span class="sxs-lookup"><span data-stu-id="abc5a-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="abc5a-121">Der OsC-Anbieter gibt die folgenden Elemente an, um seine Unterstützung für die Authentifizierung und Kontokonfiguration zu zeigen:</span><span class="sxs-lookup"><span data-stu-id="abc5a-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="abc5a-122">**useLogonWebAuth** als **false,** um anzugeben, dass der OSC-Anbieter die Standardauthentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abc5a-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="abc5a-123">**supportsAutoConfigure** as **false,** um anzugeben, dass das OSC nicht automatisch konfigurieren und sich beim sozialen Netzwerk für den Benutzer anmelden sollte.</span><span class="sxs-lookup"><span data-stu-id="abc5a-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="abc5a-124">**useLogonCached** und **hideRememberMyPassword** als **false,** um anzugeben, dass das OSC jedes Mal ein Kennwort einfordern und keine zwischengespeicherten Anmeldeinformationen zum Anmelden verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="abc5a-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="abc5a-125">**displayUrl** als **false,** um anzugeben, dass die URL für das soziale Netzwerk im Dialogfeld Kontokonfiguration nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abc5a-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="abc5a-126">**hideHyperlinks** als **false,** um anzugeben, dass der OSC-Anbieter nur vorhandene Konten  mit bekannten Kennwörtern unterstützt, und das OSC sollte nicht die Hyperlinks Klicken Sie hier zum Erstellen eines Kontos und **Kennwort vergessen?** im Dialogfeld Kontokonfiguration anzeigen.</span><span class="sxs-lookup"><span data-stu-id="abc5a-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="abc5a-127">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="abc5a-127">XML example</span></span>

<span data-ttu-id="abc5a-128">Das folgende Beispiel zeigt die **Funktionen-XML** eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="abc5a-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="abc5a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc5a-129">See also</span></span>

- [<span data-ttu-id="abc5a-130">OSC-Anbieter-XML-Beispiele</span><span class="sxs-lookup"><span data-stu-id="abc5a-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="abc5a-131">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="abc5a-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="abc5a-132">Friends-XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="abc5a-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="abc5a-133">Beispiel für Aktivitätsfeed-XML</span><span class="sxs-lookup"><span data-stu-id="abc5a-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="abc5a-134">Outlook XML-Schema des Anbieters für sozialen Connector</span><span class="sxs-lookup"><span data-stu-id="abc5a-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

