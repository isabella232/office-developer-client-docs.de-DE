---
title: Übersicht über das MAPI-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328164"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="c58f5-103">Übersicht über das MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="c58f5-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="c58f5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c58f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c58f5-105">Ein Profil ist eine Sammlung von Informationen zu den Nachrichtendiensten und Dienstanbietern, die ein Benutzer einer Clientanwendung während einer bestimmten MAPI-Sitzung verfügbar sein möchte.</span><span class="sxs-lookup"><span data-stu-id="c58f5-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="c58f5-106">Jeder Benutzer verfügt über mindestens ein Profil. Viele Benutzer behalten mehrere.</span><span class="sxs-lookup"><span data-stu-id="c58f5-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="c58f5-107">Ein Benutzer kann beispielsweise ein Profil für die Arbeit mit einem serverbasierten Nachrichtenspeicherdienst und ein anderes Profil für die Arbeit mit einem Nachrichtenspeicherdienst auf dem lokalen Computer haben.</span><span class="sxs-lookup"><span data-stu-id="c58f5-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="c58f5-108">Ein Benutzer möchte möglicherweise auf eine Gruppe von Messagingsystemen zugreifen, indem er die entsprechenden Transportdienste für einen Teil des Tages und einen anderen Satz für den Rest des Tages verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58f5-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="c58f5-109">Profile bieten eine flexible Möglichkeit, Kombinationen von Messagingsystemdiensten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c58f5-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="c58f5-110">Profile können Namen von bis zu 64 alphanumerischen Zeichen haben.</span><span class="sxs-lookup"><span data-stu-id="c58f5-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="c58f5-111">Die Namen können Akzentzeichen, den Unterstrich und eingebettete Leerzeichen enthalten und dürfen keine vor- oder nachgestellten Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c58f5-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="c58f5-112">Profile sind hierarchisch organisiert und in Abschnitte unterteilt, mit einem Abschnitt für jeden Nachrichtendienst und einem Abschnitt für jeden Dienstanbieter in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="c58f5-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="c58f5-113">Die zugehörigen Abschnitte sind verknüpft, wodurch die Navigation durch die Informationen erleichtert wird.</span><span class="sxs-lookup"><span data-stu-id="c58f5-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="c58f5-114">Jeder Abschnitt enthält eine Reihe von Einträgen, die MAPI oder eine Clientanwendung für die Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c58f5-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="c58f5-115">Die Einträge in einem Profil variieren vom Nachrichtendienst zum Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="c58f5-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="c58f5-116">Zu den gängigen Einträgen gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="c58f5-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="c58f5-117">Der Name der einzelnen Nachrichtendienste oder Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c58f5-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="c58f5-118">Der Name der DLLs, die Dienstanbieter und Nachrichtendienste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c58f5-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="c58f5-119">Der Name der Einstiegspunktfunktion jedes Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="c58f5-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="c58f5-120">Eine Liste der Dienstanbieter, aus den einzelnen Nachrichtendiensten.</span><span class="sxs-lookup"><span data-stu-id="c58f5-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="c58f5-121">Profile können bei der Installation, beim Laden von MAPI oder einem Nachrichtendienst auf einen Computer oder zu einem späteren Zeitpunkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c58f5-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="c58f5-122">MAPI bietet den Profil-Assistenten für die Profilverwaltung.</span><span class="sxs-lookup"><span data-stu-id="c58f5-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="c58f5-123">Der Profil-Assistent ist eine Anwendung, die neue Profile mit minimalem Arbeitsvolumen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c58f5-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="c58f5-124">Der Assistent verwendet Standardwerte für Einstellungen, wo immer möglich, was benutzern Zeit und Aufwand spart.</span><span class="sxs-lookup"><span data-stu-id="c58f5-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="c58f5-125">Benutzer geben Werte nur ein, wenn dies unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c58f5-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="c58f5-126">Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="c58f5-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="c58f5-127">Sie können auch das Office-Anpassungstool verwenden, um ein neues Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c58f5-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="c58f5-128">Weitere Informationen finden Sie unter [Office-Anpassungstool](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="c58f5-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c58f5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c58f5-129">See also</span></span>



[<span data-ttu-id="c58f5-130">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="c58f5-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

