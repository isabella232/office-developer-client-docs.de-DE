---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592094"
---
# <a name="uphier"></a><span data-ttu-id="43b2a-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="43b2a-103">UPHIER</span></span>
 
<span data-ttu-id="43b2a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b2a-105">Informationen zum Synchronisieren von einer Ordnerhierarchie während der [Hierarchie Zustand hochladen](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="43b2a-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="43b2a-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="43b2a-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="43b2a-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="43b2a-107">Members</span></span>

<span data-ttu-id="43b2a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43b2a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="43b2a-109">[in] Kennzeichen, die das Verhalten bei der Synchronisierung der Ordnerhierarchie ändern.</span><span class="sxs-lookup"><span data-stu-id="43b2a-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="43b2a-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="43b2a-110">UPH_OK</span></span>
    
    - <span data-ttu-id="43b2a-111">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="43b2a-111">[in] Upload was successful.</span></span> <span data-ttu-id="43b2a-112">Der Client legt dies nach dem Hochladen erfolgreich Informationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="43b2a-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="43b2a-113">Beim Anzeigen dieses Flag, löscht Outlook alle internen Protokollinformationen, die laut die Ordnerhierarchie aktualisieren erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43b2a-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="43b2a-114">Der Client übergibt das HRESULT, wenn der Hochladevorgang nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="43b2a-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="43b2a-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="43b2a-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="43b2a-116">[out] Dieser Member wird für die Outlook interne Verwendung reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43b2a-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="43b2a-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="43b2a-117">_iEnt_</span></span>
  
> <span data-ttu-id="43b2a-118">[out] Index zum Nachverfolgen die Anzahl von *cEnt* angegebenen Ordner zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="43b2a-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="43b2a-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="43b2a-119">_cEnt_</span></span>
  
> <span data-ttu-id="43b2a-120">[out] Anzahl der Ordner, die nicht mehr synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="43b2a-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43b2a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43b2a-121">See also</span></span>

- [<span data-ttu-id="43b2a-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="43b2a-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="43b2a-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="43b2a-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="43b2a-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="43b2a-124">MAPI Constants</span></span>](mapi-constants.md)

