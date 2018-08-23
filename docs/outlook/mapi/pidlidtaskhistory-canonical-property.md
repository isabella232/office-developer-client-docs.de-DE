---
title: PidLidTaskHistory (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ba900ec4b8c8f1bcc2c85aae6c78ab59a43ee3cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563625"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="2efbc-103">PidLidTaskHistory (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2efbc-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="2efbc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2efbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2efbc-105">Gibt den Typ der Änderung an, die für die Aufgabe zuletzt vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="2efbc-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2efbc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2efbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2efbc-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="2efbc-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="2efbc-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="2efbc-108">Property set:</span></span>  <br/> |<span data-ttu-id="2efbc-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2efbc-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2efbc-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="2efbc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2efbc-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="2efbc-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="2efbc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2efbc-112">Data type:</span></span>  <br/> |<span data-ttu-id="2efbc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2efbc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2efbc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2efbc-114">Area:</span></span>  <br/> |<span data-ttu-id="2efbc-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2efbc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2efbc-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="2efbc-116">Remarks</span></span>

<span data-ttu-id="2efbc-117">Wenn der Wert dieser Eigenschaft festgelegt ist, muss auch die **DispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md))-Eigenschaft auf die aktuelle Zeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2efbc-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="2efbc-118">In der folgenden Tabelle werden die **DispidTaskHistory** Eigenschaftenwerte, in der Reihenfolge der Priorität niedriger aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2efbc-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="2efbc-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2efbc-119">**Value**</span></span>|<span data-ttu-id="2efbc-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2efbc-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2efbc-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="2efbc-121">0x00000004</span></span>  <br/> |<span data-ttu-id="2efbc-122">Die **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md))-Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2efbc-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="2efbc-123">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="2efbc-123">0x00000003</span></span>  <br/> |<span data-ttu-id="2efbc-124">Eine andere Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2efbc-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="2efbc-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2efbc-125">0x00000001</span></span>  <br/> |<span data-ttu-id="2efbc-126">Beauftragte für die Aufgabe angenommen für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2efbc-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="2efbc-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2efbc-127">0x00000002</span></span>  <br/> |<span data-ttu-id="2efbc-128">Beauftragte für die Aufgabe abgelehnt für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="2efbc-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="2efbc-129">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="2efbc-129">0x00000005</span></span>  <br/> |<span data-ttu-id="2efbc-130">Die Aufgabe wurde einer zugewiesenen Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2efbc-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="2efbc-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2efbc-131">0x00000000</span></span>  <br/> |<span data-ttu-id="2efbc-132">Keine Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="2efbc-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2efbc-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2efbc-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2efbc-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2efbc-134">Protocol specifications</span></span>

<span data-ttu-id="2efbc-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2efbc-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2efbc-136">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2efbc-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2efbc-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2efbc-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2efbc-138">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="2efbc-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2efbc-139">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2efbc-139">Header files</span></span>

<span data-ttu-id="2efbc-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2efbc-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="2efbc-141">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2efbc-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2efbc-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2efbc-142">See also</span></span>



[<span data-ttu-id="2efbc-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2efbc-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2efbc-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2efbc-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2efbc-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2efbc-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2efbc-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2efbc-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

