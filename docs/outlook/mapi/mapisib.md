---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f696d9739014659812de3309ec885f37a6f85cc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572137"
---
# <a name="mapisib"></a><span data-ttu-id="dc529-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="dc529-103">MAPISIB</span></span>

  
  
<span data-ttu-id="dc529-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc529-105">Diese Struktur wird mit [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc529-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="dc529-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="dc529-106">Members</span></span>

 <span data-ttu-id="dc529-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="dc529-107">**ulSize**</span></span>
  
> <span data-ttu-id="dc529-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="dc529-108">The size of the structure.</span></span>
    
 <span data-ttu-id="dc529-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="dc529-109">**ulFlags**</span></span>
  
> <span data-ttu-id="dc529-110">Ein Flag, der angibt, welche Art von Synchronisierung. Es muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="dc529-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="dc529-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="dc529-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="dc529-112">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="dc529-112">0x00000200</span></span>  <br/> |<span data-ttu-id="dc529-113">Senden Sie die Nachricht an den Server (derzeit nicht in Verwendung).</span><span class="sxs-lookup"><span data-stu-id="dc529-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="dc529-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="dc529-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="dc529-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc529-115">0x00000001</span></span>  <br/> |<span data-ttu-id="dc529-116">Push-Hierarchie auf dem Server geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dc529-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="dc529-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="dc529-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="dc529-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dc529-118">0x00000002</span></span>  <br/> |<span data-ttu-id="dc529-119">Pull Hierarchie Änderungen vom Server an.</span><span class="sxs-lookup"><span data-stu-id="dc529-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="dc529-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="dc529-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="dc529-121">0 x 00000040</span><span class="sxs-lookup"><span data-stu-id="dc529-121">0x00000040</span></span>  <br/> |<span data-ttu-id="dc529-122">Drücken Sie auf Server Nachricht ändert.</span><span class="sxs-lookup"><span data-stu-id="dc529-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="dc529-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="dc529-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="dc529-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="dc529-124">0x00000080</span></span>  <br/> |<span data-ttu-id="dc529-125">Ziehen Sie Meldung Änderungen vom Server.</span><span class="sxs-lookup"><span data-stu-id="dc529-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="dc529-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="dc529-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="dc529-127">0 x 20000000</span><span class="sxs-lookup"><span data-stu-id="dc529-127">0x20000000</span></span>  <br/> |<span data-ttu-id="dc529-128">Die Synchronisierung wurde vom Benutzer initiiert und eine höhere Priorität sein.</span><span class="sxs-lookup"><span data-stu-id="dc529-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="dc529-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="dc529-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="dc529-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="dc529-130">0x02000000</span></span>  <br/> |<span data-ttu-id="dc529-131">Sollte nur Kopfzeilen und nicht vollständige synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="dc529-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="dc529-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="dc529-132">**psesSync**</span></span>
  
> <span data-ttu-id="dc529-133">[IN] Ein Zeiger auf die MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="dc529-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="dc529-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="dc529-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="dc529-135">[IN] Ein Zeiger auf die Schnittstelle auf dem laufenden bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dc529-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="dc529-136">Die Schnittstelle für Abfragen verwendet werden [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="dc529-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="dc529-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="dc529-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="dc529-138">[OUT] Das Ereignis, das ausgeführt wird, wenn der Thread, der soeben erstellte abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dc529-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="dc529-139">Der Mauszeiger muss gültig sein, da das Ereignis enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="dc529-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc529-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc529-140">See also</span></span>



[<span data-ttu-id="dc529-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc529-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="dc529-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc529-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

