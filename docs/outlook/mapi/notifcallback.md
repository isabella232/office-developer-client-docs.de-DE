---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434018"
---
# <a name="notifcallback"></a><span data-ttu-id="ebddb-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="ebddb-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="ebddb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebddb-105">Definiert eine Rückruffunktion, die MAPI aufruft, um eine Ereignisbenachrichtigung zu senden.</span><span class="sxs-lookup"><span data-stu-id="ebddb-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="ebddb-106">Diese Rückruffunktion kann nur verwendet werden, wenn sie in ein Advise Sink-Objekt gepackt wird, das durch Aufrufen der [HrAllocAdviseSink-Funktion erstellt](hrallocadvisesink.md) wurde.</span><span class="sxs-lookup"><span data-stu-id="ebddb-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebddb-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ebddb-107">Header file:</span></span>  <br/> |<span data-ttu-id="ebddb-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebddb-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ebddb-109">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ebddb-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ebddb-110">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ebddb-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ebddb-111">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="ebddb-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ebddb-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="ebddb-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="ebddb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebddb-113">Parameters</span></span>

 <span data-ttu-id="ebddb-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="ebddb-114">_lpvContext_</span></span>
  
> <span data-ttu-id="ebddb-115">[in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="ebddb-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="ebddb-116">Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung oder den Dienstanbieter von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="ebddb-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="ebddb-117">Normalerweise stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf ein C++-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="ebddb-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="ebddb-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="ebddb-118">_cNotification_</span></span>
  
> <span data-ttu-id="ebddb-119">[in] Anzahl der Ereignisbenachrichtigungen im Array, das durch den  _lpNotifications-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="ebddb-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="ebddb-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="ebddb-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="ebddb-121">[out] Zeiger auf den Speicherort, an dem diese Funktion ein Array von [NOTIFICATION-Strukturen](notification.md) schreibt, das die Ereignisbenachrichtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="ebddb-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebddb-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebddb-122">Return value</span></span>

<span data-ttu-id="ebddb-123">Der Satz gültiger Rückgabewerte für den PROTOTYP der **NOTIFCALLBACK-Funktion** hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ebddb-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="ebddb-124">Clients sollten immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="ebddb-124">Clients should always return S_OK.</span></span> <span data-ttu-id="ebddb-125">Anbieter können entweder S_OK oder CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="ebddb-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ebddb-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ebddb-126">Remarks</span></span>

<span data-ttu-id="ebddb-127">CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert nur für synchrone Rückruffunktionen. es fordert die MAPI auf, die Verarbeitung der Rückrufe für diese Benachrichtigung sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ebddb-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="ebddb-128">Wenn CALLBACK_DISCONTINUE zurückgegeben wird, legt MAPI den _lpUlFlags-Parameter_ auf NOTIFY_CANCELED fest, wenn er von [IMAPISupport::Notify zurückgegeben wird.](imapisupport-notify.md)</span><span class="sxs-lookup"><span data-stu-id="ebddb-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="ebddb-129">Es folgen Einschränkungen, was eine synchrone Rückruffunktion tun kann:</span><span class="sxs-lookup"><span data-stu-id="ebddb-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="ebddb-130">Es kann nicht dazu führen, dass eine weitere synchrone Benachrichtigung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ebddb-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="ebddb-131">Es kann keine Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ebddb-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebddb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebddb-132">See also</span></span>



[<span data-ttu-id="ebddb-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ebddb-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

