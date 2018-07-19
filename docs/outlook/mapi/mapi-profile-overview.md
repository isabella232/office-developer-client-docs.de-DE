---
title: Übersicht über die MAPI-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 573709c4374786bb1bd3d763c8ba91de59f7fb1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793028"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="d2c13-103">Übersicht über die MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="d2c13-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="d2c13-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2c13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2c13-105">Ein Profil ist eine Auflistung von Informationen zu den Message-Dienste und Dienstanbieter, die ein Benutzer von einer Clientanwendung möchte während einer bestimmten MAPI-Sitzung verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="d2c13-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="d2c13-106">Jeder Benutzer verfügt über mindestens ein Profil; viele Benutzer behalten mehrere.</span><span class="sxs-lookup"><span data-stu-id="d2c13-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="d2c13-107">Ein Benutzer möglicherweise beispielsweise ein Profil entwickelt eine serverbasierte Message Store Service und ein anderes Profil ein Informationsspeicher-Dienst auf dem lokalen Computer entwickelt.</span><span class="sxs-lookup"><span data-stu-id="d2c13-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="d2c13-108">Ein Benutzer kann auf eine Gruppe von messaging-Systeme mithilfe der entsprechenden Transportdienste für einen Teil der Tag und eine andere für den Rest des Tages zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2c13-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="d2c13-109">Profile bieten eine flexible Möglichkeit zum Kombinationen von messaging-Systemdienste auswählen.</span><span class="sxs-lookup"><span data-stu-id="d2c13-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="d2c13-110">Profile können Namen bis zu 64 alphanumerische Zeichen Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d2c13-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="d2c13-111">Die Namen können Akzent Zeichen, Unterstriche und Leerzeichen enthalten und darf keine Leerzeichen beginnen oder enden.</span><span class="sxs-lookup"><span data-stu-id="d2c13-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="d2c13-112">Profile sind hierarchisch organisiert und Abschnitte mit einem Abschnitt für jeden Nachrichtendienst und einen Abschnitt für jeden Anbieter in einem Dienst unterteilt.</span><span class="sxs-lookup"><span data-stu-id="d2c13-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="d2c13-113">Verwandte Abschnitte sind verknüpft, die Informationen Navigieren zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="d2c13-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="d2c13-114">Jeder Abschnitt enthält eine Reihe von Einträgen, die MAPI- oder einer anderen Clientanwendung für die Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2c13-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="d2c13-115">Die Einträge in einem Profil enthalten unterscheiden sich von Messagingdiensts zu Messagingdiensts.</span><span class="sxs-lookup"><span data-stu-id="d2c13-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="d2c13-116">Einige allgemeine Einträge umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d2c13-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="d2c13-117">Der Name jedes Messagingdiensts oder Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d2c13-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="d2c13-118">Der Name der DLLs, die e-Mail-Dienste und enthalten-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d2c13-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="d2c13-119">Der Name der einzelnen Messagingdiensts Eintrag Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="d2c13-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="d2c13-120">Eine Liste der Dienstanbieter, die jeder Messagingdiensts bilden.</span><span class="sxs-lookup"><span data-stu-id="d2c13-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="d2c13-121">Profile können bei der Installation, wenn MAPI oder einer Nachrichtendienst auf einem Computer geladen wird, oder zu einem späteren Zeitpunkt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2c13-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="d2c13-122">MAPI bietet der Profil-Assistent für die Benutzerprofildienst-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d2c13-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="d2c13-123">Der Profil-Assistent ist eine Anwendung, die mit einem minimum an der Arbeit neue Profile erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2c13-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="d2c13-124">Der Assistent verwendet Standardwerte für Einstellungen möglichst Benutzer Zeit und Mühe speichern.</span><span class="sxs-lookup"><span data-stu-id="d2c13-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="d2c13-125">Nur bei Bedarf Werte geben die Benutzer ein.</span><span class="sxs-lookup"><span data-stu-id="d2c13-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="d2c13-126">Weitere Informationen finden Sie unter [Erstellen eines Profils mithilfe der Profil-Assistent](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="d2c13-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="d2c13-127">Sie können auch Office-Anpassungstool verwenden, um ein neues Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2c13-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="d2c13-128">Weitere Informationen finden Sie unter [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="d2c13-128">For more information, see [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2c13-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2c13-129">See also</span></span>



[<span data-ttu-id="d2c13-130">MAPI-Features und die Architektur</span><span class="sxs-lookup"><span data-stu-id="d2c13-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

