---
title: Kanonische PidLidTaskAssigner-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5b711b1e0db0fab93016d3f1c979d81a142c9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793818"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="3a695-103">Kanonische PidLidTaskAssigner-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a695-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="3a695-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a695-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3a695-105">Namen der Benutzer, der zuletzt verwendet wurde die Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3a695-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a695-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3a695-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a695-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="3a695-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="3a695-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3a695-108">Property set:</span></span>  <br/> |<span data-ttu-id="3a695-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3a695-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3a695-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="3a695-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3a695-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="3a695-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="3a695-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3a695-112">Data type:</span></span>  <br/> |<span data-ttu-id="3a695-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a695-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3a695-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3a695-114">Area:</span></span>  <br/> |<span data-ttu-id="3a695-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3a695-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a695-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a695-116">Remarks</span></span>

<span data-ttu-id="3a695-117">Wenn die Aufgabe nicht zugewiesen wurde, bleibt diese Eigenschaft nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a695-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="3a695-118">Da der Client diese Eigenschaft festlegt, nachdem Beauftragte für die Aufgabe eine Aufgabenanfrage erhalten, wird die Eigenschaft nicht auf die Aufgabe delegierende Person Kopie der Aufgabe festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a695-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="3a695-119">Wenn der Client hinzugefügt oder entfernt eine Aufgabe delegierende Person aus der Aufgabenliste delegierende Person in der Eigenschaft **DispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), die **DispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md))-Eigenschaft muss auf das hinzugefügte festgelegt oder entfernte Aufgabe delegierende Person.</span><span class="sxs-lookup"><span data-stu-id="3a695-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a695-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3a695-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a695-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3a695-121">Protocol specifications</span></span>

<span data-ttu-id="3a695-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a695-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a695-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a695-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a695-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a695-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a695-125">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="3a695-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a695-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3a695-126">Header files</span></span>

<span data-ttu-id="3a695-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a695-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a695-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3a695-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a695-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a695-129">See also</span></span>



[<span data-ttu-id="3a695-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a695-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a695-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a695-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a695-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3a695-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a695-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3a695-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

