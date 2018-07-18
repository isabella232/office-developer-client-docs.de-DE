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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a95fc30de7511672cb27c9dd6fbc37b96e822e77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793863"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="254d5-103">PidLidTaskResetReminder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="254d5-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="254d5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="254d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="254d5-105">Gibt an, ob zukünftige Instanzen von Aufgabenserien Erinnerungen, benötigen, obwohl **DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="254d5-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="254d5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="254d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="254d5-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="254d5-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="254d5-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="254d5-108">Property set:</span></span>  <br/> |<span data-ttu-id="254d5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="254d5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="254d5-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="254d5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="254d5-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="254d5-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="254d5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="254d5-112">Data type:</span></span>  <br/> |<span data-ttu-id="254d5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="254d5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="254d5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="254d5-114">Area:</span></span>  <br/> |<span data-ttu-id="254d5-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="254d5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="254d5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="254d5-116">Remarks</span></span>

<span data-ttu-id="254d5-117">Dieser Wert wird auf TRUE festgelegt, wenn die Aufgabe Erinnerung geschlossen ist, und andernfalls auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="254d5-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="254d5-118">Wenn nicht festgelegt, wird davon ausgegangen, dass Standardwert ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="254d5-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="254d5-119">Wie in [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)angegeben gibt die **DispidReminderSet** -Eigenschaft, ob eine Erinnerung für den Vorgang festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="254d5-119">As specified in [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="254d5-120">Diese Eigenschaft gibt jedoch nur das Vorhandensein einer Erinnerung für eine einzelne Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="254d5-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="254d5-121">Es kann nicht verwendet werden, als eigenständige Anwendung, um festzustellen, ob eine zukünftige Instanz einer Aufgabenserie eine Erinnerung benötigt.</span><span class="sxs-lookup"><span data-stu-id="254d5-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="254d5-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="254d5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="254d5-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="254d5-123">Protocol specifications</span></span>

<span data-ttu-id="254d5-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254d5-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254d5-125">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="254d5-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="254d5-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254d5-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254d5-127">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="254d5-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="254d5-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254d5-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254d5-129">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="254d5-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="254d5-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="254d5-130">Header files</span></span>

<span data-ttu-id="254d5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="254d5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="254d5-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="254d5-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="254d5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="254d5-133">See also</span></span>



[<span data-ttu-id="254d5-134">Kanonische PidLidReminderSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="254d5-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="254d5-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="254d5-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="254d5-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="254d5-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="254d5-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="254d5-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="254d5-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="254d5-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

