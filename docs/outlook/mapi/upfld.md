---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795799"
---
# <a name="upfld"></a><span data-ttu-id="3a80f-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="3a80f-103">UPFLD</span></span>

<span data-ttu-id="3a80f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a80f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a80f-105">Informationen zum Hochladen eines Ordners während der [Zustand Ordner hochladen](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="3a80f-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3a80f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3a80f-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="3a80f-107">Members</span><span class="sxs-lookup"><span data-stu-id="3a80f-107">Members</span></span>

<span data-ttu-id="3a80f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a80f-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="3a80f-109">[Out] / [in] Flags an, die entsprechende Aktionen für die Uplaod bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3a80f-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="3a80f-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="3a80f-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="3a80f-111">[out] Ordner ist neu.</span><span class="sxs-lookup"><span data-stu-id="3a80f-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="3a80f-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="3a80f-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="3a80f-113">[out] Ordner wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="3a80f-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="3a80f-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="3a80f-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="3a80f-115">[out] Ordnereigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="3a80f-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="3a80f-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="3a80f-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="3a80f-117">[out] Ordner wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3a80f-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="3a80f-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="3a80f-118">UPF_OK</span></span>
    
    - <span data-ttu-id="3a80f-119">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3a80f-119">[in] Upload was successful.</span></span> <span data-ttu-id="3a80f-120">Der Client legt dies nach dem Hochladen der Ordnerinformationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="3a80f-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="3a80f-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="3a80f-121">_pfld_</span></span>
  
> <span data-ttu-id="3a80f-122">[out] Hochladen open Folder-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a80f-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="3a80f-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="3a80f-123">_feid_</span></span>
  
> <span data-ttu-id="3a80f-124">[out] Die EntryID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="3a80f-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a80f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a80f-125">See also</span></span>

- [<span data-ttu-id="3a80f-126">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="3a80f-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="3a80f-127">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="3a80f-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="3a80f-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3a80f-128">MAPI Constants</span></span>](mapi-constants.md)

