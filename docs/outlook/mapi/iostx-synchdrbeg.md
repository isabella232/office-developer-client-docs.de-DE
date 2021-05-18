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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405093"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="60023-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="60023-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="60023-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60023-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60023-105">Startet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="60023-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="60023-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60023-106">Parameters</span></span>

 <span data-ttu-id="60023-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="60023-107">_cbeid_</span></span>
  
> <span data-ttu-id="60023-108">[in] Die Anzahl der Bytes in der Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="60023-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="60023-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="60023-109">_lpeid_</span></span>
  
> <span data-ttu-id="60023-110">[in] Die Eintrags-ID für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="60023-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="60023-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="60023-111">_ppv_</span></span>
  
>  <span data-ttu-id="60023-112">[in]/[out] Zeiger auf die **[HDRSYNC-Struktur](hdrsync.md)** für den Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="60023-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="60023-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60023-113">Remarks</span></span>

<span data-ttu-id="60023-114">Bei **IOSTX::SyncHdrBeg** überwechselt der lokale Speicher den Status ["Nachrichtenkopf herunterladen".](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="60023-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="60023-115">Outlook für den Client die **HDRSYNC-Struktur** mit der aktuellen Darstellung des Nachrichtenkopfs im Speicher und im übergeordneten Ordner initialisiert.</span><span class="sxs-lookup"><span data-stu-id="60023-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="60023-116">Der Client muss dann ein vollständiges Nachrichtenelement herunterladen (als  *pmsgFull*  in **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="60023-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="60023-117">Wenn dies erfolgreich war, legt der Client *auch ulFlags* in **HDRSYNC als** **HSF_OK.**</span><span class="sxs-lookup"><span data-stu-id="60023-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="60023-118">Bei **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet die Informationen in **HDRSYNC,** um den lokalen Nachrichtenkopf zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="60023-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60023-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60023-119">See also</span></span>



[<span data-ttu-id="60023-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="60023-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="60023-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="60023-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="60023-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="60023-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="60023-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="60023-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="60023-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="60023-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="60023-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="60023-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="60023-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60023-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="60023-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="60023-127">MAPI Constants</span></span>](mapi-constants.md)

