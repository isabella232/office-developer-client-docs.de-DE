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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391794"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="88fab-103">PidLidTaskDueDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88fab-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="88fab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88fab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88fab-105">Stellt das Datum, wenn der Benutzer zum Ausführen der Aufgabe erwartet.</span><span class="sxs-lookup"><span data-stu-id="88fab-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88fab-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="88fab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88fab-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="88fab-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="88fab-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="88fab-108">Property set:</span></span>  <br/> |<span data-ttu-id="88fab-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="88fab-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="88fab-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="88fab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88fab-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="88fab-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="88fab-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="88fab-112">Data type:</span></span>  <br/> |<span data-ttu-id="88fab-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="88fab-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="88fab-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="88fab-114">Area:</span></span>  <br/> |<span data-ttu-id="88fab-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="88fab-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88fab-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88fab-116">Remarks</span></span>

<span data-ttu-id="88fab-117">Die Aufgabe wurde ohne Fälligkeitsdatum, wenn diese Eigenschaft nicht festgelegt oder legen Sie 0x5AE980E0 (1,525,252,320) ist.</span><span class="sxs-lookup"><span data-stu-id="88fab-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="88fab-118">Jedoch ist ein Fälligkeitsdatum optional nur, wenn keine Startdatum in der Eigenschaft **DispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="88fab-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="88fab-119">Wenn der Vorgang ein Fälligkeitsdatum hat, der Wert benötigen eine Zeitkomponente Mitternacht und die **DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft muss ebenfalls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="88fab-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="88fab-120">Wenn **DispidTaskStartDate** ein Startdatum aufweist, muss der Wert der Eigenschaft **DispidTaskDueDate** größer als oder gleich dem Wert der **DispidTaskStartDate**sein.</span><span class="sxs-lookup"><span data-stu-id="88fab-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88fab-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88fab-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88fab-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="88fab-122">Protocol specifications</span></span>

<span data-ttu-id="88fab-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88fab-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88fab-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="88fab-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88fab-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88fab-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88fab-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="88fab-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="88fab-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88fab-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88fab-128">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="88fab-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88fab-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="88fab-129">Header files</span></span>

<span data-ttu-id="88fab-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88fab-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="88fab-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="88fab-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88fab-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88fab-132">See also</span></span>



[<span data-ttu-id="88fab-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88fab-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88fab-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88fab-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88fab-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="88fab-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88fab-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="88fab-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

