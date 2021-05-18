---
title: PidLidTaskDueDate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303325"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="f314d-103">PidLidTaskDueDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f314d-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="f314d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f314d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f314d-105">Represents the date when the user expects to complete the task.</span><span class="sxs-lookup"><span data-stu-id="f314d-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f314d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f314d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f314d-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="f314d-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="f314d-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="f314d-108">Property set:</span></span>  <br/> |<span data-ttu-id="f314d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f314d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f314d-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f314d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f314d-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="f314d-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="f314d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f314d-112">Data type:</span></span>  <br/> |<span data-ttu-id="f314d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f314d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f314d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f314d-114">Area:</span></span>  <br/> |<span data-ttu-id="f314d-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f314d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f314d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f314d-116">Remarks</span></span>

<span data-ttu-id="f314d-117">Der Vorgang hat kein Fälligkeitsdatum, wenn diese Eigenschaft nicht festgelegt oder auf 0x5AE980E0 (1.525.252.320) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f314d-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="f314d-118">Ein Fälligkeitsdatum ist jedoch nur optional, wenn in der **eigenschaft dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) kein Startdatum angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f314d-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="f314d-119">Wenn der Vorgang ein Fälligkeitsdatum hat, muss der Wert eine Zeitkomponente von Mitternacht haben, und die **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft muss ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f314d-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="f314d-120">Wenn **dispidTaskStartDate** ein Startdatum hat, muss der Wert der **dispidTaskDueDate-Eigenschaft** größer oder gleich dem Wert von **dispidTaskStartDate sein.**</span><span class="sxs-lookup"><span data-stu-id="f314d-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f314d-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f314d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f314d-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f314d-122">Protocol specifications</span></span>

<span data-ttu-id="f314d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f314d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f314d-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f314d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f314d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f314d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f314d-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="f314d-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="f314d-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f314d-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f314d-128">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="f314d-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f314d-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f314d-129">Header files</span></span>

<span data-ttu-id="f314d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f314d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f314d-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f314d-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f314d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f314d-132">See also</span></span>



[<span data-ttu-id="f314d-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f314d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f314d-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f314d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f314d-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f314d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f314d-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f314d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

