---
title: PidLidTaskResetReminder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316618"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="bfe8b-103">PidLidTaskResetReminder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bfe8b-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="bfe8b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe8b-105">Gibt an, ob zukünftige Instanzen wiederkehrender Vorgänge Erinnerungen benötigen, auch wenn **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe8b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bfe8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfe8b-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="bfe8b-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="bfe8b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="bfe8b-108">Property set:</span></span>  <br/> |<span data-ttu-id="bfe8b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bfe8b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bfe8b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bfe8b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bfe8b-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="bfe8b-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="bfe8b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bfe8b-112">Data type:</span></span>  <br/> |<span data-ttu-id="bfe8b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bfe8b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bfe8b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bfe8b-114">Area:</span></span>  <br/> |<span data-ttu-id="bfe8b-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bfe8b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe8b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfe8b-116">Remarks</span></span>

<span data-ttu-id="bfe8b-117">Dieser Wert wird auf TRUE festgelegt, wenn die Erinnerung des Vorgangs verworfen wird, und andernfalls auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="bfe8b-118">Wenn der Wert nicht festgelegt ist, wird der Standardwert FALSE angenommen.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="bfe8b-119">Wie in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)angegeben, gibt die **dispidReminderSet-Eigenschaft** an, ob eine Erinnerung für den Vorgang festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="bfe8b-120">Diese Eigenschaft gibt jedoch nur das Vorhandensein einer Erinnerung für einen einzelnen Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="bfe8b-121">Sie kann nicht allein verwendet werden, um zu bestimmen, ob eine zukünftige Instanz einer wiederkehrenden Aufgabe eine Erinnerung benötigt.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bfe8b-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bfe8b-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfe8b-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bfe8b-123">Protocol specifications</span></span>

<span data-ttu-id="bfe8b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8b-125">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfe8b-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8b-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8b-127">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="bfe8b-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe8b-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe8b-129">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfe8b-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bfe8b-130">Header files</span></span>

<span data-ttu-id="bfe8b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfe8b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfe8b-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bfe8b-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfe8b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfe8b-133">See also</span></span>



[<span data-ttu-id="bfe8b-134">Kanonische PidLidReminderSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bfe8b-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="bfe8b-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfe8b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfe8b-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe8b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfe8b-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bfe8b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfe8b-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bfe8b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

