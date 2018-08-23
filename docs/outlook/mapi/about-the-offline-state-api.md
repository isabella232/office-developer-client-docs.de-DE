---
title: Informationen zu der Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: aa30a173251193d74d6560c8dce2663463a18e36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565984"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="b4ff2-103">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="b4ff2-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="b4ff2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4ff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4ff2-105">Die Offline Zustand-API unterstützt Rückrufe, der angibt, Änderungen in den Status der Verbindung des Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 – beispielsweise verhindern in Outlook 2013 oder Outlook 2010 online zu offline.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="b4ff2-106">Die API verwendet ein globales offline-Objekt in Outlook 2013 oder Outlook 2010, um eine solche Änderung für einen bestimmten Benutzerkontoprofil verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="b4ff2-107">Die Benachrichtigung ist die einzige unterstützte Form der Rückruf an.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="b4ff2-108">Wie Clients dieser API, e-Mail-Anbieter, die über eine solche Verbindung Zustandsänderungen benachrichtigt werden möchten, die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="b4ff2-109">Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="b4ff2-110">Öffnen Sie ein vorhandenes offline-Objekt für ein bestimmtes Profil **[HrOpenOfflineObj](hropenofflineobj.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="b4ff2-111">Ermitteln Sie, ob das Objekt die Möglichkeit der Bereitstellung von online oder offline Benachrichtigungen mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** hat.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="b4ff2-112">Registrieren Sie das Objekt für online oder offline Benachrichtigungen **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="b4ff2-113">E-Mail-Anbieter können nun Benachrichtigungen erhalten, dass Outlook 2013 oder Outlook 2010 senden **IMAPIOfflineNotify**verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="b4ff2-114">Entfernen Sie beim Herunterfahren Registrierung für online und offline Benachrichtigungen **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b4ff2-115">Im Allgemeinen Outlook 2013 und Outlook 2010 können von einem Client von online/offline Änderungen sowie weitere Änderungen benachrichtigt, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="b4ff2-116">Der Client sollte alle anderen Benachrichtigungen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="b4ff2-117">Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** und **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="b4ff2-118">Ein Beispiel für ein Client, der State-API verwendet, finden Sie unter [Informationen zu the Beispiel Offline State-Add-in](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b4ff2-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="b4ff2-119">Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, die Status-API zum Überwachen und Ändern des Verbindungsstatus verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4ff2-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="b4ff2-120">Diese API bietet folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-120">This API provides the following:</span></span>
  
<span data-ttu-id="b4ff2-121">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-121">Definitions:</span></span>
  
- [<span data-ttu-id="b4ff2-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b4ff2-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="b4ff2-123">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-123">Data types:</span></span>
  
- <span data-ttu-id="b4ff2-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="b4ff2-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="b4ff2-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="b4ff2-127">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-127">Functions:</span></span>
  
- <span data-ttu-id="b4ff2-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="b4ff2-129">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b4ff2-129">Interfaces:</span></span>
  
- <span data-ttu-id="b4ff2-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="b4ff2-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="b4ff2-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="b4ff2-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

