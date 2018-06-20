---
title: Kanonische PidLidTaskHistory-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793851"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="6e722-103">Kanonische PidLidTaskHistory-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e722-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="6e722-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e722-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e722-105">Gibt den Typ der Änderung an, die für die Aufgabe zuletzt vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6e722-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e722-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e722-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e722-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="6e722-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="6e722-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6e722-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e722-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6e722-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6e722-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6e722-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e722-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="6e722-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="6e722-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e722-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e722-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6e722-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6e722-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e722-114">Area:</span></span>  <br/> |<span data-ttu-id="6e722-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6e722-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e722-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e722-116">Remarks</span></span>

<span data-ttu-id="6e722-117">Wenn der Wert dieser Eigenschaft festgelegt ist, muss auch die **DispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md))-Eigenschaft auf die aktuelle Zeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6e722-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="6e722-118">In der folgenden Tabelle werden die **DispidTaskHistory** Eigenschaftenwerte, in der Reihenfolge der Priorität niedriger aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e722-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="6e722-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6e722-119">**Value**</span></span>|<span data-ttu-id="6e722-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e722-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e722-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="6e722-121">0x00000004</span></span>  <br/> |<span data-ttu-id="6e722-122">Die **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md))-Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e722-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="6e722-123">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="6e722-123">0x00000003</span></span>  <br/> |<span data-ttu-id="6e722-124">Eine andere Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e722-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="6e722-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e722-125">0x00000001</span></span>  <br/> |<span data-ttu-id="6e722-126">Beauftragte für die Aufgabe angenommen für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6e722-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="6e722-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6e722-127">0x00000002</span></span>  <br/> |<span data-ttu-id="6e722-128">Beauftragte für die Aufgabe abgelehnt für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6e722-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="6e722-129">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="6e722-129">0x00000005</span></span>  <br/> |<span data-ttu-id="6e722-130">Die Aufgabe wurde einer zugewiesenen Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6e722-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="6e722-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e722-131">0x00000000</span></span>  <br/> |<span data-ttu-id="6e722-132">Keine Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="6e722-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6e722-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e722-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e722-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e722-134">Protocol specifications</span></span>

<span data-ttu-id="6e722-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e722-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e722-136">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6e722-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e722-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e722-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e722-138">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="6e722-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e722-139">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6e722-139">Header files</span></span>

<span data-ttu-id="6e722-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e722-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e722-141">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6e722-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e722-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e722-142">See also</span></span>



[<span data-ttu-id="6e722-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e722-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e722-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e722-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e722-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e722-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e722-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e722-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

