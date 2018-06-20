---
title: Kanonische PidLidTaskDeadOccurrence-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 14207e513e935a296ff9b953b92ab1ab9ab41fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793814"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="35a0e-103">Kanonische PidLidTaskDeadOccurrence-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35a0e-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="35a0e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35a0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35a0e-105">Gibt an, ob neue Vorkommen generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="35a0e-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35a0e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35a0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35a0e-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="35a0e-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="35a0e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="35a0e-108">Property set:</span></span>  <br/> |<span data-ttu-id="35a0e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="35a0e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="35a0e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="35a0e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="35a0e-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="35a0e-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="35a0e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35a0e-112">Data type:</span></span>  <br/> |<span data-ttu-id="35a0e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="35a0e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="35a0e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35a0e-114">Area:</span></span>  <br/> |<span data-ttu-id="35a0e-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="35a0e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35a0e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35a0e-116">Remarks</span></span>

<span data-ttu-id="35a0e-117">Ein Serienmuster ist nicht mehr gültig, wenn die letzte Instanz befindet sich in der Vergangenheit oder die angegebene Anzahl von Instanzen generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="35a0e-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="35a0e-118">Der Client wird diese Eigenschaft auf FALSE für eine neue Aufgabe oder auf true fest, wenn die letzte Instanz einer Aufgabenserie generiert wird.</span><span class="sxs-lookup"><span data-stu-id="35a0e-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="35a0e-119">Beim Kopieren eines Vorgangs, um eine neue Instanz generieren, wird diese Eigenschaft für die Kopie auf TRUE festgelegt, das die Instanz abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="35a0e-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35a0e-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35a0e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35a0e-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="35a0e-121">Protocol specifications</span></span>

<span data-ttu-id="35a0e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35a0e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35a0e-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="35a0e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35a0e-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35a0e-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35a0e-125">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="35a0e-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="35a0e-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35a0e-126">Header files</span></span>

<span data-ttu-id="35a0e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35a0e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="35a0e-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35a0e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35a0e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a0e-129">See also</span></span>



[<span data-ttu-id="35a0e-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35a0e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35a0e-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35a0e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35a0e-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35a0e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35a0e-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35a0e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
