---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792708"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="22f11-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="22f11-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="22f11-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22f11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22f11-105">Bereitet den lokalen Speicher für die Synchronisierung in einen bestimmten Status und die erforderliche Informationen zum Replizieren von abgerufen.</span><span class="sxs-lookup"><span data-stu-id="22f11-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="22f11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22f11-106">Parameters</span></span>

 <span data-ttu-id="22f11-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="22f11-107">_uiSync_</span></span>
  
>  <span data-ttu-id="22f11-108">[in] Der Zustand, den der lokale Speicher eingeben möchten.</span><span class="sxs-lookup"><span data-stu-id="22f11-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="22f11-109">Es folgt eine Liste mit IDs Status:</span><span class="sxs-lookup"><span data-stu-id="22f11-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="22f11-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="22f11-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="22f11-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="22f11-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="22f11-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="22f11-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="22f11-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="22f11-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="22f11-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="22f11-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="22f11-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="22f11-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="22f11-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="22f11-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="22f11-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="22f11-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="22f11-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="22f11-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="22f11-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="22f11-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="22f11-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="22f11-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="22f11-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="22f11-121">_ppv_</span></span>
  
>  <span data-ttu-id="22f11-122">[in] / [out] Zeiger auf die Datenstruktur, die den Status entspricht eingeben.</span><span class="sxs-lookup"><span data-stu-id="22f11-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="22f11-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="22f11-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="22f11-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="22f11-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="22f11-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="22f11-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="22f11-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="22f11-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="22f11-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="22f11-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="22f11-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="22f11-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="22f11-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="22f11-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="22f11-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="22f11-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="22f11-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="22f11-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="22f11-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="22f11-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="22f11-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="22f11-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="22f11-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="22f11-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="22f11-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="22f11-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="22f11-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="22f11-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="22f11-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="22f11-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="22f11-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22f11-138">Remarks</span></span>

<span data-ttu-id="22f11-139">Der Client ruft **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** , um das Ergebnis der Synchronisierung festzulegen, und ruft dann **[IOSTX::SyncEnd](iostx-syncend.md)** , um diesen Zustand zu beenden.</span><span class="sxs-lookup"><span data-stu-id="22f11-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="22f11-140">Der Client muss **[IOSTX::SyncEnd](iostx-syncend.md)** für jeden Anruf, um zu bestimmen, ob der Zustand erfolgreich repliziert wurde, **IOSTX::SyncBeg** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22f11-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="22f11-141">Nachdem dies ermittelt wurde, kann Outlook beginnen, bereinigen Sie den internen Zustand.</span><span class="sxs-lookup"><span data-stu-id="22f11-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="22f11-142">Die meisten dieser Strukturen enthalten [out] / [in] Informationen, sodass Outlook zum Übergeben von Informationen an den Client und Client zum Übergeben von Informationen an Outlook.</span><span class="sxs-lookup"><span data-stu-id="22f11-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="22f11-143">Wenn der Client **IOSTX::SyncBeg**aufruft, Outlook weist die Datenstruktur für einen bestimmten Status und mit Informationen für diesen Zustand initialisiert.</span><span class="sxs-lookup"><span data-stu-id="22f11-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="22f11-144">Dies ist die [Out] Informationen.</span><span class="sxs-lookup"><span data-stu-id="22f11-144">This is the [out] information.</span></span> <span data-ttu-id="22f11-145">Klicken Sie in einem Zustand befindet, aktualisiert den Client Datenstruktur des entsprechenden für diesen Zustand.</span><span class="sxs-lookup"><span data-stu-id="22f11-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="22f11-146">Dies ist die [in] Informationen.</span><span class="sxs-lookup"><span data-stu-id="22f11-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22f11-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22f11-147">See also</span></span>



[<span data-ttu-id="22f11-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="22f11-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="22f11-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="22f11-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="22f11-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="22f11-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="22f11-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="22f11-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="22f11-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="22f11-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="22f11-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="22f11-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="22f11-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22f11-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="22f11-155">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="22f11-155">MAPI Constants</span></span>](mapi-constants.md)

