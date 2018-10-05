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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401514"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="b7db8-103">PidLidTaskDeadOccurrence (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7db8-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="b7db8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7db8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7db8-105">Gibt an, ob neue Vorkommen generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b7db8-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7db8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b7db8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7db8-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="b7db8-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="b7db8-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b7db8-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7db8-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b7db8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b7db8-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="b7db8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7db8-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="b7db8-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="b7db8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b7db8-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7db8-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b7db8-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b7db8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b7db8-114">Area:</span></span>  <br/> |<span data-ttu-id="b7db8-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b7db8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7db8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7db8-116">Remarks</span></span>

<span data-ttu-id="b7db8-117">Ein Serienmuster ist nicht mehr gültig, wenn die letzte Instanz befindet sich in der Vergangenheit oder die angegebene Anzahl von Instanzen generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7db8-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="b7db8-118">Der Client wird diese Eigenschaft auf FALSE für eine neue Aufgabe oder auf true fest, wenn die letzte Instanz einer Aufgabenserie generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7db8-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="b7db8-119">Beim Kopieren eines Vorgangs, um eine neue Instanz generieren, wird diese Eigenschaft für die Kopie auf TRUE festgelegt, das die Instanz abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b7db8-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7db8-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b7db8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7db8-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b7db8-121">Protocol specifications</span></span>

<span data-ttu-id="b7db8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7db8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7db8-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b7db8-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7db8-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7db8-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7db8-125">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="b7db8-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b7db8-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b7db8-126">Header files</span></span>

<span data-ttu-id="b7db8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7db8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7db8-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b7db8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7db8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7db8-129">See also</span></span>



[<span data-ttu-id="b7db8-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7db8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7db8-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7db8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7db8-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b7db8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7db8-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b7db8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

