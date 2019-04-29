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
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="637e6-103">Verwalten von Profilen und Nachrichtendiensten</span><span class="sxs-lookup"><span data-stu-id="637e6-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="637e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="637e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="637e6-105">Die Verwaltung von Profil-und Nachrichtendiensten kann dazu dienen, neue Profile zu erstellen, alte Profile zu löschen und die Inhalte vorhandener Profile zu ändern, indem Sie die darin enthaltenen Nachrichtendienste und Dienstanbieter ändern.</span><span class="sxs-lookup"><span data-stu-id="637e6-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="637e6-106">Nicht alle Clients unterstützen die Verwaltung von Profil-und Nachrichtendiensten als Standardfunktionen.</span><span class="sxs-lookup"><span data-stu-id="637e6-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="637e6-107">Einige Clients haben nichts mehr mit Profilen zu tun, als es Ihren Benutzern bei der Anmeldung zu erlauben, eine auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="637e6-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="637e6-108">Wenn Sie die Verwaltung des Profil-oder Nachrichtendiensts unterstützen, können Sie die folgenden Schnittstellen verwenden, die von MAPI implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="637e6-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="637e6-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) zum Verwalten eines Nachrichtendiensts in einem Profil, auf das entweder über [IMAPISession:: AdminServices](imapisession-adminservices.md) oder [IProfAdmin:: AdminServices](iprofadmin-adminservices.md)zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="637e6-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="637e6-110">Messaging-Clients rufen in der Regel **IMAPISession** auf, während Konfigurations Clients oder Clients, die keine Nachrichten senden oder empfangen, **IProfAdmin**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="637e6-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="637e6-111">Rufen Sie nach Möglichkeit die **IProfAdmin** -Methode auf, da der Nachrichtendienst nicht gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="637e6-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="637e6-112">Weitere Informationen zur Verwendung der **IMsgServiceAdmin** -Schnittstelle finden Sie in den folgenden Themen: [Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md), [Kopieren eines Nachrichten](copying-a-message-service.md)Diensts und [Löschen eines Nachrichtendiensts](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="637e6-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="637e6-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, auf das über die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="637e6-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="637e6-114">Weitere Informationen zur Verwendung der **IProfAdmin** -Schnittstelle finden Sie in den folgenden Themen: [Erstellen eines Profils mithilfe von benutzerdefiniertem Code](creating-a-profile-by-using-custom-code.md), [Kopieren eines Profils](copying-a-profile.md), [Löschen eines](deleting-a-profile.md)Profils, [Suchen eines Profilnamens](finding-a-profile-name.md)und [Festlegen eines Standardprofil](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="637e6-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="637e6-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) zum Verwalten der Eigenschaften in einem Profil Abschnitt, auf die über die [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) -oder [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="637e6-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="637e6-116">Weitere Informationen zu Profil Abschnitten finden Sie unter [MAPI-Profile](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="637e6-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="637e6-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) zum Verwalten der Dienstanbieter in einem Nachrichtendienst, auf die über [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md)zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="637e6-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="637e6-118">Weitere Informationen zur Verwendung der **IProviderAdmin** -Schnittstelle finden Sie unter [Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="637e6-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="637e6-119">Achten Sie auf die Unterstützung der Verwaltung von Profil-und Nachrichtendiensten.</span><span class="sxs-lookup"><span data-stu-id="637e6-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="637e6-120">Es gibt keine Schutzvorkehrungen, die gegen eine nachteilige Änderung eines verwendeten Profils geschützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="637e6-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="637e6-121">MAPI kann das Löschen eines verwendeten Profils verhindern, kann jedoch nicht verhindern, dass Sie jeden Nachrichtendienst darin löschen.</span><span class="sxs-lookup"><span data-stu-id="637e6-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="637e6-122">Wenn Sie jeden Nachrichtendienst in einem Profil löschen, werden alle Dienstanbieter in diesen Diensten angehalten, wodurch unvorhersehbare Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="637e6-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="637e6-123">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="637e6-123">In this section</span></span>

[<span data-ttu-id="637e6-124">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="637e6-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="637e6-125">Beschreibt das Erstellen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="637e6-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="637e6-126">Kopieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="637e6-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="637e6-127">Beschreibt das Kopieren eines Profils.</span><span class="sxs-lookup"><span data-stu-id="637e6-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="637e6-128">Löschen eines Profils</span><span class="sxs-lookup"><span data-stu-id="637e6-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="637e6-129">Beschreibt das Löschen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="637e6-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="637e6-130">Festlegen eines Standardprofils</span><span class="sxs-lookup"><span data-stu-id="637e6-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="637e6-131">Beschreibt, wie ein Standardprofil festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="637e6-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="637e6-132">Suchen nach einem Profilnamen</span><span class="sxs-lookup"><span data-stu-id="637e6-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="637e6-133">Beschreibt, wie Sie einen Namen eines Profils finden.</span><span class="sxs-lookup"><span data-stu-id="637e6-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="637e6-134">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="637e6-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="637e6-135">Beschreibt das Hinzufügen eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="637e6-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="637e6-136">Konfigurieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="637e6-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="637e6-137">Beschreibt, wie ein Nachrichtendienst konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="637e6-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="637e6-138">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="637e6-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="637e6-139">Beschreibt, wie ein Nachrichtendienst in ein Profil kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="637e6-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="637e6-140">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="637e6-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="637e6-141">Beschreibt das Löschen eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="637e6-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="637e6-142">Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst</span><span class="sxs-lookup"><span data-stu-id="637e6-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="637e6-143">Beschreibt das Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="637e6-143">Describes how to add or delete providers in a message service.</span></span>
    

