---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594698"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="a3f43-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="a3f43-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="a3f43-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3f43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3f43-105">Erzwingt abgesetzt der Benachrichtigungen an alle in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a3f43-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3f43-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a3f43-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3f43-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3f43-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3f43-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a3f43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3f43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3f43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3f43-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a3f43-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3f43-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a3f43-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3f43-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3f43-112">Parameters</span></span>

 <span data-ttu-id="a3f43-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3f43-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a3f43-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a3f43-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3f43-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a3f43-115">Return value</span></span>

<span data-ttu-id="a3f43-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3f43-116">S_OK</span></span>
  
> <span data-ttu-id="a3f43-117">Alle in der Warteschlange Benachrichtigungen haben verteilt.</span><span class="sxs-lookup"><span data-stu-id="a3f43-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="a3f43-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a3f43-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="a3f43-119">WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="a3f43-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="a3f43-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a3f43-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="a3f43-121">MAPI konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3f43-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3f43-122">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a3f43-122">Remarks</span></span>

<span data-ttu-id="a3f43-123">Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten.</span><span class="sxs-lookup"><span data-stu-id="a3f43-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="a3f43-124">Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben.</span><span class="sxs-lookup"><span data-stu-id="a3f43-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="a3f43-125">Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a3f43-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3f43-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a3f43-126">Notes to callers</span></span>

<span data-ttu-id="a3f43-127">Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) und [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a3f43-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="a3f43-128">Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="a3f43-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="a3f43-129">Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="a3f43-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

