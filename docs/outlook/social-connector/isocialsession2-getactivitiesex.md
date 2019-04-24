---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten der einzelnen durch den hashedAddresses-Parameter angegebenen Benutzer darstellt.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336449"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="89bc4-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="89bc4-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="89bc4-104">Ruft eine Zeichenfolge, die eine Auflistung von Aktivitäten der einzelnen durch den _hashedAddresses_ -Parameter angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="89bc4-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="89bc4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="89bc4-105">Parameters</span></span>

<span data-ttu-id="89bc4-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="89bc4-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="89bc4-107">in Eine Struktur, die ein Array von Hash-SMTP-Adressen für eine Gruppe von Benutzern angibt.</span><span class="sxs-lookup"><span data-stu-id="89bc4-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="89bc4-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="89bc4-108">_startTime_</span></span>
  
> <span data-ttu-id="89bc4-109">in Die Zeit, nach der die erstellten Aktivitäten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89bc4-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="89bc4-110">_Aktivitäten_</span><span class="sxs-lookup"><span data-stu-id="89bc4-110">_activities_</span></span>
  
> <span data-ttu-id="89bc4-111">Out Eine XML-Zeichenfolge, die den Satz von Aktivitäten der Benutzer darstellt, die von _hashedAddresses_ im sozialen Netzwerk seit _Startzeit_angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="89bc4-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89bc4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89bc4-112">Remarks</span></span>

<span data-ttu-id="89bc4-113">OSC ruft **GetActivitiesEx** auf, wenn der osc-Anbieter die bedarfsgesteuerte Synchronisierung von Aktivitäten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89bc4-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="89bc4-114">OSC speichert die Informationen, die in _Aktivitäten_ im Arbeitsspeicher zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89bc4-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="89bc4-115">Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="89bc4-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="89bc4-116">Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und ruft nur **GetActivitiesEx** zum Abrufen von Aktivitäten auf.</span><span class="sxs-lookup"><span data-stu-id="89bc4-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="89bc4-117">Zur Unterstützung der Suche nach Anforderungs Aktivitäten legen Sie **cacheActivities** als **false**, und GetActivities und **dynamicActivitiesLookupEx** als **true**fest, und der osc ruft **GetActivitiesEx**auf. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="89bc4-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="89bc4-118">Die zurückgegebene XML-Zeichenfolge muss der Schema Definition für **activityFeed**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="89bc4-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="89bc4-119">Der _hashedAddresses_ -Sring stellt einen Satz von Hash Adressen für jeden Benutzer dar, der im Personen Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="89bc4-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="89bc4-120">Die Hash-SMTP-Adressen werden mithilfe der Hashfunktion verschlüsselt, die durch das **hashFunction** -Element in den XML- **Funktionen** des Anbieters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="89bc4-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="89bc4-121">Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="89bc4-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="89bc4-122">Der __ StartTime-Parameter ist ein **Datums** Wert in koordinierter Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="89bc4-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="89bc4-123">Lokale Zeitwerte müssen in UTC- **Datums** Werte konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="89bc4-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="89bc4-124">Aktivitäten, die von der **GetActivitiesEx** -Methode zurückgegeben werden, müssen einen Wert für __ die Erstellungszeit haben, der größer als StartTime und kleiner als oder gleich **Now**ist.</span><span class="sxs-lookup"><span data-stu-id="89bc4-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="89bc4-125">Wenn zwischen **Startzeit** und **Now**keine Änderungen aufgetreten sind, muss der Anbieter einen OSC_E_NO_CHANGES-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="89bc4-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89bc4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89bc4-126">See also</span></span>

- [<span data-ttu-id="89bc4-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89bc4-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="89bc4-128">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="89bc4-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

