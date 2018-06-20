---
title: Funktionen XML-Beispiel
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
# <a name="capabilities-xml-example"></a><span data-ttu-id="d6b4b-104">Funktionen XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6b4b-104">Capabilities XML example</span></span>

<span data-ttu-id="d6b4b-105">Das XML-Beispiel in diesem Thema wird eine XML-Zeichenfolge an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode für ein social Network ruft.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="d6b4b-106">Der XML-Code zeigt, wie ein OSC-Anbieter die Funktionen und Anforderungen für das osc bilden angibt.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="d6b4b-107">Funktionen für Freunde</span><span class="sxs-lookup"><span data-stu-id="d6b4b-107">Capabilities for friends</span></span>

<span data-ttu-id="d6b4b-108">In diesem Beispiel gibt den OSC-Anbieter seine Funktionen in die Unterstützung für des Features Freunde anzeigen, um die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d6b4b-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="d6b4b-109">**GetFriends** als **true** an, dass der OSC-Anbieter unterstützt die [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode zum programmgesteuerten Abrufen von Informationen von Freunden.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="d6b4b-110">**CacheFriends** als **true** zur Unterstützung der Zwischenspeichern Freunde Informationen in einem Outlook-Kontakteordner.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="d6b4b-111">**ContactSyncRestartInterval** als 60 bis auf um anzugeben, dass, sollte die OSC wiederholen Aktualisieren des Caches 60 Minuten.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="d6b4b-112">**FollowPerson** als **true** an, dass die Möglichkeit, Freunde im sozialen Netzwerk hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="d6b4b-113">das Ausschließen einer Person als Freund im sozialen Netzwerk **DoNotFollowPerson** als **false** an, dass der OSC-Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="d6b4b-114">**DynamicContactsLookup** als **false,** um anzugeben, dass die OSC keine Freunde im Arbeitsspeicher gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="d6b4b-115">Funktionen für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="d6b4b-115">Capabilities for activities</span></span>

<span data-ttu-id="d6b4b-116">Der OSC-Anbieter gibt die folgenden Elemente, um die Funktion zur Unterstützung von Aktivitäten anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="d6b4b-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="d6b4b-117">**GetActivities** als **true,** um anzugeben, dass der OSC-Anbieter die [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) -Methode zum programmgesteuerten Abrufen Freunde Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="d6b4b-118">**CacheActivities** als **false** zur Unterstützung der Zwischenspeichern Aktivitäten Freunde in den ausgeblendeten Newsfeed Outlook-Ordner.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="d6b4b-119">**DynamicActivitiesLookupEx** als **true,** um anzugeben, dass die OSC Freunde Aktivitäten im Arbeitsspeicher gespeichert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="d6b4b-120">Funktionen für die Authentifizierung und Konto-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d6b4b-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="d6b4b-121">Der OSC-Anbieter gibt die folgenden Elemente, um die Unterstützung für die Authentifizierung und Kontokonfiguration anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="d6b4b-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="d6b4b-122">**UseLogonWebAuth** als **false,** um anzugeben, dass der OSC-Anbieter Standardauthentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="d6b4b-123">**SupportsAutoConfigure** als **false,** um anzugeben, dass die OSC nicht automatisch konfiguriert und melden Sie sich an dem sozialen Netzwerk für den Benutzer versuchen soll.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="d6b4b-124">die zwischengespeicherten Anmeldeinformationen zur Anmeldung bei **UseLogonCached** und **HideRememberMyPassword** als **false** um anzugeben, dass die OSC Kennwort jedes Mal anfordern soll und nicht verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="d6b4b-125">**DisplayUrl** als **false,** um anzugeben, dass die URL für das soziale Netzwerk von der OSC nicht im Dialogfeld Konfiguration Konto angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="d6b4b-126">**HideHyperlinks** als **false,** um anzugeben, dass der OSC-Anbieter nur vorhandene Konten mit bekannten Kennwörter unterstützt und die OSC nicht angezeigt werden, **Klicken Sie hier, um ein Konto erstellen sollen** und **Kennwort vergessen?** Hyperlinks in der im Dialogfeld Konto-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="d6b4b-127">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6b4b-127">XML example</span></span>

<span data-ttu-id="d6b4b-128">Das folgende Beispiel zeigt die **Funktionen** der XML-Daten des einem OSC-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d6b4b-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="d6b4b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6b4b-129">See also</span></span>

- [<span data-ttu-id="d6b4b-130">OSC-Anbieter XML-Beispielen</span><span class="sxs-lookup"><span data-stu-id="d6b4b-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="d6b4b-131">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="d6b4b-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="d6b4b-132">Freunde XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6b4b-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="d6b4b-133">Beispiel für eine Aktivität Feed XML</span><span class="sxs-lookup"><span data-stu-id="d6b4b-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="d6b4b-134">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d6b4b-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

