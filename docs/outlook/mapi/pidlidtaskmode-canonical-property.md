---
title: PidLidTaskMode (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357939"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="c8184-103">PidLidTaskMode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c8184-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="c8184-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8184-105">Gibt den Zuweisungsstatus des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="c8184-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8184-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c8184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8184-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="c8184-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="c8184-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c8184-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8184-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c8184-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c8184-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c8184-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c8184-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="c8184-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="c8184-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c8184-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8184-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8184-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8184-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c8184-114">Area:</span></span>  <br/> |<span data-ttu-id="c8184-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c8184-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8184-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8184-116">Remarks</span></span>

<span data-ttu-id="c8184-117">Der Wert muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c8184-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="c8184-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c8184-118">**Value**</span></span>|<span data-ttu-id="c8184-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8184-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8184-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8184-120">0x00000000</span></span>  <br/> |<span data-ttu-id="c8184-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c8184-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="c8184-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c8184-122">0x00000001</span></span>  <br/> |<span data-ttu-id="c8184-123">Die Aufgabe ist in eine Vorgangsanforderung eingebettet.</span><span class="sxs-lookup"><span data-stu-id="c8184-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="c8184-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c8184-124">0x00000002</span></span>  <br/> |<span data-ttu-id="c8184-125">Der Vorgang wurde vom Aufgabenbef?hnten angenommen.</span><span class="sxs-lookup"><span data-stu-id="c8184-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="c8184-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c8184-126">0x00000003</span></span>  <br/> |<span data-ttu-id="c8184-127">Der Vorgang wurde vom Aufgabenbef?hnten abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="c8184-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="c8184-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c8184-128">0x00000004</span></span>  <br/> |<span data-ttu-id="c8184-129">Die Aufgabe wird in eine Vorgangsaktualisierung eingebettet.</span><span class="sxs-lookup"><span data-stu-id="c8184-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="c8184-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c8184-130">0x00000005</span></span>  <br/> |<span data-ttu-id="c8184-131">Der Vorgang wurde dem Aufgaben zuweisende Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c8184-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c8184-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8184-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8184-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c8184-133">Protocol specifications</span></span>

<span data-ttu-id="c8184-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8184-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8184-135">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c8184-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8184-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8184-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8184-137">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="c8184-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8184-138">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c8184-138">Header files</span></span>

<span data-ttu-id="c8184-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8184-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8184-140">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c8184-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8184-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8184-141">See also</span></span>



[<span data-ttu-id="c8184-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8184-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8184-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c8184-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8184-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c8184-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8184-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c8184-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

