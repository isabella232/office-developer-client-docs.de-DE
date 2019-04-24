---
title: Kanonische Pidlidtaskhistory (-Eigenschaft
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
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303010"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="2286d-103">Kanonische Pidlidtaskhistory (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2286d-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="2286d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2286d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2286d-105">Gibt den Typ der letzten Änderung an der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="2286d-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2286d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2286d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2286d-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="2286d-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="2286d-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="2286d-108">Property set:</span></span>  <br/> |<span data-ttu-id="2286d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2286d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2286d-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="2286d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2286d-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="2286d-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="2286d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2286d-112">Data type:</span></span>  <br/> |<span data-ttu-id="2286d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2286d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2286d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2286d-114">Area:</span></span>  <br/> |<span data-ttu-id="2286d-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2286d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2286d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2286d-116">Remarks</span></span>

<span data-ttu-id="2286d-117">Wenn der Wert dieser Eigenschaft festgelegt ist, muss die **dispidTaskLastUpdate** ([pidlidtasklastupdate (](pidlidtasklastupdate-canonical-property.md))-Eigenschaft auch auf die aktuelle Uhrzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2286d-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="2286d-118">In der folgenden Tabelle sind die Werte der **dispidTaskHistory** -Eigenschaft aufgeführt, die in der Reihenfolge der niedrigeren Priorität aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2286d-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="2286d-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2286d-119">**Value**</span></span>|<span data-ttu-id="2286d-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2286d-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2286d-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2286d-121">0x00000004</span></span>  <br/> |<span data-ttu-id="2286d-122">Die **dispidTaskDueDate** ([pidlidtaskduedate (](pidlidtaskduedate-canonical-property.md))-Eigenschaft wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="2286d-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="2286d-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2286d-123">0x00000003</span></span>  <br/> |<span data-ttu-id="2286d-124">Eine andere Eigenschaft wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="2286d-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="2286d-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2286d-125">0x00000001</span></span>  <br/> |<span data-ttu-id="2286d-126">Der Aufgabenempfänger hat diese Aufgabe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2286d-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="2286d-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2286d-127">0x00000002</span></span>  <br/> |<span data-ttu-id="2286d-128">Der Aufgabenempfänger hat diese Aufgabe abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="2286d-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="2286d-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2286d-129">0x00000005</span></span>  <br/> |<span data-ttu-id="2286d-130">Die Aufgabe wurde einem Aufgabenempfänger zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2286d-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="2286d-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2286d-131">0x00000000</span></span>  <br/> |<span data-ttu-id="2286d-132">Es wurden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="2286d-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2286d-133">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2286d-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2286d-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2286d-134">Protocol specifications</span></span>

<span data-ttu-id="2286d-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2286d-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2286d-136">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="2286d-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2286d-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2286d-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2286d-138">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="2286d-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2286d-139">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2286d-139">Header files</span></span>

<span data-ttu-id="2286d-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2286d-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="2286d-141">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2286d-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2286d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2286d-142">See also</span></span>



[<span data-ttu-id="2286d-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2286d-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2286d-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2286d-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2286d-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2286d-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2286d-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2286d-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

