---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten aller vom HashedAddresses-Parameter angegebenen Benutzer darstellt.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795998"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="b5aec-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="b5aec-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="b5aec-104">Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten aller vom _HashedAddresses_ -Parameter angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5aec-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="b5aec-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5aec-105">Parameters</span></span>

<span data-ttu-id="b5aec-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="b5aec-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="b5aec-107">[in] Eine Struktur, die gibt ein Array von Hash SMTP-Adressen für eine Gruppe von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="b5aec-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="b5aec-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="b5aec-108">_startTime_</span></span>
  
> <span data-ttu-id="b5aec-109">[in] Der Zeitpunkt, nach dem erstellten Aktivitäten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b5aec-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="b5aec-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="b5aec-110">_activities_</span></span>
  
> <span data-ttu-id="b5aec-111">[out] Eine XML-Zeichenfolge, die den Satz von Aktivitäten durch _HashedAddresses_ im sozialen Netzwerk seit _StartTime_angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5aec-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5aec-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5aec-112">Remarks</span></span>

<span data-ttu-id="b5aec-113">Die OSC **GetActivitiesEx** aufgerufen, wenn der OSC-Anbieter bedarfsgesteuerten Synchronisierung von Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5aec-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="b5aec-114">Die OSC speichert die Informationen, die in _Aktivitäten_ im Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5aec-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="b5aec-115">Weitere Informationen darüber, wie die OSC verwendet und diese Informationen im Speicher aktualisiert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="b5aec-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="b5aec-116">Outlook Social Connector 2013 ab, der OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und ruft nur **GetActivitiesEx** um Aktivitäten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5aec-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="b5aec-117">Legen Sie zur Unterstützung der Aktivitäten auf Abruf Lookup **CacheActivities** , wie **"false"**, und **GetActivities** und **DynamicActivitiesLookupEx** als **true**und die OSC **GetActivitiesEx**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b5aec-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="b5aec-118">Die zurückgegebene XML-Zeichenfolge muss die Schemadefinition für **ActivityFeed**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b5aec-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="b5aec-119">Die Zeichenfolge _HashedAddresses_ stellt einen Satz von Hash Adressen für jeden Benutzer im Bereich Personen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5aec-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="b5aec-120">Hash SMTP-Adressen werden mithilfe der vom **HashFunction** -Element in der Anbieter **Funktionen** XML angegebenen Hashfunktion verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="b5aec-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="b5aec-121">Der Benutzer hat keinen Friend der angemeldete Benutzer von der [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5aec-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="b5aec-122">Der Parameter _StartTime_ ist **ein Datumswert in koordinierter Weltzeit (UTC)** .</span><span class="sxs-lookup"><span data-stu-id="b5aec-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b5aec-123">Ortszeit Werte müssen in UTC **Datum** konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5aec-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="b5aec-124">Aktivitäten, die die **GetActivitiesEx** -Methode gibt benötigen einen Erstellung Time-Wert, der _Werte von StartTime_ größer ist kleiner oder gleich **jetzt**.</span><span class="sxs-lookup"><span data-stu-id="b5aec-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="b5aec-125">Wenn keine Änderungen zwischen **StartTime** und **jetzt**aufgetreten sind, muss der Anbieter einen OSC_E_NO_CHANGES Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b5aec-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5aec-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5aec-126">See also</span></span>

- [<span data-ttu-id="b5aec-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5aec-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="b5aec-128">Synchronisieren von Freunde und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="b5aec-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

