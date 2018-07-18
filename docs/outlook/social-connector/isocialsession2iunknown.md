---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Hinzufügen von Freunden, bei Bedarf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden mit zwischengespeicherten Anmeldeinformationen unterstützt.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795999"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="347c8-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="347c8-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="347c8-104">Hinzufügen von Freunden, bei Bedarf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden mit zwischengespeicherten Anmeldeinformationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="347c8-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="347c8-105">Elemente</span><span class="sxs-lookup"><span data-stu-id="347c8-105">Members</span></span>

<span data-ttu-id="347c8-106">In der folgenden Tabelle werden die Member, die für die **ISocialSession2** -Schnittstelle verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="347c8-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="347c8-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="347c8-107">**Name**</span></span>|<span data-ttu-id="347c8-108">**Typ des Elements**</span><span class="sxs-lookup"><span data-stu-id="347c8-108">**Member type**</span></span>|<span data-ttu-id="347c8-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="347c8-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="347c8-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="347c8-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="347c8-111">Methode</span><span class="sxs-lookup"><span data-stu-id="347c8-111">Method</span></span>  <br/> |<span data-ttu-id="347c8-112">Fügt die Person, die durch die Parameter _EmailAddresses_ und _DisplayName_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="347c8-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="347c8-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="347c8-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="347c8-114">Methode</span><span class="sxs-lookup"><span data-stu-id="347c8-114">Method</span></span>  <br/> |<span data-ttu-id="347c8-115">Ruft eine Zeichenfolge, die eine Sammlung von Aktivitäten, der durch den _HashedAddresses_ -Parameter angegebenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="347c8-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="347c8-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="347c8-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="347c8-117">Methode</span><span class="sxs-lookup"><span data-stu-id="347c8-117">Method</span></span>  <br/> |<span data-ttu-id="347c8-118">Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den _PersonsAddresses_ -Parameter angegebenen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="347c8-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="347c8-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="347c8-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="347c8-120">Methode</span><span class="sxs-lookup"><span data-stu-id="347c8-120">Method</span></span>  <br/> |<span data-ttu-id="347c8-121">Meldet sich bei der social Network-Website mit zwischengespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="347c8-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="347c8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="347c8-122">Remarks</span></span>

<span data-ttu-id="347c8-123">Ein Anbieter Outlook Social Connector (OSC) können diese Schnittstelle implementieren, wenn der Anbieter unterstützt mit zwischengespeicherten Anmeldeinformationen auf Abruf oder Hybriden Synchronisierung von Freunden, bedarfsgesteuerten Synchronisierung von Aktivitäten oder im sozialen Netzwerk anmelden.</span><span class="sxs-lookup"><span data-stu-id="347c8-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="347c8-124">Wenn der OSC-Anbieter **ISocialSession2** und unterstützt die folgenden Personen im sozialen Netzwerk implementiert, die OSC würde [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md)aufrufen und der Anbieter implementiert werden müssen **ISocialSession2::FollowPersonEx**, sowie.</span><span class="sxs-lookup"><span data-stu-id="347c8-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="347c8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="347c8-125">See also</span></span>

- [<span data-ttu-id="347c8-126">Outlook Connector für soziale Netzwerke Provider-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="347c8-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

