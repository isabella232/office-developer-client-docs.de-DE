---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432870"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="ddcfe-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="ddcfe-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="ddcfe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddcfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddcfe-105">Legt das Ergebnis der Synchronisierung fest.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="ddcfe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddcfe-106">Parameters</span></span>

 <span data-ttu-id="ddcfe-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="ddcfe-107">_hrSync_</span></span>
  
>  <span data-ttu-id="ddcfe-108">[in] Das Ergebnis der Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ddcfe-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ddcfe-109">Remarks</span></span>

<span data-ttu-id="ddcfe-110">Rufen **Sie IOSTX::SetSyncResult auf,** bevor **Sie IOSTX::SyncEnd** aufrufen, um den lokalen Speicher über das Ergebnis der Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddcfe-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddcfe-111">See also</span></span>



[<span data-ttu-id="ddcfe-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ddcfe-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="ddcfe-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="ddcfe-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="ddcfe-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="ddcfe-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="ddcfe-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="ddcfe-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="ddcfe-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="ddcfe-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="ddcfe-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="ddcfe-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="ddcfe-118">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ddcfe-118">MAPI Constants</span></span>](mapi-constants.md)

