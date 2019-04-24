---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337100"
---
# <a name="dnhier"></a><span data-ttu-id="81a2c-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="81a2c-103">DNHIER</span></span>

<span data-ttu-id="81a2c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81a2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81a2c-105">Informationen zum Herunterladen einer Hierarchie vom Server während des [Zustands „Downloadhierarchie](download-hierarchy-state.md), der Teil einer vollständigen Hierarchiesynchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="81a2c-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="81a2c-106">Bei diesem Downloadvorgang wird Microsoft Exchange Incremental Change Synchronization (ICS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="81a2c-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="81a2c-107">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="81a2c-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="81a2c-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="81a2c-108">Quick info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="81a2c-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="81a2c-109">Members</span></span>

<span data-ttu-id="81a2c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81a2c-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="81a2c-111">[in] Flags, um das entsprechende Verhalten während des Downloads zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="81a2c-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="81a2c-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="81a2c-112">DNH_OK</span></span>
    
   - <span data-ttu-id="81a2c-113">[in] Download war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="81a2c-113">[in] Download was successful.</span></span> <span data-ttu-id="81a2c-114">Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.</span><span class="sxs-lookup"><span data-stu-id="81a2c-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="81a2c-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="81a2c-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="81a2c-116">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81a2c-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="81a2c-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="81a2c-117">_pxihc_</span></span>
  
>  <span data-ttu-id="81a2c-118">[out] Verweis auf die **IExchangeImportHierarchyChanges**-Hierarchieschnittstelle, die das Herunterladen von inkrementellen Hierarchieänderungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81a2c-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="81a2c-119">Weitere Informationen zu **IExchangeImportHierarchyChanges** finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="81a2c-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="81a2c-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="81a2c-120">_cEntNew_</span></span>
  
> <span data-ttu-id="81a2c-121">[out] Die Anzahl von Ordnern, die dem lokalen Speicher hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="81a2c-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="81a2c-122">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="81a2c-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="81a2c-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="81a2c-123">_cEntMod_</span></span>
  
> <span data-ttu-id="81a2c-124">[out] Die Anzahl von Ordnern, die dem lokalen Speicher geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81a2c-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="81a2c-125">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="81a2c-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="81a2c-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="81a2c-126">_cEntDel_</span></span>
  
> <span data-ttu-id="81a2c-127">[out] Die Anzahl von Ordnern, die im lokalen Speicher gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81a2c-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="81a2c-128">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="81a2c-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81a2c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81a2c-129">See also</span></span>

- [<span data-ttu-id="81a2c-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="81a2c-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="81a2c-131">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="81a2c-131">MAPI Constants</span></span>](mapi-constants.md)

