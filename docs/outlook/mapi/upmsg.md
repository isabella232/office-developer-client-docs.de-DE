---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795816"
---
# <a name="upmsg"></a><span data-ttu-id="7c307-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="7c307-103">UPMSG</span></span>

<span data-ttu-id="7c307-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c307-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c307-105">Informationen zum Hochladen eines Outlook-Elements während der [Nachrichtenstatus hochladen](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="7c307-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c307-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7c307-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7c307-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="7c307-107">Members</span></span>

 <span data-ttu-id="7c307-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c307-108">_ulFlags_</span></span>
  
> <span data-ttu-id="7c307-109">[Out] / [in] Flags, die entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7c307-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="7c307-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="7c307-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="7c307-111">[out] Element ist verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7c307-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="7c307-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="7c307-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="7c307-113">[out] Neues Element.</span><span class="sxs-lookup"><span data-stu-id="7c307-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="7c307-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="7c307-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="7c307-115">[out] Element wurde hier verschoben.</span><span class="sxs-lookup"><span data-stu-id="7c307-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="7c307-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="7c307-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="7c307-117">[out] Elementeigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="7c307-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="7c307-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="7c307-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="7c307-119">[out] Item ist ein Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="7c307-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="7c307-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="7c307-120">UPM_OK</span></span>
    
    - <span data-ttu-id="7c307-121">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7c307-121">[in] Upload was successful.</span></span> <span data-ttu-id="7c307-122">Der Client legt dies nach dem Hochladen von Informationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="7c307-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="7c307-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="7c307-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="7c307-124">[in] Element wurde erfolgreich verschoben.</span><span class="sxs-lookup"><span data-stu-id="7c307-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="7c307-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="7c307-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="7c307-126">[in] Upload-Status jetzt Commit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7c307-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="7c307-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="7c307-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="7c307-128">[in] Jetzt löschen Sie Element.</span><span class="sxs-lookup"><span data-stu-id="7c307-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="7c307-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="7c307-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="7c307-130">[in] Speichern Sie Änderungen an das Element an.</span><span class="sxs-lookup"><span data-stu-id="7c307-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="7c307-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="7c307-131">_pmsg_</span></span>
  
> <span data-ttu-id="7c307-132">[out] Open Item-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7c307-132">[out] Open item object.</span></span> <span data-ttu-id="7c307-133">Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.</span><span class="sxs-lookup"><span data-stu-id="7c307-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="7c307-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="7c307-134">_meid_</span></span>
  
> <span data-ttu-id="7c307-135">[out] Die EntryID des Elements.</span><span class="sxs-lookup"><span data-stu-id="7c307-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="7c307-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="7c307-136">_binReserved1_</span></span>
  
> <span data-ttu-id="7c307-137">[in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c307-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7c307-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="7c307-138">_binReserved2_</span></span>
  
> <span data-ttu-id="7c307-139">[in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c307-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7c307-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="7c307-140">_feid_</span></span>
  
> <span data-ttu-id="7c307-141">[out] Eintrags-ID des Quellordners, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="7c307-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="7c307-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="7c307-142">_binChg_</span></span>
  
> <span data-ttu-id="7c307-143">[out] Ändern Sie Schlüssel des Elements Ziel, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="7c307-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="7c307-144">Finden Sie unter mapidefs.h für die Definition des **SBinary**Typs.</span><span class="sxs-lookup"><span data-stu-id="7c307-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="7c307-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="7c307-145">_binPcl_</span></span>
  
> <span data-ttu-id="7c307-146">[out] Ändern Sie Liste des Elements Ziel, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="7c307-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="7c307-147">Finden Sie unter mapidefs.h für die Definition des **SBinary**Typs.</span><span class="sxs-lookup"><span data-stu-id="7c307-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="7c307-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="7c307-148">_skeySrc_</span></span>
  
> <span data-ttu-id="7c307-149">[out] Schlüssel Source des Quellelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="7c307-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c307-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c307-150">See also</span></span>

- [<span data-ttu-id="7c307-151">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="7c307-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="7c307-152">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="7c307-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7c307-153">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7c307-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="7c307-154">FEID</span><span class="sxs-lookup"><span data-stu-id="7c307-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="7c307-155">MEID</span><span class="sxs-lookup"><span data-stu-id="7c307-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="7c307-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="7c307-156">SKEY</span></span>](skey.md)

