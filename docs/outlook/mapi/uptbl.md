---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795837"
---
# <a name="uptbl"></a><span data-ttu-id="4f539-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="4f539-103">UPTBL</span></span>

<span data-ttu-id="4f539-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f539-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f539-105">Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="4f539-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4f539-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4f539-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="4f539-107">Members</span><span class="sxs-lookup"><span data-stu-id="4f539-107">Members</span></span>

<span data-ttu-id="4f539-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f539-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4f539-109">[in] Kennzeichen, die um das entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4f539-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="4f539-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="4f539-110">UPT_OK</span></span>
    
    - <span data-ttu-id="4f539-111">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4f539-111">[in] Upload was successful.</span></span> <span data-ttu-id="4f539-112">Der Client legt dies nach dem Hochladen der Inhalt des Ordners auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="4f539-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="4f539-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="4f539-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="4f539-114">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f539-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4f539-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="4f539-115">_pszName_</span></span>
  
> <span data-ttu-id="4f539-116">[out] Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4f539-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="4f539-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="4f539-117">_feid_</span></span>
  
> <span data-ttu-id="4f539-118">[out] Die EntryID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4f539-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="4f539-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="4f539-119">_uintReserved_</span></span>
  
> <span data-ttu-id="4f539-120">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f539-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4f539-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="4f539-121">_rgte_</span></span>
  
> <span data-ttu-id="4f539-122">[out] Struktur für die folgenden Informationen für normalen (oder nicht ausgeblendeten) und zugeordneten (oder ausgeblendet) Elemente im Ordner: _Rgte [0]_ für normale Elemente und _Rgte [1]_ für verknüpfte Objekte.</span><span class="sxs-lookup"><span data-stu-id="4f539-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="4f539-123">die Anzahl der neuen oder geänderten Elemente</span><span class="sxs-lookup"><span data-stu-id="4f539-123">the number of new or modified items</span></span>
   - <span data-ttu-id="4f539-124">die Anzahl der Elemente lesen</span><span class="sxs-lookup"><span data-stu-id="4f539-124">the number of read items</span></span> 
   - <span data-ttu-id="4f539-125">die Anzahl der gelöschten Elemente</span><span class="sxs-lookup"><span data-stu-id="4f539-125">the number of deleted items</span></span>
    
 <span data-ttu-id="4f539-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="4f539-126">_iEnt_</span></span>
  
> <span data-ttu-id="4f539-127">[out] Index zum Nachverfolgen die Anzahl von Änderungen durch _cEnt_angegebenen hochladen.</span><span class="sxs-lookup"><span data-stu-id="4f539-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="4f539-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="4f539-128">_cEnt_</span></span>
  
> <span data-ttu-id="4f539-129">[out] Anzahl der Änderungen in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="4f539-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="4f539-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="4f539-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="4f539-131">[out] Kette von [UPMOV](upmov.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="4f539-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="4f539-132">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="4f539-132">_pReserved_</span></span>
  
> <span data-ttu-id="4f539-133">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f539-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f539-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f539-134">See also</span></span>

- [<span data-ttu-id="4f539-135">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="4f539-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="4f539-136">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="4f539-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4f539-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4f539-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="4f539-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="4f539-138">UPTBLE</span></span>](uptble.md)

