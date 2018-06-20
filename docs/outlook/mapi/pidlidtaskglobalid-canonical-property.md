---
title: Kanonische PidLidTaskGlobalId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793826"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="422c9-103">Kanonische PidLidTaskGlobalId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="422c9-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="422c9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="422c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="422c9-105">Sucht nach einer vorhandenen Aufgabe anhand einer GUID, beim Empfang einer Aufgabenantwort oder Vorgang aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="422c9-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="422c9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="422c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="422c9-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="422c9-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="422c9-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="422c9-108">Property set:</span></span>  <br/> |<span data-ttu-id="422c9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="422c9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="422c9-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="422c9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="422c9-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="422c9-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="422c9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="422c9-112">Data type:</span></span>  <br/> |<span data-ttu-id="422c9-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="422c9-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="422c9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="422c9-114">Area:</span></span>  <br/> |<span data-ttu-id="422c9-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="422c9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="422c9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="422c9-116">Remarks</span></span>

<span data-ttu-id="422c9-117">Diese Eigenschaft bleibt für nicht zugewiesene Aufgaben nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="422c9-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="422c9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="422c9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="422c9-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="422c9-119">Protocol specifications</span></span>

<span data-ttu-id="422c9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="422c9-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="422c9-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="422c9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="422c9-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="422c9-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="422c9-123">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="422c9-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="422c9-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="422c9-124">Header files</span></span>

<span data-ttu-id="422c9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="422c9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="422c9-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="422c9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="422c9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="422c9-127">See also</span></span>



[<span data-ttu-id="422c9-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="422c9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="422c9-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="422c9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="422c9-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="422c9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="422c9-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="422c9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

