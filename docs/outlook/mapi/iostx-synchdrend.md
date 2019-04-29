---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432772"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="e2ae0-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e2ae0-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="e2ae0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2ae0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2ae0-105">Beendet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="e2ae0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2ae0-106">Parameters</span></span>

 <span data-ttu-id="e2ae0-107">_pProg_</span><span class="sxs-lookup"><span data-stu-id="e2ae0-107">_pprog_</span></span>
  
> <span data-ttu-id="e2ae0-108">in **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschobenen oder kopierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="e2ae0-109">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2ae0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2ae0-110">Remarks</span></span>

<span data-ttu-id="e2ae0-111">Bei **[IOSTX:: SyncBeg](iostx-syncbeg.md)** gibt der lokale Speicher den [Status des Download Nachrichtenkopfs](download-message-header-state.md)ein.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="e2ae0-112">Der Client lädt ein vollständiges Nachrichtenelement (als *pmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="e2ae0-113">Wenn dies erfolgreich ist, legt der Client auch *ulFlags* in **HDRSYNC** als **HSF_OK**fest.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="e2ae0-114">Bei **IOSTX:: SyncHdrEnd**überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet *pProg* und die Informationen in **HDRSYNC** , um den lokalen Nachrichtenkopf zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="e2ae0-115">Der lokale Speicher wird in den Zustand zurückgegeben, in dem er vor dem vorhergehenden **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="e2ae0-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2ae0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2ae0-116">See also</span></span>



[<span data-ttu-id="e2ae0-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e2ae0-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e2ae0-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e2ae0-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="e2ae0-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e2ae0-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="e2ae0-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e2ae0-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e2ae0-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e2ae0-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e2ae0-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e2ae0-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="e2ae0-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2ae0-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="e2ae0-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e2ae0-124">MAPI Constants</span></span>](mapi-constants.md)

