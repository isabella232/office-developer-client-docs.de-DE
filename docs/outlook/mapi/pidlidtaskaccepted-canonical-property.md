---
title: Kanonische PidLidTaskAccepted-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7448768a0a35cbf53b481eab0571b405fead1544
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793819"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="acce3-103">Kanonische PidLidTaskAccepted-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="acce3-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="acce3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="acce3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="acce3-105">Gibt an, ob eine Aufgabe zugewiesenen auf eine Aufgabenanfrage beantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="acce3-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="acce3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="acce3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acce3-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="acce3-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="acce3-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="acce3-108">Property set:</span></span>  <br/> |<span data-ttu-id="acce3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="acce3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="acce3-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="acce3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="acce3-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="acce3-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="acce3-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="acce3-112">Data type:</span></span>  <br/> |<span data-ttu-id="acce3-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="acce3-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="acce3-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="acce3-114">Area:</span></span>  <br/> |<span data-ttu-id="acce3-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="acce3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acce3-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acce3-116">Remarks</span></span>

<span data-ttu-id="acce3-117">Der Client wird diese Eigenschaft auf false festgelegt, eine neue Aufgabe, oder des Clients wird diese Eigenschaft auf TRUE festgelegt, wenn eine Aufgabe angenommen oder abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="acce3-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="acce3-118">Bleibt die Eigenschaft nicht festgelegt ist, wird davon ausgegangen, dass der Wert FALSE.</span><span class="sxs-lookup"><span data-stu-id="acce3-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="acce3-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="acce3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="acce3-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="acce3-120">Protocol specifications</span></span>

<span data-ttu-id="acce3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acce3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acce3-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="acce3-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="acce3-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acce3-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acce3-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="acce3-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="acce3-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="acce3-125">Header files</span></span>

<span data-ttu-id="acce3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acce3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="acce3-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="acce3-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acce3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acce3-128">See also</span></span>



[<span data-ttu-id="acce3-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="acce3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="acce3-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="acce3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="acce3-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="acce3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="acce3-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="acce3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

