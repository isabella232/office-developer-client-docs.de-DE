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
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421739"
---
# <a name="imapiofflinesetcurrentstate"></a><span data-ttu-id="d6de8-103">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d6de8-103">IMAPIOffline::SetCurrentState</span></span>

  
  
<span data-ttu-id="d6de8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6de8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6de8-105">Legt den aktuellen Status eines Offlineobjekts auf Online oder Offline fest.</span><span class="sxs-lookup"><span data-stu-id="d6de8-105">Sets the current state of an offline object to online or offline.</span></span>
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a><span data-ttu-id="d6de8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6de8-106">Parameters</span></span>

 <span data-ttu-id="d6de8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6de8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d6de8-108">[in] Ändert das Verhalten dieses Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="d6de8-108">[in] Modifies the behavior of this call.</span></span> <span data-ttu-id="d6de8-109">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d6de8-109">The supported values are:</span></span>
    
<span data-ttu-id="d6de8-110">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="d6de8-110">MAPIOFFLINE_FLAG_BLOCK</span></span>
  
> <span data-ttu-id="d6de8-111">Durch  _Festlegen von ulFlags_ auf diesen Wert wird der **SetCurrentState-Aufruf** blockiert, bis die Statusänderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d6de8-111">Setting  _ulFlags_ to this value will block the **SetCurrentState** call until the state change is complete.</span></span> <span data-ttu-id="d6de8-112">Standardmäßig erfolgt der Übergang asynchron.</span><span class="sxs-lookup"><span data-stu-id="d6de8-112">By default the transition takes place asynchronously.</span></span> <span data-ttu-id="d6de8-113">Wenn der Übergang asynchron erfolgt, werden alle **SetCurrentState-Aufrufe** **E_PENDING,** bis die Änderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d6de8-113">When the transition is occuring asynchronously, all **SetCurrentState** calls will return **E_PENDING** until the change is complete.</span></span> 
    
<span data-ttu-id="d6de8-114">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d6de8-114">MAPIOFFLINE_FLAG_DEFAULT</span></span>
  
> <span data-ttu-id="d6de8-115">Legt den aktuellen Status fest, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="d6de8-115">Sets the current state without blocking.</span></span>
    
 <span data-ttu-id="d6de8-116">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="d6de8-116">_ulMask_</span></span>
  
> <span data-ttu-id="d6de8-117">[in] Der Teil des zu ändernde Zustands.</span><span class="sxs-lookup"><span data-stu-id="d6de8-117">[in] The part of the state to change.</span></span> <span data-ttu-id="d6de8-118">Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="d6de8-118">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="d6de8-119">_ulState_</span><span class="sxs-lookup"><span data-stu-id="d6de8-119">_ulState_</span></span>
  
> <span data-ttu-id="d6de8-120">[in] Der Zustand, in den geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6de8-120">[in] The state to change to.</span></span> <span data-ttu-id="d6de8-121">Dabei muss es sich um einen der beiden folgenden Werte handelt:</span><span class="sxs-lookup"><span data-stu-id="d6de8-121">It must be one of these two values:</span></span>
    
<span data-ttu-id="d6de8-122">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d6de8-122">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="d6de8-123">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d6de8-123">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
 <span data-ttu-id="d6de8-124">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="d6de8-124">_pReserved_</span></span>
  
> <span data-ttu-id="d6de8-125">Dieser Parameter ist für die Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6de8-125">This parameter is reserved for Outlook internal use and is not supported.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6de8-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6de8-126">Return value</span></span>

<span data-ttu-id="d6de8-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6de8-127">S_OK</span></span>
  
> <span data-ttu-id="d6de8-128">Der Status des Offlineobjekts wurde erfolgreich geändert.</span><span class="sxs-lookup"><span data-stu-id="d6de8-128">The state of the offline object has been changed successfully.</span></span>
    
<span data-ttu-id="d6de8-129">E_PENDING</span><span class="sxs-lookup"><span data-stu-id="d6de8-129">E_PENDING</span></span>
  
> <span data-ttu-id="d6de8-130">Dies bedeutet, dass sich der Status des Offlineobjekts asynchron ändert.</span><span class="sxs-lookup"><span data-stu-id="d6de8-130">This indicates that the state of the offline object is changing asynchronously.</span></span> <span data-ttu-id="d6de8-131">Dies tritt auf, wenn  _ulFlags_ in einem früheren **SetCurrentState-Aufruf** auf MAPIOFFLINE_FLAG_BLOCK festgelegt ist und jeder nachfolgende **SetCurrentState-Aufruf** diesen Wert zurück gibt, bis die asynchrone Zustandsänderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d6de8-131">This occurs when  _ulFlags_ is set to MAPIOFFLINE_FLAG_BLOCK in an earlier **SetCurrentState** call, and any subsequent **SetCurrentState** call will return this value until the asynchronous state change is complete.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d6de8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6de8-132">See also</span></span>



[<span data-ttu-id="d6de8-133">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d6de8-133">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="d6de8-134">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d6de8-134">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)


[<span data-ttu-id="d6de8-135">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d6de8-135">MAPI Constants</span></span>](mapi-constants.md)

