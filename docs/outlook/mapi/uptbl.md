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
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438113"
---
# <a name="uptbl"></a><span data-ttu-id="9050d-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="9050d-103">UPTBL</span></span>

<span data-ttu-id="9050d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9050d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9050d-105">Informationen zum Hochladen der Inhalte eines Ordners während des [Upload-Tabellenstatus](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="9050d-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9050d-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9050d-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9050d-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="9050d-107">Members</span></span>

<span data-ttu-id="9050d-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9050d-108">_ulFlags_</span></span>
  
> <span data-ttu-id="9050d-109">in Flags zum Bestimmen des geeigneten Verhaltens während des Uploads.</span><span class="sxs-lookup"><span data-stu-id="9050d-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="9050d-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="9050d-110">UPT_OK</span></span>
    
    - <span data-ttu-id="9050d-111">in Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9050d-111">[in] Upload was successful.</span></span> <span data-ttu-id="9050d-112">Der Client legt dies fest, nachdem der Ordnerinhalt auf den Server hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="9050d-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="9050d-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="9050d-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="9050d-114">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9050d-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9050d-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="9050d-115">_pszName_</span></span>
  
> <span data-ttu-id="9050d-116">[out] Der Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="9050d-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="9050d-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="9050d-117">_feid_</span></span>
  
> <span data-ttu-id="9050d-118">[out] Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="9050d-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="9050d-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="9050d-119">_uintReserved_</span></span>
  
> <span data-ttu-id="9050d-120">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9050d-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9050d-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="9050d-121">_rgte_</span></span>
  
> <span data-ttu-id="9050d-122">Out Struktur für die folgenden Informationen für normale (oder nicht ausgeblendete) Elemente und zugeordnete (oder ausgeblendete) Elemente im Ordner: _rgte [0]_ gilt für normale Elemente, und _rgte [1]_ gilt für zugeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="9050d-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="9050d-123">die Anzahl der neuen oder geänderten Elemente</span><span class="sxs-lookup"><span data-stu-id="9050d-123">the number of new or modified items</span></span>
   - <span data-ttu-id="9050d-124">die Anzahl der gelesenen Elemente</span><span class="sxs-lookup"><span data-stu-id="9050d-124">the number of read items</span></span> 
   - <span data-ttu-id="9050d-125">die Anzahl der gelöschten Elemente</span><span class="sxs-lookup"><span data-stu-id="9050d-125">the number of deleted items</span></span>
    
 <span data-ttu-id="9050d-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="9050d-126">_iEnt_</span></span>
  
> <span data-ttu-id="9050d-127">Out Index zum Nachverfolgen des Uploads die Anzahl der durch _cEnt_angegebenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9050d-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="9050d-128">_Prozent_</span><span class="sxs-lookup"><span data-stu-id="9050d-128">_cEnt_</span></span>
  
> <span data-ttu-id="9050d-129">Out Die Anzahl der Änderungen am Ordner.</span><span class="sxs-lookup"><span data-stu-id="9050d-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="9050d-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="9050d-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="9050d-131">Out Kette von [UPMOV](upmov.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9050d-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="9050d-132">_Beibehalten_</span><span class="sxs-lookup"><span data-stu-id="9050d-132">_pReserved_</span></span>
  
> <span data-ttu-id="9050d-133">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9050d-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9050d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9050d-134">See also</span></span>

- [<span data-ttu-id="9050d-135">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="9050d-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="9050d-136">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="9050d-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9050d-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9050d-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="9050d-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="9050d-138">UPTBLE</span></span>](uptble.md)

