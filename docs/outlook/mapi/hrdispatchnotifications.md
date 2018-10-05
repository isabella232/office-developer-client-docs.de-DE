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
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385564"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="9d7ae-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="9d7ae-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="9d7ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d7ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d7ae-105">Erzwingt abgesetzt der Benachrichtigungen an alle in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d7ae-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="9d7ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d7ae-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9d7ae-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9d7ae-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9d7ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d7ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d7ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d7ae-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9d7ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="9d7ae-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9d7ae-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9d7ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d7ae-112">Parameters</span></span>

 <span data-ttu-id="9d7ae-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d7ae-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9d7ae-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d7ae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d7ae-115">Return value</span></span>

<span data-ttu-id="9d7ae-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d7ae-116">S_OK</span></span>
  
> <span data-ttu-id="9d7ae-117">Alle in der Warteschlange Benachrichtigungen haben verteilt.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="9d7ae-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9d7ae-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="9d7ae-119">WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="9d7ae-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9d7ae-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="9d7ae-121">MAPI konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d7ae-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d7ae-122">Remarks</span></span>

<span data-ttu-id="9d7ae-123">Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="9d7ae-124">Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="9d7ae-125">Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9d7ae-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9d7ae-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9d7ae-126">Notes to callers</span></span>

<span data-ttu-id="9d7ae-127">Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) und [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) and [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="9d7ae-128">Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="9d7ae-129">Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="9d7ae-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

