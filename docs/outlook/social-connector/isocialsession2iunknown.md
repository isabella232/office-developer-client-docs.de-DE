---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Unterstützt das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408831"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="30a14-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30a14-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="30a14-104">Unterstützt das Hinzufügen von Freunden, die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="30a14-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="30a14-105">Elemente</span><span class="sxs-lookup"><span data-stu-id="30a14-105">Members</span></span>

<span data-ttu-id="30a14-106">In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialSession2-Schnittstelle verfügbar** sind.</span><span class="sxs-lookup"><span data-stu-id="30a14-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="30a14-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="30a14-107">**Name**</span></span>|<span data-ttu-id="30a14-108">**Membertyp**</span><span class="sxs-lookup"><span data-stu-id="30a14-108">**Member type**</span></span>|<span data-ttu-id="30a14-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30a14-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30a14-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="30a14-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="30a14-111">Methode</span><span class="sxs-lookup"><span data-stu-id="30a14-111">Method</span></span>  <br/> |<span data-ttu-id="30a14-112">Fügt die person hinzu, die durch die  _Parameter emailAddresses_ und  _displayName_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="30a14-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="30a14-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="30a14-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="30a14-114">Methode</span><span class="sxs-lookup"><span data-stu-id="30a14-114">Method</span></span>  <br/> |<span data-ttu-id="30a14-115">Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der Benutzer darstellt, die durch den  _HashedAddresses-Parameter angegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="30a14-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="30a14-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="30a14-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="30a14-117">Methode</span><span class="sxs-lookup"><span data-stu-id="30a14-117">Method</span></span>  <br/> |<span data-ttu-id="30a14-118">Gibt eine Zeichenfolge zurück, die eine Auflistung von Personen- und Bilddetails für die benutzer enthält, die durch den  _parameter personsAddresses angegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="30a14-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="30a14-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="30a14-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="30a14-120">Methode</span><span class="sxs-lookup"><span data-stu-id="30a14-120">Method</span></span>  <br/> |<span data-ttu-id="30a14-121">Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="30a14-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a14-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30a14-122">Remarks</span></span>

<span data-ttu-id="30a14-123">Ein Outlook Social Connector (OSC)-Anbieter kann diese Schnittstelle implementieren, wenn der Anbieter die On-Demand- oder Hybridsynchronisierung von Freunden, die On-Demand-Synchronisierung von Aktivitäten oder die Anmeldung beim sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30a14-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="30a14-124">Wenn der OSC-Anbieter **ISocialSession2 implementiert** und folgende Personen im sozialen Netzwerk unterstützt, würde das OSC [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)aufrufen, und der Anbieter muss **auch ISocialSession2::FollowPersonEx** implementieren.</span><span class="sxs-lookup"><span data-stu-id="30a14-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30a14-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a14-125">See also</span></span>

- [<span data-ttu-id="30a14-126">Outlook Schnittstellen für Anbieter für soziale Verbindungen</span><span class="sxs-lookup"><span data-stu-id="30a14-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

