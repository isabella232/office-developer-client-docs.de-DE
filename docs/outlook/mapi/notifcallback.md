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
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793287"
---
# <a name="notifcallback"></a><span data-ttu-id="25501-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="25501-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="25501-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25501-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25501-105">Definiert eine Rückruffunktion, die MAPI senden eine ereignisbenachrichtigung aufruft.</span><span class="sxs-lookup"><span data-stu-id="25501-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="25501-106">Diese Callback-Funktion kann nur verwendet werden, wenn in einer Advise-Empfängerobjekt erstellt durch Aufrufen der Funktion [HrAllocAdviseSink](hrallocadvisesink.md) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="25501-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25501-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="25501-107">Header file:</span></span>  <br/> |<span data-ttu-id="25501-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25501-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25501-109">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="25501-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="25501-110">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="25501-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="25501-111">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="25501-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="25501-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="25501-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="25501-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="25501-113">Parameters</span></span>

 <span data-ttu-id="25501-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="25501-114">_lpvContext_</span></span>
  
> <span data-ttu-id="25501-115">[in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="25501-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="25501-116">Dieser Wert kann eine Bedeutung für die Clientanwendung oder Dienstanbieter-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="25501-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="25501-117">In der Regel stellt der _LpvContext_ -Parameter für C++-Code einen Zeiger auf ein C++-Objekt.</span><span class="sxs-lookup"><span data-stu-id="25501-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="25501-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="25501-118">_cNotification_</span></span>
  
> <span data-ttu-id="25501-119">[in] Anzahl der ereignisbenachrichtigungen im Array durch den Parameter _LpNotifications_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="25501-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="25501-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="25501-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="25501-121">[out] Zeiger auf den Speicherort, in dem diese Funktion ein Array von [Benachrichtigung](notification.md) Strukturen, schreibt, enthält die ereignisbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="25501-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="25501-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25501-122">Return value</span></span>

<span data-ttu-id="25501-123">Der Satz von gültigen Rückgabewerte für die **NOTIFCALLBACK** Funktionsprototyp hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="25501-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="25501-124">Clients sollte immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="25501-124">Clients should always return S_OK.</span></span> <span data-ttu-id="25501-125">Anbieter können S_OK oder CALLBACK_DISCONTINUE zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="25501-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25501-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25501-126">Remarks</span></span>

<span data-ttu-id="25501-127">CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert für nur synchrone Rückruffunktionen. fordert, dass MAPI sofort Beenden der Verarbeitung der Rückrufe für diese Benachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="25501-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="25501-128">Wenn CALLBACK_DISCONTINUE zurückgegeben wird, wird MAPI der _LpUlFlags_ -Parameter auf NOTIFY_CANCELED, wenn es vom [IMAPISupport::Notify](imapisupport-notify.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="25501-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="25501-129">Im folgenden sind Einschränkungen auf was eine synchrone Callback-Funktion möglich:</span><span class="sxs-lookup"><span data-stu-id="25501-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="25501-130">Es kann nicht dazu führen, dass eine andere synchrone Benachrichtigung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25501-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="25501-131">Es kann keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25501-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25501-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25501-132">See also</span></span>



[<span data-ttu-id="25501-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="25501-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

