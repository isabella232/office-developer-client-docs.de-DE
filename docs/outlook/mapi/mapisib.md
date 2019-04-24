---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270210"
---
# <a name="mapisib"></a><span data-ttu-id="3bafa-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="3bafa-103">MAPISIB</span></span>

  
  
<span data-ttu-id="3bafa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bafa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bafa-105">Diese Struktur wird mit [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bafa-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="3bafa-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="3bafa-106">Members</span></span>

 <span data-ttu-id="3bafa-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="3bafa-107">**ulSize**</span></span>
  
> <span data-ttu-id="3bafa-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="3bafa-108">The size of the structure.</span></span>
    
 <span data-ttu-id="3bafa-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3bafa-109">**ulFlags**</span></span>
  
> <span data-ttu-id="3bafa-110">Ein Flag, das den Synchronisierungs angibt. Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="3bafa-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="3bafa-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="3bafa-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="3bafa-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="3bafa-112">0x00000200</span></span>  <br/> |<span data-ttu-id="3bafa-113">Senden Sie die Nachricht an den Server (derzeit nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="3bafa-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="3bafa-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3bafa-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="3bafa-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3bafa-115">0x00000001</span></span>  <br/> |<span data-ttu-id="3bafa-116">Hierarchieänderungen auf dem Server pushen.</span><span class="sxs-lookup"><span data-stu-id="3bafa-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="3bafa-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3bafa-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="3bafa-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3bafa-118">0x00000002</span></span>  <br/> |<span data-ttu-id="3bafa-119">Hierarchieänderungen vom Server abrufen.</span><span class="sxs-lookup"><span data-stu-id="3bafa-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="3bafa-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3bafa-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="3bafa-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="3bafa-121">0x00000040</span></span>  <br/> |<span data-ttu-id="3bafa-122">Push Message Changes to Server.</span><span class="sxs-lookup"><span data-stu-id="3bafa-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="3bafa-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3bafa-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="3bafa-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3bafa-124">0x00000080</span></span>  <br/> |<span data-ttu-id="3bafa-125">Nachrichtenänderungen vom Server abrufen.</span><span class="sxs-lookup"><span data-stu-id="3bafa-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="3bafa-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="3bafa-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="3bafa-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="3bafa-127">0x20000000</span></span>  <br/> |<span data-ttu-id="3bafa-128">Die Synchronisierung wurde vom Benutzer initiiert und sollte eine höhere Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="3bafa-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="3bafa-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3bafa-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="3bafa-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="3bafa-130">0x02000000</span></span>  <br/> |<span data-ttu-id="3bafa-131">Sollte nur Kopfzeilen und keine vollständigen Körper synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3bafa-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="3bafa-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="3bafa-132">**psesSync**</span></span>
  
> <span data-ttu-id="3bafa-133">IN Ein Zeiger auf die MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3bafa-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="3bafa-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="3bafa-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="3bafa-135">IN Ein Zeiger auf die Schnittstelle, für die der Fortschritt bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bafa-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="3bafa-136">Sie kann zum Abfragen der Schnittstelle für [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bafa-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="3bafa-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="3bafa-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="3bafa-138">Out Das Ereignis, das auftritt, wenn der soeben erstellte Thread abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3bafa-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="3bafa-139">Der Zeiger muss gültig sein, da er das Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="3bafa-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bafa-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bafa-140">See also</span></span>



[<span data-ttu-id="3bafa-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bafa-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="3bafa-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bafa-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

