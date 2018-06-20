---
title: Über die Offline State-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791246"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="c2288-103">Über die Offline State-API</span><span class="sxs-lookup"><span data-stu-id="c2288-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="c2288-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2288-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2288-105">Die Offline Zustand-API unterstützt Rückrufe, der angibt, Änderungen in den Status der Verbindung des Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 – beispielsweise verhindern in Outlook 2013 oder Outlook 2010 online zu offline.</span><span class="sxs-lookup"><span data-stu-id="c2288-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="c2288-106">Die API verwendet ein globales offline-Objekt in Outlook 2013 oder Outlook 2010, um eine solche Änderung für einen bestimmten Benutzerkontoprofil verfolgen.</span><span class="sxs-lookup"><span data-stu-id="c2288-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="c2288-107">Die Benachrichtigung ist die einzige unterstützte Form der Rückruf an.</span><span class="sxs-lookup"><span data-stu-id="c2288-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="c2288-108">Wie Clients dieser API, e-Mail-Anbieter, die über eine solche Verbindung Zustandsänderungen benachrichtigt werden möchten, die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c2288-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="c2288-109">Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="c2288-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="c2288-110">Öffnen Sie ein vorhandenes offline-Objekt für ein bestimmtes Profil **[HrOpenOfflineObj](hropenofflineobj.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2288-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="c2288-111">Ermitteln Sie, ob das Objekt die Möglichkeit der Bereitstellung von online oder offline Benachrichtigungen mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** hat.</span><span class="sxs-lookup"><span data-stu-id="c2288-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="c2288-112">Registrieren Sie das Objekt für online oder offline Benachrichtigungen **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2288-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="c2288-113">E-Mail-Anbieter können nun Benachrichtigungen erhalten, dass Outlook 2013 oder Outlook 2010 senden **IMAPIOfflineNotify**verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2288-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="c2288-114">Entfernen Sie beim Herunterfahren Registrierung für online und offline Benachrichtigungen **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2288-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c2288-115">Im Allgemeinen Outlook 2013 und Outlook 2010 können von einem Client von online/offline Änderungen sowie weitere Änderungen benachrichtigt, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c2288-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="c2288-116">Der Client sollte alle anderen Benachrichtigungen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c2288-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="c2288-117">Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** und **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="c2288-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="c2288-118">Ein Beispiel für ein Client, der State-API verwendet, finden Sie unter [Informationen zu the Beispiel Offline State-Add-in](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="c2288-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="c2288-119">Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, die Status-API zum Überwachen und Ändern des Verbindungsstatus verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2288-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="c2288-120">Diese API bietet folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c2288-120">This API provides the following:</span></span>
  
<span data-ttu-id="c2288-121">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="c2288-121">Definitions:</span></span>
  
- [<span data-ttu-id="c2288-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c2288-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="c2288-123">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="c2288-123">Data types:</span></span>
  
- <span data-ttu-id="c2288-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="c2288-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="c2288-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="c2288-127">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c2288-127">Functions:</span></span>
  
- <span data-ttu-id="c2288-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="c2288-129">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="c2288-129">Interfaces:</span></span>
  
- <span data-ttu-id="c2288-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="c2288-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="c2288-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c2288-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

