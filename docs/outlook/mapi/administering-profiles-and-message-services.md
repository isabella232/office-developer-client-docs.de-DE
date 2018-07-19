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
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791270"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="dbdb5-103">Verwalten von Profilen und Nachrichtendiensten</span><span class="sxs-lookup"><span data-stu-id="dbdb5-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="dbdb5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbdb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbdb5-105">Benutzerprofil und Nachricht, dass Verwalten des Diensts umfassen kann, neue Profile erstellen, alte Profile löschen und Ändern des Inhalts der vorhandene Profile durch Ändern der Message-Dienste und die darin enthaltenen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="dbdb5-106">Nicht alle Clients unterstützen Benutzerprofil und Nachricht Verwalten des Diensts als Standardfeatures.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="dbdb5-107">Einige Clients müssen keine weiteren Schritte durchgeführt mit Profilen, die als ihre Benutzer bei der Anmeldung auswählen können.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="dbdb5-108">Verwalten des Diensts Profil oder einer Nachricht unterstützen, sind wahrscheinlich, dass Sie die folgenden Schnittstellen verwenden möchten, die von MAPI implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="dbdb5-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="dbdb5-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) eine Message Service in einem Profil, das über [IMAPISession::AdminServices](imapisession-adminservices.md) oder [IProfAdmin::AdminServices](iprofadmin-adminservices.md)verwalten.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="dbdb5-110">Messaging-Clients rufen **IMAPISession** normalerweise während der Konfiguration oder Clients, die nicht senden oder Empfangen von Nachrichten, **IProfAdmin**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="dbdb5-111">Wenn möglich, rufen Sie die **IProfAdmin** -Methode, da sie nicht den Dienst gestartet werden führt.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="dbdb5-112">Weitere Informationen zur Verwendung der **IMsgServiceAdmin** -Schnittstelle finden Sie unter den folgenden Themen: [Konfigurieren einer Nachricht](configuring-a-message-service.md), [eine Message Service kopieren](copying-a-message-service.md)und [Löschen einer Nachricht-Dienstes](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="dbdb5-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="dbdb5-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, über die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="dbdb5-114">Weitere Informationen zur Verwendung der **IProfAdmin** -Schnittstelle finden Sie unter den folgenden Themen: [Erstellen eines Profils durch Verwendung benutzerdefinierter Code](creating-a-profile-by-using-custom-code.md), [Kopieren eines Profils](copying-a-profile.md), [Löschen ein Profil](deleting-a-profile.md), [Suchen Sie einen Profilnamen](finding-a-profile-name.md)und [Einstellung ein Standardprofil](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="dbdb5-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="dbdb5-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) zur Aufrechterhaltung der Eigenschaften in einem Profilabschnitt kann über die [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="dbdb5-116">Weitere Informationen über Profil Abschnitte finden Sie unter [MAPI-Profile](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="dbdb5-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="dbdb5-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) zur Verwaltung der Dienstanbieter in einem Message-Dienst über [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="dbdb5-118">Weitere Informationen zur Verwendung der **IProviderAdmin** -Schnittstelle finden Sie unter [Hinzufügen oder Löschen von Anbietern in einem Message-Dienst](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="dbdb5-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="dbdb5-119">Achten Sie darauf, dass in Ihre Unterstützung von Profil- und Nachricht verwalten.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="dbdb5-120">Es gibt keine Sicherheitsfunktionen zum Schutz gegen ändern sich negativ auf ein Profil, das verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="dbdb5-121">MAPI kann verhindern, dass Sie löschen ein Profil verwendet, aber kann nicht verhindern, dass Sie alle Messagingdiensts darin löschen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="dbdb5-122">Wenn Sie jeden Nachrichtendienst in einem Profil löschen, hält alle-Dienstanbieter in dieser Dienste und verursacht dadurch zu unvorhersehbaren Ergebnissen eintritt.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="dbdb5-123">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="dbdb5-123">In this section</span></span>

[<span data-ttu-id="dbdb5-124">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="dbdb5-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="dbdb5-125">Beschreibt, wie Sie ein Profil erstellen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="dbdb5-126">Kopieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="dbdb5-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="dbdb5-127">Beschreibt, wie ein Profil zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="dbdb5-128">Löschen eines Profils</span><span class="sxs-lookup"><span data-stu-id="dbdb5-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="dbdb5-129">Beschreibt, wie ein Profil zu löschen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="dbdb5-130">Festlegen eines Standardprofils</span><span class="sxs-lookup"><span data-stu-id="dbdb5-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="dbdb5-131">Beschreibt, wie ein Standardprofil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="dbdb5-132">Suchen nach einem Profilnamen</span><span class="sxs-lookup"><span data-stu-id="dbdb5-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="dbdb5-133">Beschreibt, wie ein Profil einen Namen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="dbdb5-134">Hinzufügen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="dbdb5-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="dbdb5-135">Beschreibt, wie einen Nachrichtendienst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="dbdb5-136">Konfigurieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="dbdb5-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="dbdb5-137">Beschreibt, wie eine Message Service konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="dbdb5-138">Kopieren eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="dbdb5-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="dbdb5-139">Beschreibt, wie eine Messagingdiensts zu einem Profil zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="dbdb5-140">Löschen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="dbdb5-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="dbdb5-141">Beschreibt, wie eine Messagingdiensts zu löschen.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="dbdb5-142">Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst</span><span class="sxs-lookup"><span data-stu-id="dbdb5-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="dbdb5-143">Beschreibt das Hinzufügen oder Löschen von Anbietern in einem Message-Dienst.</span><span class="sxs-lookup"><span data-stu-id="dbdb5-143">Describes how to add or delete providers in a message service.</span></span>
    

