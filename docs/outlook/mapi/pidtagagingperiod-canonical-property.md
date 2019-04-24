---
title: Kanonische Pidtagagingperiod (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360116"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="22024-103">Kanonische Pidtagagingperiod (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22024-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="22024-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22024-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22024-105">Stellt die Anzahl der Zeiteinheiten dar, die verwendet werden, um zu bestimmen, wie lange ein Element in einem Ordner verbleiben soll, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="22024-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="22024-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="22024-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22024-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="22024-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="22024-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="22024-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22024-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="22024-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="22024-110">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="22024-110">Property type:</span></span>  <br/> |<span data-ttu-id="22024-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22024-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22024-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="22024-112">Area:</span></span>  <br/> |<span data-ttu-id="22024-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="22024-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22024-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22024-114">Remarks</span></span>

<span data-ttu-id="22024-115">Die Zeitdauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird, wird durch zwei Eigenschaften bestimmt: **PR_AGING_PERIOD** und **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="22024-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="22024-116">**PR_AGING_GRANULARITY** stellt die Zeiteinheit dar, in der **PR_AGING_PERIOD** ausgedrückt wird, wenn diese Zeitdauer bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="22024-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="22024-117">Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="22024-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="22024-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="22024-118">**Name**</span></span>|<span data-ttu-id="22024-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22024-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22024-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="22024-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="22024-121">**PR_AGING_PERIOD** ist in der Anzahl der Monate definiert.</span><span class="sxs-lookup"><span data-stu-id="22024-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="22024-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="22024-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="22024-123">**PR_AGING_PERIOD** ist in der Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="22024-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="22024-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="22024-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="22024-125">**PR_AGING_PERIOD** wird in Tagen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22024-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="22024-126">Wenn ein Ordner ein Element beispielsweise nur archiviert, nachdem sich das Element zwei Wochen lang im Ordner befindet, dann ist **PR_AGING_GRANULARITY** **AG_WEEKS** , und **PR_AGING_PERIOD** ist 2.</span><span class="sxs-lookup"><span data-stu-id="22024-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="22024-127">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22024-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22024-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="22024-128">Protocol specifications</span></span>

<span data-ttu-id="22024-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22024-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22024-130">Stellt Definitionen für Eigenschaftensätze bereit.</span><span class="sxs-lookup"><span data-stu-id="22024-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="22024-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22024-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22024-132">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22024-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="22024-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22024-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22024-134">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="22024-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22024-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="22024-135">Header files</span></span>

<span data-ttu-id="22024-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="22024-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="22024-137">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="22024-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="22024-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="22024-138">Mapitags.h</span></span>
  
> <span data-ttu-id="22024-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="22024-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22024-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22024-140">See also</span></span>



[<span data-ttu-id="22024-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22024-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22024-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22024-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22024-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="22024-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22024-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="22024-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

