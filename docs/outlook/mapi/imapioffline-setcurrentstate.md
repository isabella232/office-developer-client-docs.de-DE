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
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567139"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="ea26c-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ea26c-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="ea26c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea26c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea26c-105">Legt den aktuellen Zustand eines offline-Objekts zu online oder offline.</span><span class="sxs-lookup"><span data-stu-id="ea26c-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="ea26c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea26c-106">Parameters</span></span>

 <span data-ttu-id="ea26c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ea26c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ea26c-108">[in] Ändert das Verhalten dieses Anrufs.</span><span class="sxs-lookup"><span data-stu-id="ea26c-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="ea26c-109">Die unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ea26c-109">The supported values are:</span></span>
    
<span data-ttu-id="ea26c-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="ea26c-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="ea26c-111">_UlFlags_ auf diesen Wert festlegen blockiert den Anruf **SetCurrentState** , bis die Änderung der Status abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ea26c-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="ea26c-112">Standardmäßig erfolgt der Übergang asynchron.</span><span class="sxs-lookup"><span data-stu-id="ea26c-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="ea26c-113">Beim Übergang asynchron vorliegt, gibt alle **SetCurrentState** Anrufe **E_PENDING** zurück, bis die Änderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ea26c-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="ea26c-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ea26c-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="ea26c-115">Legt den aktuellen Status ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="ea26c-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="ea26c-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="ea26c-116">_ulMask_</span></span>
  
> <span data-ttu-id="ea26c-117">[in] Der Teil des Status zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ea26c-117">[in] The part of the state to change.</span></span> <span data-ttu-id="ea26c-118">Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="ea26c-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="ea26c-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="ea26c-119">_ulState_</span></span>
  
> <span data-ttu-id="ea26c-120">[in] Der Zustand, zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ea26c-120">[in] The state to change to.</span></span> <span data-ttu-id="ea26c-121">Es muss eine der folgenden zwei Werte sein:</span><span class="sxs-lookup"><span data-stu-id="ea26c-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="ea26c-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ea26c-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="ea26c-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ea26c-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="ea26c-124">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="ea26c-124">_pReserved_</span></span>
  
> <span data-ttu-id="ea26c-125">Dieser Parameter ist für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea26c-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ea26c-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ea26c-126">Return value</span></span>

<span data-ttu-id="ea26c-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea26c-127">S_OK</span></span>
  
> <span data-ttu-id="ea26c-128">Der Status des offline-Objekts wurde erfolgreich geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ea26c-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="ea26c-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="ea26c-129">E_PENDING</span></span>
  
> <span data-ttu-id="ea26c-130">Dies gibt an, dass der Zustand des offline-Objekts asynchron geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ea26c-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="ea26c-131">Dies tritt auf, wenn _UlFlags_ auf MAPIOFFLINE_FLAG_BLOCK in einem früheren **SetCurrentState** Aufruf festgelegt ist, und alle nachfolgender **SetCurrentState** Aufruf diesen Wert, bis zum Abschluss der asynchronen Zustand ändern zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="ea26c-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ea26c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea26c-132">See also</span></span>



[<span data-ttu-id="ea26c-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ea26c-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="ea26c-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ea26c-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="ea26c-135">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea26c-135">MAPI Constants</span></span>](mapi-constants.md)

