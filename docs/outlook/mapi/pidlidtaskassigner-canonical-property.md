---
title: Kanonische Pidlidtaskassigner (-Eigenschaft
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
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340089"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="ffb68-103">Kanonische Pidlidtaskassigner (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ffb68-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="ffb68-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffb68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ffb68-105">Benennt den Benutzer, dem die Aufgabe zuletzt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ffb68-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffb68-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ffb68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffb68-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="ffb68-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="ffb68-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ffb68-108">Property set:</span></span>  <br/> |<span data-ttu-id="ffb68-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ffb68-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ffb68-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="ffb68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ffb68-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="ffb68-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="ffb68-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ffb68-112">Data type:</span></span>  <br/> |<span data-ttu-id="ffb68-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ffb68-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ffb68-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ffb68-114">Area:</span></span>  <br/> |<span data-ttu-id="ffb68-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ffb68-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffb68-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffb68-116">Remarks</span></span>

<span data-ttu-id="ffb68-117">Wenn die Aufgabe nicht zugewiesen wurde, wird diese Eigenschaft nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffb68-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="ffb68-118">Da der Client diese Eigenschaft festlegt, nachdem der Aufgabenempfänger eine Aufgabenanforderung erhalten hat, wird die Eigenschaft nicht für die Kopie der Aufgabe des Aufgaben beauftragten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffb68-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="ffb68-119">Wenn der Client einen Aufgaben beauftragten aus der Liste Aufgaben Verteiler in der **dispidTaskMyDelegators** ([pidlidtaskassigners (](pidlidtaskassigners-canonical-property.md))-Eigenschaft hinzufügt oder daraus entfernt, muss die **dispidTaskDelegator** ([pidlidtaskassigner (](pidlidtaskassigner-canonical-property.md))-Eigenschaft auf den hinzugefügten Wert festgelegt werden. oder entfernter Aufgaben Versender.</span><span class="sxs-lookup"><span data-stu-id="ffb68-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffb68-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ffb68-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffb68-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ffb68-121">Protocol specifications</span></span>

<span data-ttu-id="ffb68-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffb68-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffb68-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="ffb68-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffb68-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffb68-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffb68-125">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="ffb68-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffb68-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ffb68-126">Header files</span></span>

<span data-ttu-id="ffb68-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ffb68-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffb68-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ffb68-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffb68-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffb68-129">See also</span></span>



[<span data-ttu-id="ffb68-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffb68-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffb68-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffb68-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffb68-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ffb68-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffb68-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ffb68-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

