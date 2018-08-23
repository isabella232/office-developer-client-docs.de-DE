---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580439"
---
# <a name="uptbl"></a><span data-ttu-id="fdb28-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="fdb28-103">UPTBL</span></span>

<span data-ttu-id="fdb28-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdb28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdb28-105">Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="fdb28-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fdb28-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="fdb28-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="fdb28-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="fdb28-107">Members</span></span>

<span data-ttu-id="fdb28-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fdb28-108">_ulFlags_</span></span>
  
> <span data-ttu-id="fdb28-109">[in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fdb28-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="fdb28-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="fdb28-110">UPT_OK</span></span>
    
    - <span data-ttu-id="fdb28-111">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fdb28-111">[in] Upload was successful.</span></span> <span data-ttu-id="fdb28-112">Der Client legt dies nach dem Hochladen der Inhalt des Ordners auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="fdb28-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="fdb28-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="fdb28-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="fdb28-114">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fdb28-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fdb28-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="fdb28-115">_pszName_</span></span>
  
> <span data-ttu-id="fdb28-116">[out] Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="fdb28-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="fdb28-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="fdb28-117">_feid_</span></span>
  
> <span data-ttu-id="fdb28-118">[out] Die EntryID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="fdb28-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="fdb28-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="fdb28-119">_uintReserved_</span></span>
  
> <span data-ttu-id="fdb28-120">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fdb28-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fdb28-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="fdb28-121">_rgte_</span></span>
  
> <span data-ttu-id="fdb28-122">[out] Struktur für die folgenden Informationen für normalen (oder nicht ausgeblendeten) und zugeordneten (oder ausgeblendet) Elemente im Ordner: _Rgte [0]_ für normale Elemente und _Rgte [1]_ für verknüpfte Objekte.</span><span class="sxs-lookup"><span data-stu-id="fdb28-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="fdb28-123">die Anzahl der neuen oder geänderten Elemente</span><span class="sxs-lookup"><span data-stu-id="fdb28-123">the number of new or modified items</span></span>
   - <span data-ttu-id="fdb28-124">die Anzahl der Elemente lesen</span><span class="sxs-lookup"><span data-stu-id="fdb28-124">the number of read items</span></span> 
   - <span data-ttu-id="fdb28-125">die Anzahl der gelöschten Elemente</span><span class="sxs-lookup"><span data-stu-id="fdb28-125">the number of deleted items</span></span>
    
 <span data-ttu-id="fdb28-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="fdb28-126">_iEnt_</span></span>
  
> <span data-ttu-id="fdb28-127">[out] Index zum Nachverfolgen die Anzahl von Änderungen durch _cEnt_angegebenen hochladen.</span><span class="sxs-lookup"><span data-stu-id="fdb28-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="fdb28-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="fdb28-128">_cEnt_</span></span>
  
> <span data-ttu-id="fdb28-129">[out] Anzahl der Änderungen in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="fdb28-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="fdb28-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="fdb28-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="fdb28-131">[out] Kette von [UPMOV](upmov.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="fdb28-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="fdb28-132">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="fdb28-132">_pReserved_</span></span>
  
> <span data-ttu-id="fdb28-133">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fdb28-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fdb28-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdb28-134">See also</span></span>

- [<span data-ttu-id="fdb28-135">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="fdb28-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="fdb28-136">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="fdb28-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fdb28-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="fdb28-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="fdb28-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="fdb28-138">UPTBLE</span></span>](uptble.md)

