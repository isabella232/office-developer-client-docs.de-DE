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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439576"
---
# <a name="iostxsyncend"></a><span data-ttu-id="1b248-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="1b248-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="1b248-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b248-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b248-105">Beendet die Synchronisierung im aktuellen Zustand und beendet den Status.</span><span class="sxs-lookup"><span data-stu-id="1b248-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="1b248-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b248-106">Remarks</span></span>

<span data-ttu-id="1b248-107">Der Client muss **IOSTX::SyncEnd** für jeden Aufruf von [IOSTX::SyncBeg aufrufen.](iostx-syncbeg.md)</span><span class="sxs-lookup"><span data-stu-id="1b248-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="1b248-108">Die entsprechende Datenstruktur enthält Informationen, um anzugeben, ob der Client den aktuellen Status erfolgreich abgeschlossen hat, damit Outlook internen Zustand bereinigen kann.</span><span class="sxs-lookup"><span data-stu-id="1b248-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b248-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b248-109">See also</span></span>



[<span data-ttu-id="1b248-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b248-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="1b248-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="1b248-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="1b248-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="1b248-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="1b248-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="1b248-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="1b248-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="1b248-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="1b248-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="1b248-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="1b248-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b248-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="1b248-117">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1b248-117">MAPI Constants</span></span>](mapi-constants.md)

