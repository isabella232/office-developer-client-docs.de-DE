---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338871"
---
# <a name="upmsg"></a><span data-ttu-id="624f5-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="624f5-103">UPMSG</span></span>

<span data-ttu-id="624f5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="624f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="624f5-105">Informationen zum Hochladen eines Outlook-Elements während des [Upload-Nachrichtenstatus](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="624f5-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="624f5-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="624f5-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="624f5-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="624f5-107">Members</span></span>

 <span data-ttu-id="624f5-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="624f5-108">_ulFlags_</span></span>
  
> <span data-ttu-id="624f5-109">[out]/[in] Flags zum Bestimmen des geeigneten Verhaltens während des Uploads.</span><span class="sxs-lookup"><span data-stu-id="624f5-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="624f5-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="624f5-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="624f5-111">Out Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="624f5-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="624f5-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="624f5-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="624f5-113">Out Neues Element.</span><span class="sxs-lookup"><span data-stu-id="624f5-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="624f5-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="624f5-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="624f5-115">Out Das Element wurde hierhin verschoben.</span><span class="sxs-lookup"><span data-stu-id="624f5-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="624f5-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="624f5-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="624f5-117">Out Elementeigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="624f5-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="624f5-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="624f5-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="624f5-119">Out Item ist eine Nachrichtenkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="624f5-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="624f5-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="624f5-120">UPM_OK</span></span>
    
    - <span data-ttu-id="624f5-121">in Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="624f5-121">[in] Upload was successful.</span></span> <span data-ttu-id="624f5-122">Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="624f5-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="624f5-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="624f5-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="624f5-124">in Das Element wurde erfolgreich verschoben.</span><span class="sxs-lookup"><span data-stu-id="624f5-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="624f5-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="624f5-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="624f5-126">in Commit-Uploadstatus jetzt.</span><span class="sxs-lookup"><span data-stu-id="624f5-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="624f5-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="624f5-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="624f5-128">in Element jetzt löschen.</span><span class="sxs-lookup"><span data-stu-id="624f5-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="624f5-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="624f5-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="624f5-130">in Speichert die Änderungen am Element.</span><span class="sxs-lookup"><span data-stu-id="624f5-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="624f5-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="624f5-131">_pmsg_</span></span>
  
> <span data-ttu-id="624f5-132">Out Open Item-Objekt.</span><span class="sxs-lookup"><span data-stu-id="624f5-132">[out] Open item object.</span></span> <span data-ttu-id="624f5-133">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="624f5-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="624f5-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="624f5-134">_meid_</span></span>
  
> <span data-ttu-id="624f5-135">Out Eintrags-ID des Elements.</span><span class="sxs-lookup"><span data-stu-id="624f5-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="624f5-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="624f5-136">_binReserved1_</span></span>
  
> <span data-ttu-id="624f5-137">in Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="624f5-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="624f5-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="624f5-138">_binReserved2_</span></span>
  
> <span data-ttu-id="624f5-139">in Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="624f5-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="624f5-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="624f5-140">_feid_</span></span>
  
> <span data-ttu-id="624f5-141">Out Eintrags-ID des Quellordners, wenn item verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="624f5-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="624f5-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="624f5-142">_binChg_</span></span>
  
> <span data-ttu-id="624f5-143">Out Ändern des Schlüssels des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="624f5-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="624f5-144">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="624f5-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="624f5-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="624f5-145">_binPcl_</span></span>
  
> <span data-ttu-id="624f5-146">Out Ändern Sie die Liste des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="624f5-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="624f5-147">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="624f5-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="624f5-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="624f5-148">_skeySrc_</span></span>
  
> <span data-ttu-id="624f5-149">Out Quellschlüssel des Quellelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="624f5-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="624f5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="624f5-150">See also</span></span>

- [<span data-ttu-id="624f5-151">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="624f5-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="624f5-152">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="624f5-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="624f5-153">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="624f5-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="624f5-154">FEID</span><span class="sxs-lookup"><span data-stu-id="624f5-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="624f5-155">MEID</span><span class="sxs-lookup"><span data-stu-id="624f5-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="624f5-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="624f5-156">SKEY</span></span>](skey.md)

