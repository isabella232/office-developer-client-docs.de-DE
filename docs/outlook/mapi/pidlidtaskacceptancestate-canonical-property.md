---
title: Kanonische Pidlidtaskacceptancestate (-Eigenschaft
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
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331290"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="455f3-103">Kanonische Pidlidtaskacceptancestate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="455f3-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="455f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="455f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="455f3-105">Gibt den Akzeptanz Status der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="455f3-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="455f3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="455f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="455f3-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="455f3-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="455f3-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="455f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="455f3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="455f3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="455f3-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="455f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="455f3-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="455f3-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="455f3-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="455f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="455f3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="455f3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="455f3-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="455f3-114">Area:</span></span>  <br/> |<span data-ttu-id="455f3-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="455f3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="455f3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="455f3-116">Remarks</span></span>

<span data-ttu-id="455f3-117">In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="455f3-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="455f3-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="455f3-118">**Value**</span></span>|<span data-ttu-id="455f3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="455f3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="455f3-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="455f3-120">0x00000000</span></span>  <br/> |<span data-ttu-id="455f3-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="455f3-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="455f3-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="455f3-122">0x00000001</span></span>  <br/> |<span data-ttu-id="455f3-123">Der Akzeptanz Status der Aufgabe ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="455f3-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="455f3-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="455f3-124">0x00000002</span></span>  <br/> |<span data-ttu-id="455f3-125">Der Aufgabenempfänger hat die Aufgabe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="455f3-125">The task assignee accepted the task.</span></span> <span data-ttu-id="455f3-126">Dieser Wert wird festgelegt, wenn der Client eine Aufgaben Akzeptanz verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="455f3-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="455f3-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="455f3-127">0x00000003</span></span>  <br/> |<span data-ttu-id="455f3-128">Der Task-Empfänger hat die Aufgabe abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="455f3-128">The task assignee rejected the task.</span></span> <span data-ttu-id="455f3-129">Dieser Wert wird festgelegt, wenn der Client eine Aufgaben Ablehnung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="455f3-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="455f3-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="455f3-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="455f3-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="455f3-131">Protocol specifications</span></span>

<span data-ttu-id="455f3-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="455f3-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="455f3-133">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="455f3-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="455f3-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="455f3-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="455f3-135">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="455f3-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="455f3-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="455f3-136">Header files</span></span>

<span data-ttu-id="455f3-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="455f3-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="455f3-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="455f3-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="455f3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="455f3-139">See also</span></span>



[<span data-ttu-id="455f3-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="455f3-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="455f3-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="455f3-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="455f3-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="455f3-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="455f3-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="455f3-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

