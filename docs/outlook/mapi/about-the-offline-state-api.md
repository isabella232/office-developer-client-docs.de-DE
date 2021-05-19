---
title: Informationen zur Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410483"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="42f41-103">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="42f41-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="42f41-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42f41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42f41-105">Die Offlinestatus-API unterstützt Rückrufe, die Änderungen im Verbindungsstatus eines Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 anzeigen, z. B. von der Onlineverwendung in Outlook 2013 oder Outlook 2010 bis zum Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="42f41-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="42f41-106">Die API verwendet ein globales Offlineobjekt in Outlook 2013 oder Outlook 2010, um solche Änderungen für ein bestimmtes Benutzerkontoprofil nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="42f41-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="42f41-107">Benachrichtigung ist die einzige unterstützte Form des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="42f41-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="42f41-108">Als Clients dieser API gehen E-Mail-Anbieter, die über solche Verbindungsstatusänderungen benachrichtigt werden möchten, wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="42f41-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="42f41-109">Implementieren **[sie IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="42f41-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="42f41-110">Öffnen Sie ein vorhandenes Offlineobjekt für ein bestimmtes Profil mithilfe **[von HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="42f41-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="42f41-111">Ermitteln Sie, ob das Objekt über die Möglichkeit verfügt, Online- oder Offlinebenachrichtigungen mithilfe von **[IMAPIOffline::GetCapabilities zur Verfügung zu stellen.](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="42f41-112">Registrieren Sie das Objekt für Online- oder Offlinebenachrichtigungen mithilfe **[von IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="42f41-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="42f41-113">E-Mail-Anbieter können nun Benachrichtigungen empfangen, die Outlook 2013 oder Outlook 2010 senden, indem **sie IMAPIOfflineNotify verwenden.**</span><span class="sxs-lookup"><span data-stu-id="42f41-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="42f41-114">Entfernen Sie beim Herunterfahren die Registrierung für Online- und Offlinebenachrichtigungen mithilfe **[von IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="42f41-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="42f41-115">Im Allgemeinen können Outlook 2013 und Outlook 2010 einen Client über Online-/Offlineänderungen sowie andere Änderungen benachrichtigen, aber die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen.</span><span class="sxs-lookup"><span data-stu-id="42f41-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="42f41-116">Der Client sollte alle anderen Benachrichtigungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="42f41-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="42f41-117">Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="42f41-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="42f41-118">Ein Beispiel für einen Client, der die Offlinestatus-API verwendet, finden Sie unter [Informationen zum Beispiel-Offlinestatus-Add-In](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="42f41-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="42f41-119">Das Beispiel-Offlinestatus-Add-In ist ein COM-Add-In, das die Offlinestatus-API verwendet, um den Verbindungsstatus zu überwachen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="42f41-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="42f41-120">Diese API bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42f41-120">This API provides the following:</span></span>
  
<span data-ttu-id="42f41-121">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="42f41-121">Definitions:</span></span>
  
- [<span data-ttu-id="42f41-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="42f41-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="42f41-123">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="42f41-123">Data types:</span></span>
  
- <span data-ttu-id="42f41-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="42f41-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="42f41-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="42f41-127">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="42f41-127">Functions:</span></span>
  
- <span data-ttu-id="42f41-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="42f41-129">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="42f41-129">Interfaces:</span></span>
  
- <span data-ttu-id="42f41-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="42f41-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="42f41-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="42f41-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

