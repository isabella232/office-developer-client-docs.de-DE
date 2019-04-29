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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424882"
---
# <a name="updele"></a><span data-ttu-id="8616c-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="8616c-103">UPDELE</span></span>

<span data-ttu-id="8616c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8616c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8616c-105">Erweiterte Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="8616c-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="8616c-106">Diese Informationen werden während des Status Status des [Uploads gelöscht](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="8616c-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8616c-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8616c-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8616c-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="8616c-108">Members</span></span>

<span data-ttu-id="8616c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8616c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8616c-110">[out]/[in] Flags zur Bestimmung des geeigneten Verhaltens beim Hochladen.</span><span class="sxs-lookup"><span data-stu-id="8616c-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="8616c-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="8616c-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="8616c-112">Out Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8616c-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="8616c-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="8616c-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="8616c-114">Out Das Element wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="8616c-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="8616c-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="8616c-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="8616c-116">in Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8616c-116">[in] Upload was successful.</span></span> <span data-ttu-id="8616c-117">Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="8616c-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="8616c-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="8616c-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="8616c-119">in Das Element wurde erfolgreich verschoben.</span><span class="sxs-lookup"><span data-stu-id="8616c-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="8616c-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="8616c-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="8616c-121">in Quellelement als geändert markieren.</span><span class="sxs-lookup"><span data-stu-id="8616c-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="8616c-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="8616c-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="8616c-123">in Commit-Uploadstatus Now (Entry 0).</span><span class="sxs-lookup"><span data-stu-id="8616c-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="8616c-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="8616c-124">_skey_</span></span>
  
> <span data-ttu-id="8616c-125">Out Quellschlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="8616c-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="8616c-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="8616c-126">_dwReserved_</span></span>
  
> <span data-ttu-id="8616c-127">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8616c-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="8616c-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="8616c-128">_binChg_</span></span>
  
> <span data-ttu-id="8616c-129">Out Ändern des Schlüssels des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8616c-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8616c-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="8616c-130">_binPcl_</span></span>
  
> <span data-ttu-id="8616c-131">Out Ändern der Liste des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8616c-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8616c-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="8616c-132">_skeyDst_</span></span>
  
> <span data-ttu-id="8616c-133">Out Quellschlüssel des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8616c-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8616c-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="8616c-134">_pupmov_</span></span>
  
> <span data-ttu-id="8616c-135">Out Zielordner Informationen, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8616c-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8616c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8616c-136">See also</span></span>

- [<span data-ttu-id="8616c-137">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="8616c-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="8616c-138">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="8616c-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="8616c-139">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8616c-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="8616c-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="8616c-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="8616c-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="8616c-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="8616c-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="8616c-142">UPMOV</span></span>](upmov.md)

