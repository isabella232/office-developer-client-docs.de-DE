---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795795"
---
# <a name="updele"></a><span data-ttu-id="4ed05-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="4ed05-103">UPDELE</span></span>

<span data-ttu-id="4ed05-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ed05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ed05-105">Erweiterte Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4ed05-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="4ed05-106">Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ed05-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ed05-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4ed05-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="4ed05-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4ed05-108">Members</span></span>

<span data-ttu-id="4ed05-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ed05-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4ed05-110">[Out] / [in] Flags, die entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4ed05-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="4ed05-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="4ed05-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="4ed05-112">[out] Element ist verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4ed05-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="4ed05-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="4ed05-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="4ed05-114">[out] Element wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="4ed05-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="4ed05-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="4ed05-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="4ed05-116">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4ed05-116">[in] Upload was successful.</span></span> <span data-ttu-id="4ed05-117">Der Client legt dies nach dem Hochladen von Informationen zum Server.</span><span class="sxs-lookup"><span data-stu-id="4ed05-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="4ed05-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="4ed05-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="4ed05-119">[in] Element wurde erfolgreich verschoben.</span><span class="sxs-lookup"><span data-stu-id="4ed05-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="4ed05-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="4ed05-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="4ed05-121">[in] Mark Quellelement als geändert.</span><span class="sxs-lookup"><span data-stu-id="4ed05-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="4ed05-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="4ed05-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="4ed05-123">[in] Commit jetzt Upload-Status (Eintrag 0).</span><span class="sxs-lookup"><span data-stu-id="4ed05-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="4ed05-124">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="4ed05-124">_skey_</span></span>
  
> <span data-ttu-id="4ed05-125">[out] Quellschlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="4ed05-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="4ed05-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="4ed05-126">_dwReserved_</span></span>
  
> <span data-ttu-id="4ed05-127">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ed05-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="4ed05-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="4ed05-128">_binChg_</span></span>
  
> <span data-ttu-id="4ed05-129">[out] Ändern Sie Schlüssel des Zielelement, wenn Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="4ed05-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4ed05-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="4ed05-130">_binPcl_</span></span>
  
> <span data-ttu-id="4ed05-131">[out] Ändern Sie Liste der Zielelement, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="4ed05-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4ed05-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="4ed05-132">_skeyDst_</span></span>
  
> <span data-ttu-id="4ed05-133">[out] Schlüssel Source Ziel-Elements, wenn das Element wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="4ed05-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4ed05-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="4ed05-134">_pupmov_</span></span>
  
> <span data-ttu-id="4ed05-135">[out] Ordnerinformationen Ziel, wenn das Element wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="4ed05-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ed05-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ed05-136">See also</span></span>

- [<span data-ttu-id="4ed05-137">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4ed05-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="4ed05-138">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4ed05-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4ed05-139">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4ed05-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="4ed05-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="4ed05-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="4ed05-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="4ed05-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="4ed05-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="4ed05-142">UPMOV</span></span>](upmov.md)

