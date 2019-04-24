---
title: Kanonische Pidlidtaskdeadoccurrence (-Eigenschaft
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
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303430"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="0099a-103">Kanonische Pidlidtaskdeadoccurrence (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0099a-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="0099a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0099a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0099a-105">Gibt an, ob neue Vorkommen generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0099a-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0099a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0099a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0099a-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="0099a-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="0099a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="0099a-108">Property set:</span></span>  <br/> |<span data-ttu-id="0099a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0099a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0099a-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="0099a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0099a-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="0099a-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="0099a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0099a-112">Data type:</span></span>  <br/> |<span data-ttu-id="0099a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0099a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0099a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0099a-114">Area:</span></span>  <br/> |<span data-ttu-id="0099a-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0099a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0099a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0099a-116">Remarks</span></span>

<span data-ttu-id="0099a-117">Ein Serienmuster ist nicht mehr wirksam, wenn sich seine letzte Instanz in der Vergangenheit befindet oder die angegebene Anzahl von Instanzen generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0099a-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="0099a-118">Der Client legt diese Eigenschaft für eine neue Aufgabe oder für TRUE fest, wenn Sie die letzte Instanz eines wiederkehrenden Vorgangs generiert.</span><span class="sxs-lookup"><span data-stu-id="0099a-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="0099a-119">Wenn Sie eine Aufgabe kopieren, um eine neue Instanz zu generieren, wird diese Eigenschaft in der Kopie, die die abgeschlossene Instanz ist, auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0099a-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0099a-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0099a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0099a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0099a-121">Protocol specifications</span></span>

<span data-ttu-id="0099a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0099a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0099a-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="0099a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0099a-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0099a-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0099a-125">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="0099a-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="0099a-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0099a-126">Header files</span></span>

<span data-ttu-id="0099a-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0099a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0099a-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0099a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0099a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0099a-129">See also</span></span>



[<span data-ttu-id="0099a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0099a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0099a-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0099a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0099a-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0099a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0099a-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0099a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

