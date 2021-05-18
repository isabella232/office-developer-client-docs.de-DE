---
title: PidLidTaskDeadOccurrence (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303430"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="1fc87-103">PidLidTaskDeadOccurrence (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1fc87-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="1fc87-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fc87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fc87-105">Gibt an, ob neue Vorkommen generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1fc87-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1fc87-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1fc87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fc87-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="1fc87-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="1fc87-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="1fc87-108">Property set:</span></span>  <br/> |<span data-ttu-id="1fc87-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1fc87-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1fc87-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1fc87-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1fc87-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="1fc87-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="1fc87-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1fc87-112">Data type:</span></span>  <br/> |<span data-ttu-id="1fc87-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1fc87-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1fc87-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1fc87-114">Area:</span></span>  <br/> |<span data-ttu-id="1fc87-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1fc87-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fc87-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fc87-116">Remarks</span></span>

<span data-ttu-id="1fc87-117">Ein Serienmuster ist nicht mehr wirksam, wenn sich die letzte Instanz in der Vergangenheit befindet oder die angegebene Anzahl von Instanzen generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1fc87-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="1fc87-118">Der Client legt diese Eigenschaft für einen neuen Vorgang auf FALSE oder true fest, wenn die letzte Instanz einer wiederkehrenden Aufgabe generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fc87-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="1fc87-119">Wenn Sie eine Aufgabe kopieren, um eine neue Instanz zu generieren, wird diese Eigenschaft für die Kopie auf TRUE festgelegt, bei der es sich um die abgeschlossene Instanz handelt.</span><span class="sxs-lookup"><span data-stu-id="1fc87-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1fc87-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1fc87-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fc87-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1fc87-121">Protocol specifications</span></span>

<span data-ttu-id="1fc87-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fc87-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fc87-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1fc87-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fc87-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fc87-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fc87-125">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="1fc87-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="1fc87-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1fc87-126">Header files</span></span>

<span data-ttu-id="1fc87-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fc87-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fc87-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1fc87-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fc87-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc87-129">See also</span></span>



[<span data-ttu-id="1fc87-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fc87-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fc87-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1fc87-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fc87-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1fc87-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fc87-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1fc87-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

