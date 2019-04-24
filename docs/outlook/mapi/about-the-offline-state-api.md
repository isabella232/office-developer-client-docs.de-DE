---
title: Informationen zur Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321791"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="ecb5f-103">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="ecb5f-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="ecb5f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb5f-105">Die Offlinestatus-API unterstützt Rückrufe, die Änderungen des Verbindungsstatus eines Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 angeben, beispielsweise von der Online Funktion in Outlook 2013 oder Outlook 2010 zum Offline schalten.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="ecb5f-106">Die API verwendet ein globales Offline-Objekt in Outlook 2013 oder Outlook 2010, um solche Änderungen für ein bestimmtes Benutzerkontoprofil nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="ecb5f-107">Benachrichtigung ist das einzige unterstützte Rückrufformular.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="ecb5f-108">Als Clients dieser API gehen e-Mail-Anbieter, die über einen solchen Verbindungsstatus benachrichtigt werden möchten, wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="ecb5f-109">Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="ecb5f-110">Öffnen Sie ein vorhandenes Offline-Objekt für ein bestimmtes Profil mit **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="ecb5f-111">Bestimmen Sie, ob das Objekt über die Möglichkeit zum Bereitstellen von Online-oder offline Benachrichtigungen mithilfe von **[IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)** verfügt.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="ecb5f-112">Registrieren Sie das Objekt für Online-oder offline Benachrichtigungen mit **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ecb5f-113">E-Mail-Anbieter können jetzt Benachrichtigungen erhalten, die von Outlook 2013 oder Outlook 2010 mithilfe von **IMAPIOfflineNotify**gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="ecb5f-114">Entfernen Sie beim Herunterfahren die Registrierung für Online-und Offline Benachrichtigungen mit **[IMAPIOfflineMgr:: Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ecb5f-115">Im Allgemeinen können Outlook 2013 und Outlook 2010 einen Client über Online-/Offline-Änderungen sowie andere Änderungen informieren, die Offlinestatus-API unterstützt jedoch nur Benachrichtigungen für Online/Offline-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="ecb5f-116">Der Client sollte alle anderen Benachrichtigungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="ecb5f-117">Weitere Informationen finden Sie unter **[IMAPIOfflineNotify:: notify](imapiofflinenotify-notify.md)** und **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="ecb5f-118">Ein Beispiel für einen Client, der die Offlinestatus-API verwendet, finden Sie unter [Informationen zum Offlinestatus-Add-in-Beispiel](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="ecb5f-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="ecb5f-119">Das Beispiel für Offlinestatus-Add-in ist ein COM-Add-in, das die Offline Status-API verwendet, um den Verbindungsstatus zu überwachen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ecb5f-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="ecb5f-120">Diese API bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-120">This API provides the following:</span></span>
  
<span data-ttu-id="ecb5f-121">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-121">Definitions:</span></span>
  
- [<span data-ttu-id="ecb5f-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ecb5f-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="ecb5f-123">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-123">Data types:</span></span>
  
- <span data-ttu-id="ecb5f-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="ecb5f-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="ecb5f-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="ecb5f-127">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-127">Functions:</span></span>
  
- <span data-ttu-id="ecb5f-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="ecb5f-129">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="ecb5f-129">Interfaces:</span></span>
  
- <span data-ttu-id="ecb5f-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="ecb5f-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="ecb5f-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb5f-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

