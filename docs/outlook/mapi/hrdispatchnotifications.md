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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791918"
---
# <a name="hrdispatchnotifications"></a><span data-ttu-id="a599d-103">HrDispatchNotifications</span><span class="sxs-lookup"><span data-stu-id="a599d-103">HrDispatchNotifications</span></span>

  
  
<span data-ttu-id="a599d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a599d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a599d-105">Erzwingt abgesetzt der Benachrichtigungen an alle in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a599d-105">Forces dispatching of all queued notifications.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a599d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a599d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a599d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a599d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a599d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a599d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a599d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a599d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a599d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a599d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a599d-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a599d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a599d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a599d-112">Parameters</span></span>

 <span data-ttu-id="a599d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a599d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a599d-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a599d-114">[in] Reserved; must be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a599d-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a599d-115">Return value</span></span>

<span data-ttu-id="a599d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a599d-116">S_OK</span></span>
  
> <span data-ttu-id="a599d-117">Alle in der Warteschlange Benachrichtigungen haben verteilt.</span><span class="sxs-lookup"><span data-stu-id="a599d-117">All queued notifications have been dispatched.</span></span>
    
<span data-ttu-id="a599d-118">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a599d-118">MAPI_E_USER_CANCEL</span></span>
  
> <span data-ttu-id="a599d-119">WM_QUIT, WM_QUERYENDSESSION oder WM_ENDSESSION wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="a599d-119">WM_QUIT, WM_QUERYENDSESSION, or WM_ENDSESSION was received.</span></span>
    
<span data-ttu-id="a599d-120">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a599d-120">MAPI_E_NOT_INITIALIZED</span></span>
  
> <span data-ttu-id="a599d-121">MAPI konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a599d-121">MAPI was not initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a599d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a599d-122">Remarks</span></span>

<span data-ttu-id="a599d-123">Die Funktion **HrDispatchNotifications** bewirkt, dass MAPI zu sendende alle Benachrichtigungen, die derzeit in der MAPI-Benachrichtigung Engine Warteschlange abgelegt werden ohne eine Nachricht Versendung warten.</span><span class="sxs-lookup"><span data-stu-id="a599d-123">The **HrDispatchNotifications** function causes MAPI to dispatch all notifications that are currently queued in the MAPI notification engine without waiting for a message dispatch.</span></span> <span data-ttu-id="a599d-124">Dies kann eine wirtschaftliche Auswirkung auf die RAM-Auslastung von haben.</span><span class="sxs-lookup"><span data-stu-id="a599d-124">This can have a beneficial effect on memory utilization.</span></span> <span data-ttu-id="a599d-125">Weitere Informationen finden Sie unter [erzwingen eine Benachrichtigung](forcing-a-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a599d-125">For more information, see [Forcing a Notification](forcing-a-notification.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a599d-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a599d-126">Notes to callers</span></span>

<span data-ttu-id="a599d-127">Einige Anwendungen warten Sie eine Benachrichtigung in einer Timeoutschleife, die mit dem Windows- [PeekMessage](http://msdn.microsoft.com/de-de/library/ms644943.aspx) und [DispatchMessage](http://msdn.microsoft.com/de-de/library/ms644934.aspx) Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a599d-127">Some applications wait for a notification message in a timeout loop using the Windows [PeekMessage](http://msdn.microsoft.com/de-de/library/ms644943.aspx) and [DispatchMessage](http://msdn.microsoft.com/de-de/library/ms644934.aspx) functions.</span></span> <span data-ttu-id="a599d-128">Klicken Sie auf alle außer den schnellsten Plattformen können solcher Anwendungen schlechten Leistung oder sogar Blockierung der Benachrichtigungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="a599d-128">On all but the fastest platforms, such applications might experience poor performance or even blockage of notifications.</span></span> <span data-ttu-id="a599d-129">Mithilfe von **HrDispatchNotifications** nicht nur verringert Code, sondern wird die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="a599d-129">Using **HrDispatchNotifications** not only reduces code but improves performance.</span></span> 
  

