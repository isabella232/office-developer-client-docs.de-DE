---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793139"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="5bfb5-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="5bfb5-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="5bfb5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bfb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bfb5-105">Hierbei handelt es sich um die Benachrichtigung für eine Änderung in den Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="5bfb5-106">Es gibt den Teil des Verbindungsstatus, der geändert wurde, den alten Verbindungsstatus und den neuen Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5bfb5-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5bfb5-107">Quick info</span></span>

<span data-ttu-id="5bfb5-108">Finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="5bfb5-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="5bfb5-109">Members</span></span>

 <span data-ttu-id="5bfb5-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-110">_ulSize_</span></span>
  
> <span data-ttu-id="5bfb5-111">Größe der Struktur **MAPIOFFLINE_NOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="5bfb5-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="5bfb5-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-112">_NotifyType_</span></span>
  
> <span data-ttu-id="5bfb5-113">Typ der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-113">Type of notification.</span></span> <span data-ttu-id="5bfb5-114">Beachten Sie, dass nur Benachrichtigung über die Änderung der Verbindungsstatus unterstützt wird. Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="5bfb5-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="5bfb5-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="5bfb5-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="5bfb5-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="5bfb5-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="5bfb5-119">Ein Token vom Client in der Struktur **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** definiert.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="5bfb5-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-120">_ulMask_</span></span>
  
> <span data-ttu-id="5bfb5-121">Der Teil der Status der Verbindung, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="5bfb5-122">Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="5bfb5-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="5bfb5-124">Die alte Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-124">The old connection state.</span></span> <span data-ttu-id="5bfb5-125">Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="5bfb5-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="5bfb5-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="5bfb5-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="5bfb5-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="5bfb5-129">Die neue Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-129">The new connection state.</span></span> <span data-ttu-id="5bfb5-130">Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="5bfb5-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="5bfb5-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bfb5-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bfb5-133">Remarks</span></span>

<span data-ttu-id="5bfb5-134">Die Offline Zustand API unterstützt nur Benachrichtigungen für Online-/offline geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="5bfb5-135">Ein Client muss überprüfen, dass Outlook die folgenden Werte zurückgibt, bevor Sie die eigentliche Änderung untersuchen:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="5bfb5-136">*NotifyType* hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="5bfb5-137">In diesem Fall kann der Client wird vorausgesetzt, dass die Änderung eine Verbindung Zustand ist und *Info* der Struktur *StateChange* ist.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="5bfb5-138">*UlMask* hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="5bfb5-139">In diesem Fall kann der Client wird vorausgesetzt, dass die Änderung eine Änderung der Verbindung online/offline-Status ist, und mit *UlStateOld* und *UlStateNew* untersuchen fortfahren kann.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="5bfb5-140">Es ist möglich, dass Outlook einen Client weitere Änderungen darüber informiert werden, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="5bfb5-141">In solchen Fällen *NotifyType* wäre nicht eine der drei Werte zuvor erwähnt oder *UlMask* wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss den Rest der Daten in *Info* ignorieren.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bfb5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfb5-142">See also</span></span>

- [<span data-ttu-id="5bfb5-143">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="5bfb5-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="5bfb5-144">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="5bfb5-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="5bfb5-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="5bfb5-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

