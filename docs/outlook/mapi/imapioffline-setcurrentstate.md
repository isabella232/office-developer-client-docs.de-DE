---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15e2d5c2aca595c3a06d215cd069c23da3e48125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792243"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="f084d-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="f084d-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="f084d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f084d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f084d-105">Legt den aktuellen Zustand eines offline-Objekts zu online oder offline.</span><span class="sxs-lookup"><span data-stu-id="f084d-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="f084d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f084d-106">Parameters</span></span>

 <span data-ttu-id="f084d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f084d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f084d-108">[in] Ändert das Verhalten dieses Anrufs.</span><span class="sxs-lookup"><span data-stu-id="f084d-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="f084d-109">Die unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f084d-109">The supported values are:</span></span>
    
<span data-ttu-id="f084d-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="f084d-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="f084d-111">_UlFlags_ auf diesen Wert festlegen blockiert den Anruf **SetCurrentState** , bis die Änderung der Status abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f084d-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="f084d-112">Standardmäßig erfolgt der Übergang asynchron.</span><span class="sxs-lookup"><span data-stu-id="f084d-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="f084d-113">Beim Übergang asynchron vorliegt, gibt alle **SetCurrentState** Anrufe **E_PENDING** zurück, bis die Änderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f084d-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="f084d-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f084d-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="f084d-115">Legt den aktuellen Status ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="f084d-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="f084d-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="f084d-116">_ulMask_</span></span>
  
> <span data-ttu-id="f084d-117">[in] Der Teil des Status zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f084d-117">[in] The part of the state to change.</span></span> <span data-ttu-id="f084d-118">Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="f084d-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="f084d-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="f084d-119">_ulState_</span></span>
  
> <span data-ttu-id="f084d-120">[in] Der Zustand, zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f084d-120">[in] The state to change to.</span></span> <span data-ttu-id="f084d-121">Es muss eine der folgenden zwei Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f084d-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="f084d-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="f084d-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="f084d-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="f084d-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="f084d-124">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="f084d-124">_pReserved_</span></span>
  
> <span data-ttu-id="f084d-125">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f084d-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f084d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f084d-126">Return value</span></span>

<span data-ttu-id="f084d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="f084d-127">S_OK</span></span>
  
> <span data-ttu-id="f084d-128">Der Status des offline-Objekts wurde erfolgreich geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f084d-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="f084d-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="f084d-129">E_PENDING</span></span>
  
> <span data-ttu-id="f084d-130">Dies gibt an, dass der Zustand des offline-Objekts asynchron geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f084d-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="f084d-131">Dies tritt auf, wenn _UlFlags_ auf MAPIOFFLINE_FLAG_BLOCK in einem früheren **SetCurrentState** Aufruf festgelegt ist, und alle nachfolgender **SetCurrentState** Aufruf diesen Wert, bis zum Abschluss der asynchronen Zustand ändern zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="f084d-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f084d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f084d-132">See also</span></span>



[<span data-ttu-id="f084d-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="f084d-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="f084d-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="f084d-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="f084d-135">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f084d-135">MAPI Constants</span></span>](mapi-constants.md)

