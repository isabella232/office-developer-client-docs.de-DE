---
title: PidLidTaskAcceptanceState (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331290"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="e2d7b-103">PidLidTaskAcceptanceState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e2d7b-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="e2d7b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2d7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2d7b-105">Gibt den Annahmestatus des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2d7b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e2d7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2d7b-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="e2d7b-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="e2d7b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="e2d7b-108">Property set:</span></span>  <br/> |<span data-ttu-id="e2d7b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e2d7b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e2d7b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e2d7b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e2d7b-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="e2d7b-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="e2d7b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e2d7b-112">Data type:</span></span>  <br/> |<span data-ttu-id="e2d7b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2d7b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e2d7b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e2d7b-114">Area:</span></span>  <br/> |<span data-ttu-id="e2d7b-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e2d7b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2d7b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2d7b-116">Remarks</span></span>

<span data-ttu-id="e2d7b-117">In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="e2d7b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e2d7b-118">**Value**</span></span>|<span data-ttu-id="e2d7b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2d7b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2d7b-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d7b-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e2d7b-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e2d7b-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e2d7b-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e2d7b-123">Der Annahmestatus des Vorgangs ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="e2d7b-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e2d7b-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e2d7b-125">Der Aufgabenbef?hnte hat den Vorgang angenommen.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-125">The task assignee accepted the task.</span></span> <span data-ttu-id="e2d7b-126">Dieser Wert wird festgelegt, wenn der Client eine Vorgangsakzeptanz verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="e2d7b-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e2d7b-127">0x00000003</span></span>  <br/> |<span data-ttu-id="e2d7b-128">Der Aufgabenbef?hnte hat den Vorgang abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-128">The task assignee rejected the task.</span></span> <span data-ttu-id="e2d7b-129">Dieser Wert wird festgelegt, wenn der Client eine Vorgangsabweisung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e2d7b-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2d7b-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2d7b-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e2d7b-131">Protocol specifications</span></span>

<span data-ttu-id="e2d7b-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2d7b-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2d7b-133">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2d7b-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2d7b-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2d7b-135">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2d7b-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e2d7b-136">Header files</span></span>

<span data-ttu-id="e2d7b-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2d7b-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2d7b-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2d7b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d7b-139">See also</span></span>



[<span data-ttu-id="e2d7b-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2d7b-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2d7b-141">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e2d7b-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2d7b-142">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e2d7b-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2d7b-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e2d7b-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

