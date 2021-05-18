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
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303010"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="254c6-103">PidLidTaskHistory (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="254c6-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="254c6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="254c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="254c6-105">Gibt den Typ der Änderung an, die zuletzt an der Aufgabe vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="254c6-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="254c6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="254c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="254c6-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="254c6-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="254c6-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="254c6-108">Property set:</span></span>  <br/> |<span data-ttu-id="254c6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="254c6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="254c6-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="254c6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="254c6-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="254c6-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="254c6-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="254c6-112">Data type:</span></span>  <br/> |<span data-ttu-id="254c6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="254c6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="254c6-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="254c6-114">Area:</span></span>  <br/> |<span data-ttu-id="254c6-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="254c6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="254c6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="254c6-116">Remarks</span></span>

<span data-ttu-id="254c6-117">Wenn der Wert dieser Eigenschaft festgelegt ist, muss auch die **eigenschaft dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) auf die aktuelle Uhrzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="254c6-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="254c6-118">In der folgenden Tabelle sind **die werte der dispidTaskHistory-Eigenschaft** aufgeführt, die in der Reihenfolge der abnehmenden Priorität aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="254c6-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="254c6-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="254c6-119">**Value**</span></span>|<span data-ttu-id="254c6-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="254c6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="254c6-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="254c6-121">0x00000004</span></span>  <br/> |<span data-ttu-id="254c6-122">Die **eigenschaft dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="254c6-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="254c6-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="254c6-123">0x00000003</span></span>  <br/> |<span data-ttu-id="254c6-124">Eine andere Eigenschaft wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="254c6-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="254c6-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="254c6-125">0x00000001</span></span>  <br/> |<span data-ttu-id="254c6-126">Der Aufgabenbef?hnte hat diese Aufgabe angenommen.</span><span class="sxs-lookup"><span data-stu-id="254c6-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="254c6-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="254c6-127">0x00000002</span></span>  <br/> |<span data-ttu-id="254c6-128">Der Aufgabenbef?hnte hat diesen Vorgang abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="254c6-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="254c6-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="254c6-129">0x00000005</span></span>  <br/> |<span data-ttu-id="254c6-130">Die Aufgabe wurde einem Aufgabenbef nen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="254c6-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="254c6-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="254c6-131">0x00000000</span></span>  <br/> |<span data-ttu-id="254c6-132">Es wurden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="254c6-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="254c6-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="254c6-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="254c6-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="254c6-134">Protocol specifications</span></span>

<span data-ttu-id="254c6-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254c6-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254c6-136">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="254c6-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="254c6-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254c6-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254c6-138">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="254c6-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="254c6-139">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="254c6-139">Header files</span></span>

<span data-ttu-id="254c6-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="254c6-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="254c6-141">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="254c6-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="254c6-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="254c6-142">See also</span></span>



[<span data-ttu-id="254c6-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="254c6-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="254c6-144">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="254c6-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="254c6-145">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="254c6-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="254c6-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="254c6-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

