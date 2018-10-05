---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389085"
---
# <a name="dnhier"></a><span data-ttu-id="b61da-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="b61da-103">DNHIER</span></span>

<span data-ttu-id="b61da-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b61da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b61da-105">Informationen für das Herunterladen einer Hierarchie vom Server während der [Hierarchie Zustand herunterladen](download-hierarchy-state.md), die Teil einer vollständigen hierarchiesynchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="b61da-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="b61da-106">Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="b61da-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b61da-107">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b61da-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b61da-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b61da-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="b61da-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="b61da-109">Members</span></span>

<span data-ttu-id="b61da-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b61da-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="b61da-111">[in] Kennzeichen, die um das entsprechende Verhalten während des Downloads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b61da-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="b61da-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="b61da-112">DNH_OK</span></span>
    
   - <span data-ttu-id="b61da-113">[in] Download war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b61da-113">[in] Download was successful.</span></span> <span data-ttu-id="b61da-114">Der Client legt dies nach dem Herunterladen von Informationen vom Server.</span><span class="sxs-lookup"><span data-stu-id="b61da-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="b61da-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="b61da-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="b61da-116">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b61da-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="b61da-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="b61da-117">_pxihc_</span></span>
  
>  <span data-ttu-id="b61da-118">[out] Zeiger auf die **IExchangeImportHierarchyChanges** Hierarchie-Schnittstelle unterstützt, die Hierarchie inkrementelle Änderungen herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b61da-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="b61da-119">Weitere Informationen zu **IExchangeImportHierarchyChanges**finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b61da-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="b61da-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="b61da-120">_cEntNew_</span></span>
  
> <span data-ttu-id="b61da-121">[out] Anzahl der Ordner auf dem lokalen Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b61da-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="b61da-122">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b61da-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="b61da-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="b61da-123">_cEntMod_</span></span>
  
> <span data-ttu-id="b61da-124">[out] Anzahl der Ordner auf dem lokalen Speicher geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b61da-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="b61da-125">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b61da-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="b61da-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="b61da-126">_cEntDel_</span></span>
  
> <span data-ttu-id="b61da-127">[out] Anzahl der Ordner auf dem lokalen Speicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b61da-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="b61da-128">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b61da-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b61da-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b61da-129">See also</span></span>

- [<span data-ttu-id="b61da-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b61da-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="b61da-131">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b61da-131">MAPI Constants</span></span>](mapi-constants.md)

