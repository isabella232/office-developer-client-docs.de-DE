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
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792713"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="e9ca1-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e9ca1-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="e9ca1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9ca1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9ca1-105">Synchronisierung für ein Nachrichtenkopf endet.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="e9ca1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9ca1-106">Parameters</span></span>

 <span data-ttu-id="e9ca1-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="e9ca1-107">_pprog_</span></span>
  
> <span data-ttu-id="e9ca1-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschoben oder kopiert Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="e9ca1-109">Finden Sie unter mapidefs.h für die Definition des **LPMAPIPROGRESS**Typs.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e9ca1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9ca1-110">Remarks</span></span>

<span data-ttu-id="e9ca1-111">Gibt ein der lokale Speicher nach **[IOSTX::SyncBeg](iostx-syncbeg.md)** den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca1-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="e9ca1-112">Der Client lädt eine vollständige e-Mail-Element (als *PmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="e9ca1-113">Wenn dies erfolgreich ist, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="e9ca1-114">Bei **IOSTX::SyncHdrEnd**Outlook überprüft das Ergebnis in **HDRSYNC** und *Pprog* und die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="e9ca1-115">Auf den Status, in dem vor den vorherigen **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="e9ca1-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9ca1-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ca1-116">See also</span></span>



[<span data-ttu-id="e9ca1-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e9ca1-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e9ca1-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e9ca1-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="e9ca1-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e9ca1-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="e9ca1-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e9ca1-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e9ca1-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e9ca1-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e9ca1-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e9ca1-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="e9ca1-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9ca1-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="e9ca1-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e9ca1-124">MAPI Constants</span></span>](mapi-constants.md)

