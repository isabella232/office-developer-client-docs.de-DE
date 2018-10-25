---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398122"
---
# <a name="dntbl"></a><span data-ttu-id="4c824-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="4c824-103">DNTBL</span></span>
 
<span data-ttu-id="4c824-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c824-105">Informationen zum Herunterladen der Inhalte eines Ordners vom Server während des [Download-Tabellenzustands](download-table-state.md) als Teil einer vollständigen Synchronisierung für Inhalte in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="4c824-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4c824-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4c824-106">Quick Info</span></span>

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

## <a name="members"></a><span data-ttu-id="4c824-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="4c824-107">Members</span></span>

<span data-ttu-id="4c824-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c824-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4c824-109">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="4c824-109">[in] Flags to modify behavior.</span></span> 
    
  - <span data-ttu-id="4c824-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="4c824-110">DNT_OK</span></span>
    
    - <span data-ttu-id="4c824-111">[in] Download war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4c824-111">[in] Download was successful.</span></span> <span data-ttu-id="4c824-112">Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.</span><span class="sxs-lookup"><span data-stu-id="4c824-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="4c824-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="4c824-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="4c824-114">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="4c824-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="4c824-116">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="4c824-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="4c824-118">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="4c824-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="4c824-120">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="4c824-121">_pxicc_</span></span>
  
>  <span data-ttu-id="4c824-122">[out] Verweis auf die **IExchangeImportContentsChanges**-Inhaltsschnittstelle, die das Herunterladen von Änderungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="4c824-123">Weitere Informationen zu **IExchangeImportContentsChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c824-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="4c824-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="4c824-124">_pxihc_</span></span>
  
>  <span data-ttu-id="4c824-125">[out] Verweis auf die **IExchangeImportHierarchyChanges**-Hierarchieschnittstelle, die das Herunterladen von inkrementellen Hierarchieänderungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="4c824-126">Weitere Informationen zu **IExchangeImportHierarchyChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c824-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="4c824-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="4c824-127">_pszName_</span></span>
  
>  <span data-ttu-id="4c824-128">[out] Der Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c824-128">Name of the folder.</span></span> 
    
<span data-ttu-id="4c824-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="4c824-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="4c824-130">[out] Uhrzeit der letzten Änderung des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c824-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="4c824-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="4c824-131">_ulRights_</span></span>
  
>  <span data-ttu-id="4c824-132">[out] Der Wert der **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)**-Eigenschaft des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c824-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="4c824-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="4c824-133">_FEID_</span></span>
  
>  <span data-ttu-id="4c824-134">[out] Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c824-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="4c824-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="4c824-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="4c824-136">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="4c824-137">_rgte_</span></span>
  
> <span data-ttu-id="4c824-138">[out] Änderungen für normale (oder nicht ausgeblendet) und verknüpfte (oder ausgeblendeten) Elemente.</span><span class="sxs-lookup"><span data-stu-id="4c824-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="4c824-139">*rgte[0]*  ist für normale Elemente, *rgte[1]* ist für verknüpfte Elemente.</span><span class="sxs-lookup"><span data-stu-id="4c824-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="4c824-140">Outlook füllt dieses Element während des Herunterladens bei Verwendung von Incremental Change Synchronization (ICS) auf.</span><span class="sxs-lookup"><span data-stu-id="4c824-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="4c824-141">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c824-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="4c824-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="4c824-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="4c824-143">[in]/[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="4c824-144">_boReserved_</span></span>
  
>  <span data-ttu-id="4c824-145">[in] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="4c824-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="4c824-147">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="4c824-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="4c824-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="4c824-149">[in] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c824-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4c824-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c824-150">See also</span></span>

- [<span data-ttu-id="4c824-151">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4c824-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="4c824-152">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4c824-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="4c824-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="4c824-153">DNTBLE</span></span>](dntble.md)

