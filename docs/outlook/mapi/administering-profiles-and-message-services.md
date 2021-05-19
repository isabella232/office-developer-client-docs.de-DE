---
title: Verwalten von Profilen und Nachrichtendiensten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410560"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="2339c-103">Verwalten von Profilen und Nachrichtendiensten</span><span class="sxs-lookup"><span data-stu-id="2339c-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="2339c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2339c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2339c-105">Die Profil- und Nachrichtendienstverwaltung kann das Erstellen neuer Profile, das Löschen alter Profile und das Ändern der Inhalte vorhandener Profile umfassen, indem die darin enthaltenen Nachrichtendienste und Dienstanbieter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2339c-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="2339c-106">Nicht alle Clients unterstützen die Profil- und Nachrichtendienstverwaltung als Standardfeatures.</span><span class="sxs-lookup"><span data-stu-id="2339c-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="2339c-107">Einige Clients haben nichts weiter mit Profilen zu tun, als ihren Benutzern die Auswahl eines zur Anmeldezeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2339c-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="2339c-108">Wenn Sie die Profil- oder Nachrichtendienstverwaltung unterstützen, verwenden Sie wahrscheinlich die folgenden Schnittstellen, die von MAPI implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="2339c-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="2339c-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) zum Verwalten eines Nachrichtendiensts in einem Profil, auf das über [IMAPISession::AdminServices](imapisession-adminservices.md) oder [IProfAdmin::AdminServices](iprofadmin-adminservices.md)zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2339c-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="2339c-110">Messagingclients rufen in der Regel **IMAPISession auf,** während Konfigurationsclients oder Clients, die keine Nachrichten senden oder empfangen, **IProfAdmin aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="2339c-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="2339c-111">Rufen Sie nach Möglichkeit die **IProfAdmin-Methode** auf, da dadurch der Nachrichtendienst nicht gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2339c-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="2339c-112">Weitere Informationen zur Verwendung der **IMsgServiceAdmin-Schnittstelle** finden Sie in den folgenden [Themen:](configuring-a-message-service.md)Konfigurieren eines Nachrichtendiensts, [](copying-a-message-service.md)Kopieren eines Nachrichtendiensts und Löschen eines [Nachrichtendiensts.](deleting-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="2339c-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="2339c-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, auf das über die [MAPIAdminProfiles-Funktion zugegriffen werden](mapiadminprofiles.md) kann.</span><span class="sxs-lookup"><span data-stu-id="2339c-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="2339c-114">Weitere Informationen zur Verwendung der **IProfAdmin-Schnittstelle** finden Sie in den folgenden Themen: Erstellen eines Profils mithilfe von benutzerdefiniertem [Code,](creating-a-profile-by-using-custom-code.md)Kopieren eines [Profils,](copying-a-profile.md)Löschen eines Profils, [](deleting-a-profile.md)Suchen eines Profilnamens [und](finding-a-profile-name.md)Festlegen eines Standardprofils. [](setting-a-default-profile.md)</span><span class="sxs-lookup"><span data-stu-id="2339c-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="2339c-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) zum Verwalten der Eigenschaften in einem Profilabschnitt, auf den über die [IMAPISession::OpenProfileSection-](imapisession-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection-Methode](iprovideradmin-openprofilesection.md) zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2339c-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="2339c-116">Weitere Informationen zu Profilabschnitten finden Sie unter [MAPI Profiles](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="2339c-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="2339c-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) zum Verwalten der Dienstanbieter in einem Nachrichtendienst, auf den über [IMsgServiceAdmin::AdminProviders zugegriffen werden kann.](imsgserviceadmin-adminproviders.md)</span><span class="sxs-lookup"><span data-stu-id="2339c-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="2339c-118">Weitere Informationen zur Verwendung der **IProviderAdmin-Schnittstelle** finden Sie unter Hinzufügen oder Löschen von Anbietern [in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="2339c-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="2339c-119">Seien Sie vorsichtig bei der Unterstützung der Profil- und Nachrichtendienstverwaltung.</span><span class="sxs-lookup"><span data-stu-id="2339c-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="2339c-120">Es gibt keine Schutzmaßnahmen zum Schutz vor einer negativen Änderung eines verwendeten Profils.</span><span class="sxs-lookup"><span data-stu-id="2339c-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="2339c-121">MAPI kann verhindern, dass Sie ein verwendetes Profil löschen, aber Nicht verhindern, dass Sie alle Nachrichtendienste löschen.</span><span class="sxs-lookup"><span data-stu-id="2339c-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="2339c-122">Wenn Sie jeden Nachrichtendienst in einem Profil löschen, werden alle Dienstanbieter in diesen Diensten beendet, wodurch unvorhersehbare Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="2339c-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2339c-123">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="2339c-123">In this section</span></span>

[<span data-ttu-id="2339c-124">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="2339c-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="2339c-125">Beschreibt das Erstellen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="2339c-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="2339c-126">Kopieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="2339c-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="2339c-127">Beschreibt das Kopieren eines Profils.</span><span class="sxs-lookup"><span data-stu-id="2339c-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="2339c-128">Löschen eines Profils</span><span class="sxs-lookup"><span data-stu-id="2339c-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="2339c-129">Beschreibt das Löschen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="2339c-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="2339c-130">Festlegen eines Standardprofils</span><span class="sxs-lookup"><span data-stu-id="2339c-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="2339c-131">Beschreibt das Festlegen eines Standardprofils.</span><span class="sxs-lookup"><span data-stu-id="2339c-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="2339c-132">Suchen eines Profilnamens</span><span class="sxs-lookup"><span data-stu-id="2339c-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="2339c-133">Beschreibt, wie Sie einen Namen eines Profils finden.</span><span class="sxs-lookup"><span data-stu-id="2339c-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="2339c-134">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2339c-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="2339c-135">Beschreibt das Hinzufügen eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="2339c-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="2339c-136">Konfigurieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2339c-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="2339c-137">Beschreibt das Konfigurieren eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="2339c-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="2339c-138">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2339c-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="2339c-139">Beschreibt, wie ein Nachrichtendienst in ein Profil kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2339c-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="2339c-140">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="2339c-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="2339c-141">Beschreibt das Löschen eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="2339c-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="2339c-142">Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst</span><span class="sxs-lookup"><span data-stu-id="2339c-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="2339c-143">Beschreibt, wie Anbieter in einem Nachrichtendienst hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2339c-143">Describes how to add or delete providers in a message service.</span></span>
    

