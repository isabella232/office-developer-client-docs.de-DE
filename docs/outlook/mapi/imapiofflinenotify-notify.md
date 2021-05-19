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
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410693"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="a7c6a-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="a7c6a-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="a7c6a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7c6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7c6a-105">Sendet Benachrichtigungen über Änderungen im Verbindungsstatus an den Client.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="a7c6a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c6a-106">Parameters</span></span>

 <span data-ttu-id="a7c6a-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="a7c6a-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="a7c6a-108">[in] Die Benachrichtigung, Outlook an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="a7c6a-109">Die Benachrichtigung gibt den Teil des geänderten Verbindungsstatus, den alten Verbindungsstatus und den neuen Verbindungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7c6a-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7c6a-110">Remarks</span></span>

<span data-ttu-id="a7c6a-111">Outlook verwendet diese Methode, um Benachrichtigungsrückrufe an einen Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="a7c6a-112">Um diese Schnittstelle für Microsoft Outlook 2010 oder Microsoft Outlook 2013 zur Verfügung zu stellen, muss der Client diese Schnittstelle implementieren und einen Zeiger als Mitglied in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** übergeben, wenn Rückrufe mit **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="a7c6a-113">Der Client übergibt  außerdem MAPIOFFLINE_ADVISEINFO ein Clienttoken, das Outlook 2010 oder Outlook 2013 in **IMAPIOfflineNotify::Notify** verwendet wird, um den für den Benachrichtigungsrückruf registrierten Client zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="a7c6a-114">Im Allgemeinen können Outlook 2010 und Outlook 2013 einen Client über Online-/Offlineänderungen und andere Verbindungsstatusänderungen benachrichtigen, die Offlinestatus-API unterstützt jedoch nur Benachrichtigungen für Online-/Offlineänderungen.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="a7c6a-115">Der Client muss alle anderen Benachrichtigungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="a7c6a-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7c6a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7c6a-116">See also</span></span>



[<span data-ttu-id="a7c6a-117">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="a7c6a-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="a7c6a-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="a7c6a-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

