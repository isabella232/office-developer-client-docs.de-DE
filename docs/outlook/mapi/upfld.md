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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360480"
---
# <a name="upfld"></a><span data-ttu-id="b46bd-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="b46bd-103">UPFLD</span></span>

<span data-ttu-id="b46bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b46bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b46bd-105">Informationen zum Hochladen eines Ordners während des [Upload-Ordner Status](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="b46bd-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b46bd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b46bd-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="b46bd-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="b46bd-107">Members</span></span>

<span data-ttu-id="b46bd-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b46bd-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="b46bd-109">[out]/[in] Flags, um geeignete Aktionen für das Uplaod zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b46bd-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="b46bd-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="b46bd-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="b46bd-111">Out Folder ist neu.</span><span class="sxs-lookup"><span data-stu-id="b46bd-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="b46bd-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="b46bd-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="b46bd-113">Out Der Ordner wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="b46bd-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="b46bd-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="b46bd-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="b46bd-115">Out Die Ordner Eigenschaften wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="b46bd-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="b46bd-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="b46bd-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="b46bd-117">Out Der Ordner wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b46bd-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="b46bd-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="b46bd-118">UPF_OK</span></span>
    
    - <span data-ttu-id="b46bd-119">in Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b46bd-119">[in] Upload was successful.</span></span> <span data-ttu-id="b46bd-120">Der Client legt dies nach dem Hochladen von Ordnerinformationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="b46bd-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="b46bd-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="b46bd-121">_pfld_</span></span>
  
> <span data-ttu-id="b46bd-122">Out Das geöffnete Folder-Objekt, das hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b46bd-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="b46bd-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="b46bd-123">_feid_</span></span>
  
> <span data-ttu-id="b46bd-124">[out] Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="b46bd-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b46bd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b46bd-125">See also</span></span>

- [<span data-ttu-id="b46bd-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="b46bd-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="b46bd-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b46bd-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b46bd-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b46bd-128">MAPI Constants</span></span>](mapi-constants.md)

