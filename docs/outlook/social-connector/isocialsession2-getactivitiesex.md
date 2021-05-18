---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den HashedAddresses-Parameter angegeben werden.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404337"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="1663b-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="1663b-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="1663b-104">Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der einzelnen Benutzer darstellt, die durch den  _HashedAddresses-Parameter angegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="1663b-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="1663b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1663b-105">Parameters</span></span>

<span data-ttu-id="1663b-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="1663b-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="1663b-107">[in] Eine Struktur, die ein Array mit #A0 mit Hash für eine Gruppe von Benutzern angibt.</span><span class="sxs-lookup"><span data-stu-id="1663b-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="1663b-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="1663b-108">_startTime_</span></span>
  
> <span data-ttu-id="1663b-109">[in] Die Zeit, nach der die erstellten Aktivitäten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1663b-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="1663b-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="1663b-110">_activities_</span></span>
  
> <span data-ttu-id="1663b-111">[out] Eine XML-Zeichenfolge, die den Satz von Aktivitäten der Benutzer darstellt, die von _hashedAddresses_ im sozialen Netzwerk seit _startTime angegeben werden._</span><span class="sxs-lookup"><span data-stu-id="1663b-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1663b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1663b-112">Remarks</span></span>

<span data-ttu-id="1663b-113">Das OSC ruft **GetActivitiesEx auf,** wenn der OSC-Anbieter die On-Demand-Synchronisierung von Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1663b-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="1663b-114">Das OSC speichert die in Aktivitäten zurückgegebenen  _Informationen_ im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1663b-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="1663b-115">Weitere Informationen dazu, wie das OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="1663b-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="1663b-116">Ab Outlook Social Connector 2013 unterstützt das OSC nur die On-Demand-Synchronisierung von Aktivitäten und ruft **nur GetActivitiesEx** auf, um Aktivitäten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1663b-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="1663b-117">Legen Sie **cacheActivities** als **false** und **getActivities** und **dynamicActivitiesLookupEx** als **true** vor, um die Suche nach On-Demand-Aktivitäten zu unterstützen, und das OSC wird **GetActivitiesEx aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="1663b-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="1663b-118">Die zurückgegebene XML-Zeichenfolge muss der Schemadefinition für **activityFeed** entsprechen, wie im Schema für die Erweiterbarkeit des OSC-Anbieters definiert.</span><span class="sxs-lookup"><span data-stu-id="1663b-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="1663b-119">Der  _HashedAddresses-Sring_ stellt eine Gruppe von Hashadressen für jeden Benutzer dar, der im Personenbereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1663b-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="1663b-120">Die #A0 mit Hash werden mithilfe der hashing-Funktion verschlüsselt, die durch das **hashFunction-Element** in der #A1 des **Anbieters angegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="1663b-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="1663b-121">Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession::LoggedOnUserName-Eigenschaft dargestellt](isocialsession-loggedonusername.md) wird.</span><span class="sxs-lookup"><span data-stu-id="1663b-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="1663b-122">Der  _parameter startTime_ ist ein **Date-Wert** in koordinierter Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="1663b-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1663b-123">Ortszeitwerte müssen in **UTC-Datumswerte konvertiert** werden.</span><span class="sxs-lookup"><span data-stu-id="1663b-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="1663b-124">Aktivitäten, die die **GetActivitiesEx-Methode** zurückgibt, müssen einen Erstellungszeitwert haben, der größer als _startTime_ und kleiner als oder gleich **Now ist.**</span><span class="sxs-lookup"><span data-stu-id="1663b-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="1663b-125">Wenn zwischen **startTime** und **Now** keine Änderungen vorgenommen wurden, muss der Anbieter einen Fehler OSC_E_NO_CHANGES zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1663b-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1663b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1663b-126">See also</span></span>

- [<span data-ttu-id="1663b-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1663b-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="1663b-128">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="1663b-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

