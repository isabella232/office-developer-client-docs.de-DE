---
title: PidLidTaskFRecurring (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb97d278640b4cdd2b14152bf4745f883fe2edba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793827"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="265da-103">PidLidTaskFRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="265da-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="265da-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="265da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="265da-105">Gibt an, ob der Vorgang ein Serienmuster enthält.</span><span class="sxs-lookup"><span data-stu-id="265da-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="265da-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="265da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="265da-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="265da-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="265da-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="265da-108">Property set:</span></span>  <br/> |<span data-ttu-id="265da-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="265da-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="265da-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="265da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="265da-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="265da-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="265da-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="265da-112">Data type:</span></span>  <br/> |<span data-ttu-id="265da-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="265da-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="265da-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="265da-114">Area:</span></span>  <br/> |<span data-ttu-id="265da-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="265da-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="265da-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="265da-116">Remarks</span></span>

<span data-ttu-id="265da-117">Wenn Sie diese Eigenschaft nicht festgelegt lassen, wird der Standardwert FALSE angenommen.</span><span class="sxs-lookup"><span data-stu-id="265da-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="265da-118">Wenn sie auf true festgelegt ist, die **DispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) festgelegt ist und **DispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) Eigenschaften auch als festgelegt werden müssen, die in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="265da-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="265da-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="265da-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="265da-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="265da-120">Protocol specifications</span></span>

<span data-ttu-id="265da-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="265da-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="265da-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="265da-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="265da-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="265da-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="265da-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="265da-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="265da-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="265da-125">Header files</span></span>

<span data-ttu-id="265da-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="265da-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="265da-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="265da-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="265da-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="265da-128">See also</span></span>



[<span data-ttu-id="265da-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="265da-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="265da-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="265da-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="265da-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="265da-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="265da-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="265da-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

