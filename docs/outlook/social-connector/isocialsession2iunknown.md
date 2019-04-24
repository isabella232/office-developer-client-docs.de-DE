---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Unterstützt das Hinzufügen von Freunden, der on-Demand-oder Hybrid Synchronisierung von Freunden, der bedarfsgesteuerten Synchronisierung von Aktivitäten oder der Anmeldung am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345297"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="df93e-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df93e-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="df93e-104">Unterstützt das Hinzufügen von Freunden, der on-Demand-oder Hybrid Synchronisierung von Freunden, der bedarfsgesteuerten Synchronisierung von Aktivitäten oder der Anmeldung am sozialen Netzwerk mithilfe von zwischengespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="df93e-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="df93e-105">Elemente</span><span class="sxs-lookup"><span data-stu-id="df93e-105">Members</span></span>

<span data-ttu-id="df93e-106">In der folgenden Tabelle sind die Member aufgeführt, die auf der **ISocialSession2** -Schnittstelle verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="df93e-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="df93e-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="df93e-107">**Name**</span></span>|<span data-ttu-id="df93e-108">**Mitgliedstyp**</span><span class="sxs-lookup"><span data-stu-id="df93e-108">**Member type**</span></span>|<span data-ttu-id="df93e-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df93e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df93e-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="df93e-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="df93e-111">Methode</span><span class="sxs-lookup"><span data-stu-id="df93e-111">Method</span></span>  <br/> |<span data-ttu-id="df93e-112">Fügt die Person, die von den Parametern " _Email_ " und " _DisplayName_ " identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="df93e-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="df93e-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="df93e-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="df93e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="df93e-114">Method</span></span>  <br/> |<span data-ttu-id="df93e-115">Ruft eine Zeichenfolge ab, die eine Auflistung von Aktivitäten der durch den _hashedAddresses_ -Parameter angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="df93e-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="df93e-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="df93e-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="df93e-117">Methode</span><span class="sxs-lookup"><span data-stu-id="df93e-117">Method</span></span>  <br/> |<span data-ttu-id="df93e-118">Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den _personsAddresses_ -Parameter angegebenen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="df93e-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="df93e-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="df93e-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="df93e-120">Methode</span><span class="sxs-lookup"><span data-stu-id="df93e-120">Method</span></span>  <br/> |<span data-ttu-id="df93e-121">Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen am Netzwerkstandort für soziale Netzwerke an.</span><span class="sxs-lookup"><span data-stu-id="df93e-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df93e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df93e-122">Remarks</span></span>

<span data-ttu-id="df93e-123">Ein Outlook Social Connector-Anbieter (OSC) kann diese Schnittstelle implementieren, wenn der Anbieter die on-Demand-oder Hybrid Synchronisierung von Freunden, die bedarfsgesteuerte Synchronisierung von Aktivitäten oder die Anmeldung am sozialen Netzwerk mithilfe zwischengespeicherter Anmeldeinformationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df93e-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="df93e-124">Wenn der OSC-Anbieter **ISocialSession2** implementiert und folgende Personen im sozialen Netzwerk unterstützt, würde osc [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession: FollowPerson](isocialsession-followperson.md)aufrufen, und der Anbieter muss **ISocialSession2:: FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="df93e-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df93e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df93e-125">See also</span></span>

- [<span data-ttu-id="df93e-126">Outlook Social Connector-Anbieterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="df93e-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

