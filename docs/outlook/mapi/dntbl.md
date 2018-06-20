---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791590"
---
# <a name="dntbl"></a><span data-ttu-id="03174-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="03174-103">DNTBL</span></span>
 
<span data-ttu-id="03174-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03174-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03174-105">Informationen für das Herunterladen von den Inhalt eines Ordners auf dem Server während der [Tabelle Downloadstatus](download-table-state.md), als Teil einer vollständigen Synchronisierung für Inhalt in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="03174-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="03174-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="03174-106">Quick info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="03174-107">Members</span><span class="sxs-lookup"><span data-stu-id="03174-107">Members</span></span>

<span data-ttu-id="03174-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03174-108">_ulFlags_</span></span>
  
> <span data-ttu-id="03174-109">[in] Flags Ändern des Verhaltens</span><span class="sxs-lookup"><span data-stu-id="03174-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="03174-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="03174-110">DNT_OK</span></span>
    
    - <span data-ttu-id="03174-111">[in] Download war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="03174-111">[in] Download was successful.</span></span> <span data-ttu-id="03174-112">Der Client legt dies nach dem Herunterladen von Informationen vom Server.</span><span class="sxs-lookup"><span data-stu-id="03174-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="03174-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="03174-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="03174-114">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="03174-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="03174-116">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="03174-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="03174-118">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="03174-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="03174-120">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="03174-121">_pxicc_</span></span>
  
>  <span data-ttu-id="03174-122">[out] Zeiger auf die **IExchangeImportContentsChanges** Inhalt-Schnittstelle unterstützt, Herunterladen von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="03174-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="03174-123">Weitere Informationen zu **IExchangeImportContentsChanges**finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03174-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="03174-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="03174-124">_pxihc_</span></span>
  
>  <span data-ttu-id="03174-125">[out] Zeiger auf die **IExchangeImportHierarchyChanges** Hierarchie-Schnittstelle unterstützt, die Hierarchie inkrementelle Änderungen herunterladen.</span><span class="sxs-lookup"><span data-stu-id="03174-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="03174-126">Weitere Informationen zu **IExchangeImportHierarchyChanges**finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03174-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="03174-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="03174-127">_pszName_</span></span>
  
>  <span data-ttu-id="03174-128">[out] Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="03174-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="03174-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="03174-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="03174-130">[out] Zeitpunkt der letzten Änderung des Ordners.</span><span class="sxs-lookup"><span data-stu-id="03174-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="03174-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="03174-131">_ulRights_</span></span>
  
>  <span data-ttu-id="03174-132">[out] Der Wert der Eigenschaft **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** des Ordners.</span><span class="sxs-lookup"><span data-stu-id="03174-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="03174-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="03174-133">_feid_</span></span>
  
>  <span data-ttu-id="03174-134">[out] Die EntryID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="03174-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="03174-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="03174-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="03174-136">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="03174-137">_rgte_</span></span>
  
> <span data-ttu-id="03174-138">[out] Änderungen für normalen (oder nicht ausgeblendeten) und zugeordneten (oder ausgeblendet) Elemente.</span><span class="sxs-lookup"><span data-stu-id="03174-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="03174-139">*Rgte [0]* ist für normale Elemente und *Rgte [1]* ist für verknüpfte Objekte.</span><span class="sxs-lookup"><span data-stu-id="03174-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="03174-140">Outlook wird dieser Member während des Herunterladens, wenn Sie inkrementelle Änderung Synchronisierung (ICS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="03174-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="03174-141">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03174-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="03174-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="03174-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="03174-143">[in] / [out] dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="03174-144">_boReserved_</span></span>
  
>  <span data-ttu-id="03174-145">[in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="03174-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="03174-147">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="03174-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="03174-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="03174-149">[in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03174-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="03174-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03174-150">See also</span></span>

- [<span data-ttu-id="03174-151">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="03174-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="03174-152">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="03174-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="03174-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="03174-153">DNTBLE</span></span>](dntble.md)

