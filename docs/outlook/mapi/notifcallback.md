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
# <a name="notifcallback"></a><span data-ttu-id="641f8-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="641f8-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="641f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="641f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="641f8-105">Definiert eine Rückruffunktion, die von MAPI aufgerufen wird, um eine Ereignisbenachrichtigung zu senden.</span><span class="sxs-lookup"><span data-stu-id="641f8-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="641f8-106">Diese Rückruffunktion kann nur verwendet werden, wenn Sie in ein Advise-Senke-Objekt eingeschlossen wird, das durch Aufrufen der [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="641f8-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="641f8-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="641f8-107">Header file:</span></span>  <br/> |<span data-ttu-id="641f8-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="641f8-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="641f8-109">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="641f8-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="641f8-110">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="641f8-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="641f8-111">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="641f8-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="641f8-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="641f8-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="641f8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="641f8-113">Parameters</span></span>

 <span data-ttu-id="641f8-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="641f8-114">_lpvContext_</span></span>
  
> <span data-ttu-id="641f8-115">in Zeiger auf einen beliebigen Wert, der beim Aufrufen von MAPI an die Rückruffunktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="641f8-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="641f8-116">Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung oder den Dienstanbieter von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="641f8-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="641f8-117">Für C++-Code stellt der Parameter _LpvContext_ in der Regel einen Zeiger auf ein c++-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="641f8-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="641f8-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="641f8-118">_cNotification_</span></span>
  
> <span data-ttu-id="641f8-119">in Die Anzahl der Ereignisbenachrichtigungen im durch den _lpNotifications_ -Parameter angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="641f8-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="641f8-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="641f8-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="641f8-121">Out Zeiger auf den Speicherort, an dem diese Funktion ein Array [](notification.md) von Benachrichtigungs Strukturen mit den Ereignisbenachrichtigungen schreibt.</span><span class="sxs-lookup"><span data-stu-id="641f8-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="641f8-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="641f8-122">Return value</span></span>

<span data-ttu-id="641f8-123">Die Menge gültiger Rückgabewerte für den Prototyp der **NOTIFCALLBACK** -Funktion hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="641f8-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="641f8-124">Clients sollten immer S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="641f8-124">Clients should always return S_OK.</span></span> <span data-ttu-id="641f8-125">Anbieter können S_OK oder CALLBACK_DISCONTINUE zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="641f8-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="641f8-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="641f8-126">Remarks</span></span>

<span data-ttu-id="641f8-127">CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert für synchrone Rückruffunktionen; Sie fordert, dass MAPI die Verarbeitung der Rückrufe für diese Benachrichtigung sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="641f8-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="641f8-128">Wenn CALLBACK_DISCONTINUE zurückgegeben wird, wird der Parameter _lpUlFlags_ auf NOTIFY_CANCELED festgelegt, wenn er von [IMAPISupport:: notify](imapisupport-notify.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="641f8-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="641f8-129">Die folgenden Einschränkungen gelten für eine synchrone Rückruffunktion:</span><span class="sxs-lookup"><span data-stu-id="641f8-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="641f8-130">Es kann keine weitere synchrone Benachrichtigung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="641f8-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="641f8-131">Eine Benutzeroberfläche kann nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="641f8-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="641f8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="641f8-132">See also</span></span>



[<span data-ttu-id="641f8-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="641f8-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

