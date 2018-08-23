---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a84114a3363f9cbcd9455bce12d3171843bd18a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571115"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="1794c-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="1794c-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="1794c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1794c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1794c-105">Sendet Benachrichtigungen an den Client zu den geänderten in Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="1794c-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="1794c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1794c-106">Parameters</span></span>

 <span data-ttu-id="1794c-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="1794c-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="1794c-108">[in] Benachrichtigung, die Outlook an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="1794c-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="1794c-109">Die Benachrichtigung gibt den Teil des Verbindungsstatus, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="1794c-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1794c-110">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1794c-110">Remarks</span></span>

<span data-ttu-id="1794c-111">Outlook verwendet diese Methode, um die Benachrichtigung Rückrufe an einen Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="1794c-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="1794c-112">Microsoft Outlook 2010 oder Microsoft Outlook 2013 diese Schnittstelle zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren, und übergeben einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** beim Einrichten von Rückrufe mit **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1794c-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="1794c-113">Der Client auch übergibt an **MAPIOFFLINE_ADVISEINFO** ein Clienttoken, Outlook 2010 oder Outlook 2013 verwendet in **IMAPIOfflineNotify::Notify** zum Identifizieren des Clients für den Rückruf Benachrichtigung registriert.</span><span class="sxs-lookup"><span data-stu-id="1794c-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="1794c-114">Im Allgemeinen Outlook 2010 und Outlook 2013 können benachrichtigt werden, einem Client online/offline ändert und andere ändern, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1794c-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="1794c-115">Der Client muss alle anderen Benachrichtigungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="1794c-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1794c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1794c-116">See also</span></span>



[<span data-ttu-id="1794c-117">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="1794c-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="1794c-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="1794c-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

