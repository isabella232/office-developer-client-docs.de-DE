---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792718"
---
# <a name="iostxsyncend"></a><span data-ttu-id="d3afc-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="d3afc-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="d3afc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3afc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3afc-105">Synchronisierung in den aktuellen Status beendet und diesen Status beendet.</span><span class="sxs-lookup"><span data-stu-id="d3afc-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="d3afc-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3afc-106">Remarks</span></span>

<span data-ttu-id="d3afc-107">Der Client muss für jeden Aufruf von [IOSTX::SyncBeg](iostx-syncbeg.md) **IOSTX::SyncEnd** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d3afc-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="d3afc-108">Die entsprechenden-Datenstruktur enthält Informationen an, ob der Client den aktuellen Status erfolgreich abgeschlossen wurde, damit der interne Zustand von Outlook bereinigen kann.</span><span class="sxs-lookup"><span data-stu-id="d3afc-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3afc-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3afc-109">See also</span></span>



[<span data-ttu-id="d3afc-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d3afc-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="d3afc-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="d3afc-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="d3afc-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="d3afc-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="d3afc-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="d3afc-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="d3afc-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="d3afc-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="d3afc-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="d3afc-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="d3afc-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3afc-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="d3afc-117">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d3afc-117">MAPI Constants</span></span>](mapi-constants.md)

