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
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411939"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="11c09-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="11c09-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="11c09-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c09-105">Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.</span><span class="sxs-lookup"><span data-stu-id="11c09-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="11c09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c09-106">Parameters</span></span>

 <span data-ttu-id="11c09-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="11c09-107">_uiSync_</span></span>
  
>  <span data-ttu-id="11c09-108">in Der Zustand, der vom lokalen Speicher eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11c09-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="11c09-109">Es folgt eine Liste der Status Identifier:</span><span class="sxs-lookup"><span data-stu-id="11c09-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="11c09-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="11c09-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="11c09-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="11c09-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="11c09-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="11c09-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="11c09-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="11c09-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="11c09-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="11c09-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="11c09-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="11c09-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="11c09-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="11c09-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="11c09-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="11c09-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="11c09-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="11c09-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="11c09-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="11c09-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="11c09-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="11c09-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="11c09-121">_PPV_</span><span class="sxs-lookup"><span data-stu-id="11c09-121">_ppv_</span></span>
  
>  <span data-ttu-id="11c09-122">[in]/[out] Zeiger auf die Datenstruktur, die dem zu gebenden Zustand entspricht.</span><span class="sxs-lookup"><span data-stu-id="11c09-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="11c09-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="11c09-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="11c09-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="11c09-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="11c09-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="11c09-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="11c09-126">SYNCHRONISIERUNGS</span><span class="sxs-lookup"><span data-stu-id="11c09-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="11c09-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="11c09-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="11c09-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="11c09-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="11c09-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="11c09-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="11c09-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="11c09-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="11c09-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="11c09-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="11c09-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="11c09-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="11c09-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="11c09-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="11c09-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="11c09-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="11c09-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="11c09-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="11c09-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="11c09-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="11c09-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="11c09-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="11c09-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11c09-138">Remarks</span></span>

<span data-ttu-id="11c09-139">Der Client ruft **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** auf, um das Ergebnis der Synchronisierung festzulegen, und ruft dann **[IOSTX:: SyncEnd](iostx-syncend.md)** auf, um diesen Status zu beenden.</span><span class="sxs-lookup"><span data-stu-id="11c09-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="11c09-140">Der Client muss **[IOSTX:: SyncEnd](iostx-syncend.md)** für jeden Aufruf von **IOSTX:: SyncBeg** aufrufen, um zu bestimmen, ob der Status erfolgreich repliziert wurde.</span><span class="sxs-lookup"><span data-stu-id="11c09-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="11c09-141">Nachdem dies bestimmt wurde, kann Outlook beginnen, den internen Status zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="11c09-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="11c09-142">Die meisten dieser Strukturen enthalten [out]/[in]-Informationen, sodass Outlook Informationen an den Client und den Client weitergeleitet werden kann, um Informationen an Outlook zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="11c09-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="11c09-143">Wenn der Client **IOSTX:: SyncBeg**aufruft, weist Outlook die Datenstruktur für einen bestimmten Zustand zu und initialisiert sie mit Informationen für diesen Status.</span><span class="sxs-lookup"><span data-stu-id="11c09-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="11c09-144">Dies sind die [out]-Informationen.</span><span class="sxs-lookup"><span data-stu-id="11c09-144">This is the [out] information.</span></span> <span data-ttu-id="11c09-145">In einem Zustand aktualisiert der Client die entsprechende Datenstruktur für diesen Status.</span><span class="sxs-lookup"><span data-stu-id="11c09-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="11c09-146">Dies sind die [in]-Informationen.</span><span class="sxs-lookup"><span data-stu-id="11c09-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11c09-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c09-147">See also</span></span>



[<span data-ttu-id="11c09-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="11c09-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="11c09-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="11c09-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="11c09-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="11c09-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="11c09-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="11c09-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="11c09-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="11c09-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="11c09-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="11c09-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="11c09-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11c09-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="11c09-155">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="11c09-155">MAPI Constants</span></span>](mapi-constants.md)

