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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792711"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="91e31-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="91e31-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="91e31-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91e31-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91e31-105">Synchronisierung für ein Nachrichtenkopf gestartet.</span><span class="sxs-lookup"><span data-stu-id="91e31-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="91e31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e31-106">Parameters</span></span>

 <span data-ttu-id="91e31-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="91e31-107">_cbeid_</span></span>
  
> <span data-ttu-id="91e31-108">[in] Die Anzahl von Bytes in die Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91e31-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="91e31-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="91e31-109">_lpeid_</span></span>
  
> <span data-ttu-id="91e31-110">[in] Die Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91e31-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="91e31-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="91e31-111">_ppv_</span></span>
  
>  <span data-ttu-id="91e31-112">[in] / [out] Zeiger auf die Struktur **[HDRSYNC](hdrsync.md)** für die Nachrichtenkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="91e31-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="91e31-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91e31-113">Remarks</span></span>

<span data-ttu-id="91e31-114">Bei **IOSTX::SyncHdrBeg**Speichern der lokalen Kopie Übergänge, um den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="91e31-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="91e31-115">Outlook initialisiert die **HDRSYNC** -Struktur mit der aktuellen Darstellung der Kopfzeile der Nachricht in den Speicher und die des übergeordneten Ordners für den Client.</span><span class="sxs-lookup"><span data-stu-id="91e31-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="91e31-116">Der Client muss dann eine vollständige e-Mail-Element (als *PmsgFull* in **HDRSYNC** ) heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91e31-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="91e31-117">Wenn dies erfolgreich war, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="91e31-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="91e31-118">Bei **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** Outlook überprüft das Ergebnis in **HDRSYNC** und verwendet die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="91e31-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91e31-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91e31-119">See also</span></span>



[<span data-ttu-id="91e31-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="91e31-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="91e31-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="91e31-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="91e31-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="91e31-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="91e31-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="91e31-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="91e31-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="91e31-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="91e31-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="91e31-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="91e31-126">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="91e31-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="91e31-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="91e31-127">MAPI Constants</span></span>](mapi-constants.md)

