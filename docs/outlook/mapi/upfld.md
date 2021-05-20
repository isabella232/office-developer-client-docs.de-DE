---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431358"
---
# <a name="upfld"></a><span data-ttu-id="396e8-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="396e8-103">UPFLD</span></span>

<span data-ttu-id="396e8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="396e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="396e8-105">Informationen zum Hochladen eines Ordners während des [Uploadordnerstatus](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="396e8-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="396e8-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="396e8-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="396e8-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="396e8-107">Members</span></span>

<span data-ttu-id="396e8-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="396e8-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="396e8-109">[out]/[in] Flags, um geeignete Aktionen für den Uplaod zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="396e8-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="396e8-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="396e8-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="396e8-111">[out] Ordner ist neu.</span><span class="sxs-lookup"><span data-stu-id="396e8-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="396e8-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="396e8-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="396e8-113">[out] Ordner wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="396e8-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="396e8-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="396e8-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="396e8-115">[out] Die Ordnereigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="396e8-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="396e8-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="396e8-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="396e8-117">[out] Ordner wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="396e8-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="396e8-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="396e8-118">UPF_OK</span></span>
    
    - <span data-ttu-id="396e8-119">[in] Hochladen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="396e8-119">[in] Upload was successful.</span></span> <span data-ttu-id="396e8-120">Der Client legt dies nach dem Hochladen von Ordnerinformationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="396e8-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="396e8-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="396e8-121">_pfld_</span></span>
  
> <span data-ttu-id="396e8-122">[out] Das hochzuladende Objekt des geöffneten Ordners.</span><span class="sxs-lookup"><span data-stu-id="396e8-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="396e8-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="396e8-123">_feid_</span></span>
  
> <span data-ttu-id="396e8-124">[out] Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="396e8-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="396e8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="396e8-125">See also</span></span>

- [<span data-ttu-id="396e8-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="396e8-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="396e8-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="396e8-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="396e8-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="396e8-128">MAPI Constants</span></span>](mapi-constants.md)

