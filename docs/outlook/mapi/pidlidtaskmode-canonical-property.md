---
title: Kanonische Pidlidtaskmode (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357939"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="4de94-103">Kanonische Pidlidtaskmode (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4de94-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="4de94-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4de94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4de94-105">Gibt den Zuordnungsstatus der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="4de94-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4de94-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4de94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4de94-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="4de94-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="4de94-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4de94-108">Property set:</span></span>  <br/> |<span data-ttu-id="4de94-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4de94-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4de94-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="4de94-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4de94-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="4de94-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="4de94-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4de94-112">Data type:</span></span>  <br/> |<span data-ttu-id="4de94-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4de94-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4de94-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4de94-114">Area:</span></span>  <br/> |<span data-ttu-id="4de94-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="4de94-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4de94-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4de94-116">Remarks</span></span>

<span data-ttu-id="4de94-117">Der Wert muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="4de94-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="4de94-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4de94-118">**Value**</span></span>|<span data-ttu-id="4de94-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4de94-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4de94-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4de94-120">0x00000000</span></span>  <br/> |<span data-ttu-id="4de94-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4de94-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="4de94-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4de94-122">0x00000001</span></span>  <br/> |<span data-ttu-id="4de94-123">Die Aufgabe ist in eine Aufgabenanfrage eingebettet.</span><span class="sxs-lookup"><span data-stu-id="4de94-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="4de94-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4de94-124">0x00000002</span></span>  <br/> |<span data-ttu-id="4de94-125">Die Aufgabe wurde vom Aufgabenempfänger akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4de94-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="4de94-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4de94-126">0x00000003</span></span>  <br/> |<span data-ttu-id="4de94-127">Die Aufgabe wurde vom Aufgabenempfänger abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="4de94-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="4de94-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4de94-128">0x00000004</span></span>  <br/> |<span data-ttu-id="4de94-129">Die Aufgabe ist in eine Vorgangsaktualisierung eingebettet.</span><span class="sxs-lookup"><span data-stu-id="4de94-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="4de94-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4de94-130">0x00000005</span></span>  <br/> |<span data-ttu-id="4de94-131">Die Aufgabe wurde dem Aufgaben beauftragten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4de94-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4de94-132">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4de94-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4de94-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4de94-133">Protocol specifications</span></span>

<span data-ttu-id="4de94-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4de94-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4de94-135">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="4de94-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4de94-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4de94-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4de94-137">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="4de94-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4de94-138">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4de94-138">Header files</span></span>

<span data-ttu-id="4de94-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4de94-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="4de94-140">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4de94-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4de94-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4de94-141">See also</span></span>



[<span data-ttu-id="4de94-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4de94-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4de94-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4de94-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4de94-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4de94-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4de94-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4de94-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

