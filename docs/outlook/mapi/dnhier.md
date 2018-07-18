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
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791591"
---
# <a name="dnhier"></a><span data-ttu-id="c9d22-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="c9d22-103">DNHIER</span></span>

<span data-ttu-id="c9d22-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9d22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9d22-105">Informationen für das Herunterladen einer Hierarchie vom Server während der [Hierarchie Zustand herunterladen](download-hierarchy-state.md), die Teil einer vollständigen hierarchiesynchronisierung ist.</span><span class="sxs-lookup"><span data-stu-id="c9d22-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="c9d22-106">Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="c9d22-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="c9d22-107">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9d22-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c9d22-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c9d22-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c9d22-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d22-109">Members</span></span>

<span data-ttu-id="c9d22-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9d22-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="c9d22-111">[in] Kennzeichen, die um das entsprechende Verhalten während des Downloads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c9d22-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="c9d22-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="c9d22-112">DNH_OK</span></span>
    
   - <span data-ttu-id="c9d22-113">[in] Download war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c9d22-113">[in] Download was successful.</span></span> <span data-ttu-id="c9d22-114">Der Client legt dies nach dem Herunterladen von Informationen vom Server.</span><span class="sxs-lookup"><span data-stu-id="c9d22-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="c9d22-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="c9d22-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="c9d22-116">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9d22-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c9d22-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="c9d22-117">_pxihc_</span></span>
  
>  <span data-ttu-id="c9d22-118">[out] Zeiger auf die **IExchangeImportHierarchyChanges** Hierarchie-Schnittstelle unterstützt, die Hierarchie inkrementelle Änderungen herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c9d22-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="c9d22-119">Weitere Informationen zu **IExchangeImportHierarchyChanges**finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9d22-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c9d22-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="c9d22-120">_cEntNew_</span></span>
  
> <span data-ttu-id="c9d22-121">[out] Anzahl der Ordner auf dem lokalen Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c9d22-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="c9d22-122">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c9d22-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="c9d22-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="c9d22-123">_cEntMod_</span></span>
  
> <span data-ttu-id="c9d22-124">[out] Anzahl der Ordner auf dem lokalen Speicher geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c9d22-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="c9d22-125">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c9d22-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="c9d22-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="c9d22-126">_cEntDel_</span></span>
  
> <span data-ttu-id="c9d22-127">[out] Anzahl der Ordner auf dem lokalen Speicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9d22-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="c9d22-128">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c9d22-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9d22-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9d22-129">See also</span></span>

- [<span data-ttu-id="c9d22-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="c9d22-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="c9d22-131">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c9d22-131">MAPI Constants</span></span>](mapi-constants.md)

