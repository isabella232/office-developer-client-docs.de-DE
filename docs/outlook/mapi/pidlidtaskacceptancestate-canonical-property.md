---
title: Kanonische PidLidTaskAcceptanceState-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 970fc57a3fd129f0ac50af3f71e0d5e15ff22371
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793813"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="e01f8-103">Kanonische PidLidTaskAcceptanceState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e01f8-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="e01f8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e01f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e01f8-105">Gibt den Annahmestatus des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e01f8-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e01f8-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e01f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e01f8-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="e01f8-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="e01f8-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e01f8-108">Property set:</span></span>  <br/> |<span data-ttu-id="e01f8-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e01f8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e01f8-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="e01f8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e01f8-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="e01f8-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="e01f8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e01f8-112">Data type:</span></span>  <br/> |<span data-ttu-id="e01f8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e01f8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e01f8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e01f8-114">Area:</span></span>  <br/> |<span data-ttu-id="e01f8-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e01f8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e01f8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e01f8-116">Remarks</span></span>

<span data-ttu-id="e01f8-117">In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e01f8-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="e01f8-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e01f8-118">**Value**</span></span>|<span data-ttu-id="e01f8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e01f8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e01f8-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e01f8-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e01f8-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e01f8-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e01f8-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e01f8-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e01f8-123">Der Status der Aufgabe Annahme ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e01f8-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="e01f8-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e01f8-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e01f8-125">Beauftragte für die Aufgabe hat die Aufgabe angenommen.</span><span class="sxs-lookup"><span data-stu-id="e01f8-125">The task assignee accepted the task.</span></span> <span data-ttu-id="e01f8-126">Dieser Wert wird festgelegt, wenn der Client eine Aufgabe Annahme verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e01f8-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="e01f8-127">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="e01f8-127">0x00000003</span></span>  <br/> |<span data-ttu-id="e01f8-128">Beauftragte für die Aufgabe abgelehnt, die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="e01f8-128">The task assignee rejected the task.</span></span> <span data-ttu-id="e01f8-129">Dieser Wert wird festgelegt, wenn der Client eine Aufgabe Ablehnung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e01f8-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e01f8-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e01f8-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e01f8-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e01f8-131">Protocol specifications</span></span>

<span data-ttu-id="e01f8-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e01f8-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e01f8-133">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e01f8-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e01f8-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e01f8-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e01f8-135">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="e01f8-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e01f8-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e01f8-136">Header files</span></span>

<span data-ttu-id="e01f8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e01f8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e01f8-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e01f8-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e01f8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e01f8-139">See also</span></span>



[<span data-ttu-id="e01f8-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e01f8-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e01f8-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e01f8-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e01f8-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e01f8-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e01f8-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e01f8-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

