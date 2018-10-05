---
title: PidLidTaskAcceptanceState(kanonische Eigenschaft)
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399151"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="33b39-103">PidLidTaskAcceptanceState(kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="33b39-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="33b39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33b39-105">Gibt den Annahmestatus des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="33b39-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33b39-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="33b39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33b39-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="33b39-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="33b39-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="33b39-108">Property set:</span></span>  <br/> |<span data-ttu-id="33b39-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="33b39-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="33b39-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="33b39-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="33b39-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="33b39-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="33b39-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="33b39-112">Data type:</span></span>  <br/> |<span data-ttu-id="33b39-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33b39-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33b39-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="33b39-114">Area:</span></span>  <br/> |<span data-ttu-id="33b39-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="33b39-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33b39-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33b39-116">Remarks</span></span>

<span data-ttu-id="33b39-117">In der folgenden Tabelle sind die möglichen Werte für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="33b39-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="33b39-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="33b39-118">**Value**</span></span>|<span data-ttu-id="33b39-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33b39-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33b39-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33b39-120">0x00000000</span></span>  <br/> |<span data-ttu-id="33b39-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="33b39-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="33b39-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="33b39-122">0x00000001</span></span>  <br/> |<span data-ttu-id="33b39-123">Der Status der Aufgabe Annahme ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="33b39-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="33b39-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="33b39-124">0x00000002</span></span>  <br/> |<span data-ttu-id="33b39-125">Beauftragte für die Aufgabe hat die Aufgabe angenommen.</span><span class="sxs-lookup"><span data-stu-id="33b39-125">The task assignee accepted the task.</span></span> <span data-ttu-id="33b39-126">Dieser Wert wird festgelegt, wenn der Client eine Aufgabe Annahme verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="33b39-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="33b39-127">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="33b39-127">0x00000003</span></span>  <br/> |<span data-ttu-id="33b39-128">Beauftragte für die Aufgabe abgelehnt, die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="33b39-128">The task assignee rejected the task.</span></span> <span data-ttu-id="33b39-129">Dieser Wert wird festgelegt, wenn der Client eine Aufgabe Ablehnung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="33b39-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="33b39-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="33b39-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33b39-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="33b39-131">Protocol specifications</span></span>

<span data-ttu-id="33b39-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33b39-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33b39-133">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="33b39-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33b39-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33b39-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33b39-135">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="33b39-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33b39-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="33b39-136">Header files</span></span>

<span data-ttu-id="33b39-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33b39-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="33b39-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="33b39-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33b39-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b39-139">See also</span></span>



[<span data-ttu-id="33b39-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33b39-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33b39-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33b39-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33b39-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="33b39-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33b39-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="33b39-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

