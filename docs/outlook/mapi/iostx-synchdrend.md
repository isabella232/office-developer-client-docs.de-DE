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
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591331"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="cf69a-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="cf69a-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="cf69a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf69a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf69a-105">Synchronisierung für ein Nachrichtenkopf endet.</span><span class="sxs-lookup"><span data-stu-id="cf69a-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="cf69a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf69a-106">Parameters</span></span>

 <span data-ttu-id="cf69a-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="cf69a-107">_pprog_</span></span>
  
> <span data-ttu-id="cf69a-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschoben oder kopiert Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="cf69a-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="cf69a-109">Finden Sie unter mapidefs.h für die Definition des **LPMAPIPROGRESS**Typs.</span><span class="sxs-lookup"><span data-stu-id="cf69a-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf69a-110">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cf69a-110">Remarks</span></span>

<span data-ttu-id="cf69a-111">Gibt ein der lokale Speicher nach **[IOSTX::SyncBeg](iostx-syncbeg.md)** den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="cf69a-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="cf69a-112">Der Client lädt eine vollständige e-Mail-Element (als *PmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter.</span><span class="sxs-lookup"><span data-stu-id="cf69a-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="cf69a-113">Wenn dies erfolgreich ist, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="cf69a-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="cf69a-114">Bei **IOSTX::SyncHdrEnd**Outlook überprüft das Ergebnis in **HDRSYNC** und *Pprog* und die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf69a-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="cf69a-115">Auf den Status, in dem vor den vorherigen **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="cf69a-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf69a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf69a-116">See also</span></span>



[<span data-ttu-id="cf69a-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="cf69a-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="cf69a-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="cf69a-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="cf69a-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="cf69a-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="cf69a-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="cf69a-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="cf69a-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="cf69a-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="cf69a-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="cf69a-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="cf69a-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf69a-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="cf69a-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="cf69a-124">MAPI Constants</span></span>](mapi-constants.md)

