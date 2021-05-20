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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427269"
---
# <a name="upmsg"></a><span data-ttu-id="da4a8-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="da4a8-103">UPMSG</span></span>

<span data-ttu-id="da4a8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da4a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da4a8-105">Informationen zum Hochladen eines Outlook element während des [Status der Uploadnachricht](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="da4a8-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="da4a8-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="da4a8-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="da4a8-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="da4a8-107">Members</span></span>

 <span data-ttu-id="da4a8-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da4a8-108">_ulFlags_</span></span>
  
> <span data-ttu-id="da4a8-109">[out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="da4a8-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="da4a8-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="da4a8-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="da4a8-111">[out] Element ist zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="da4a8-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="da4a8-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="da4a8-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="da4a8-113">[out] Neues Element.</span><span class="sxs-lookup"><span data-stu-id="da4a8-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="da4a8-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="da4a8-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="da4a8-115">[out] Element wurde hier verschoben.</span><span class="sxs-lookup"><span data-stu-id="da4a8-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="da4a8-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="da4a8-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="da4a8-117">[out] Elementeigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="da4a8-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="da4a8-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="da4a8-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="da4a8-119">[out] Element ist eine Nachrichtenkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="da4a8-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="da4a8-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="da4a8-120">UPM_OK</span></span>
    
    - <span data-ttu-id="da4a8-121">[in] Hochladen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="da4a8-121">[in] Upload was successful.</span></span> <span data-ttu-id="da4a8-122">Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="da4a8-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="da4a8-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="da4a8-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="da4a8-124">[in] Element wurde erfolgreich verschoben.</span><span class="sxs-lookup"><span data-stu-id="da4a8-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="da4a8-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="da4a8-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="da4a8-126">[in] Commit-Uploadstatus jetzt.</span><span class="sxs-lookup"><span data-stu-id="da4a8-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="da4a8-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="da4a8-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="da4a8-128">[in] Element jetzt löschen.</span><span class="sxs-lookup"><span data-stu-id="da4a8-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="da4a8-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="da4a8-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="da4a8-130">[in] Speichern Sie Änderungen am Element.</span><span class="sxs-lookup"><span data-stu-id="da4a8-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="da4a8-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="da4a8-131">_pmsg_</span></span>
  
> <span data-ttu-id="da4a8-132">[out] Öffnen Sie das Elementobjekt.</span><span class="sxs-lookup"><span data-stu-id="da4a8-132">[out] Open item object.</span></span> <span data-ttu-id="da4a8-133">Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="da4a8-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="da4a8-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="da4a8-134">_meid_</span></span>
  
> <span data-ttu-id="da4a8-135">[out] Eintrags-ID des Elements.</span><span class="sxs-lookup"><span data-stu-id="da4a8-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="da4a8-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="da4a8-136">_binReserved1_</span></span>
  
> <span data-ttu-id="da4a8-137">[in] Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da4a8-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="da4a8-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="da4a8-138">_binReserved2_</span></span>
  
> <span data-ttu-id="da4a8-139">[in] Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da4a8-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="da4a8-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="da4a8-140">_feid_</span></span>
  
> <span data-ttu-id="da4a8-141">[out] Eintrags-ID des Quellordners, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="da4a8-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="da4a8-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="da4a8-142">_binChg_</span></span>
  
> <span data-ttu-id="da4a8-143">[out] Ändern Sie den Schlüssel des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="da4a8-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="da4a8-144">Die Typdefinition von **SBinary** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="da4a8-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="da4a8-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="da4a8-145">_binPcl_</span></span>
  
> <span data-ttu-id="da4a8-146">[out] Ändern der Liste des Zielelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="da4a8-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="da4a8-147">Die Typdefinition von **SBinary** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="da4a8-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="da4a8-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="da4a8-148">_skeySrc_</span></span>
  
> <span data-ttu-id="da4a8-149">[out] Quellschlüssel des Quellelements, wenn das Element verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="da4a8-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da4a8-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da4a8-150">See also</span></span>

- [<span data-ttu-id="da4a8-151">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="da4a8-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="da4a8-152">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="da4a8-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="da4a8-153">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="da4a8-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="da4a8-154">FEID</span><span class="sxs-lookup"><span data-stu-id="da4a8-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="da4a8-155">MEID</span><span class="sxs-lookup"><span data-stu-id="da4a8-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="da4a8-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="da4a8-156">SKEY</span></span>](skey.md)

