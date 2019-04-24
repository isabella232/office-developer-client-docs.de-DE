---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317157"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="87da0-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="87da0-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="87da0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87da0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87da0-105">Startet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="87da0-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="87da0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87da0-106">Parameters</span></span>

 <span data-ttu-id="87da0-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="87da0-107">_cbeid_</span></span>
  
> <span data-ttu-id="87da0-108">in Die Anzahl der Bytes in der Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="87da0-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="87da0-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="87da0-109">_lpeid_</span></span>
  
> <span data-ttu-id="87da0-110">in Die Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="87da0-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="87da0-111">_PPV_</span><span class="sxs-lookup"><span data-stu-id="87da0-111">_ppv_</span></span>
  
>  <span data-ttu-id="87da0-112">[in]/[out] Zeiger auf die **[HDRSYNC](hdrsync.md)** -Struktur für den Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="87da0-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87da0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87da0-113">Remarks</span></span>

<span data-ttu-id="87da0-114">Bei **IOSTX:: SyncHdrBeg**wechselt der lokale Speicher in den [Status des Download Nachrichtenkopfs](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="87da0-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="87da0-115">Outlook initialisiert für den Client die **HDRSYNC** -Struktur mit der aktuellen Darstellung des Nachrichtenkopfs im Store und dem übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="87da0-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="87da0-116">Der Client muss dann ein vollständiges Nachrichtenelement (als *pmsgFull* in **HDRSYNC** ) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="87da0-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="87da0-117">Wenn dies erfolgreich war, legt der Client auch *ulFlags* in **HDRSYNC** als **HSF_OK**fest.</span><span class="sxs-lookup"><span data-stu-id="87da0-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="87da0-118">Bei **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet die Informationen in **HDRSYNC** zum Aktualisieren des lokalen Nachrichtenkopfs.</span><span class="sxs-lookup"><span data-stu-id="87da0-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87da0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87da0-119">See also</span></span>



[<span data-ttu-id="87da0-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="87da0-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="87da0-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="87da0-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="87da0-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="87da0-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="87da0-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="87da0-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="87da0-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="87da0-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="87da0-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="87da0-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="87da0-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87da0-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="87da0-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="87da0-127">MAPI Constants</span></span>](mapi-constants.md)

