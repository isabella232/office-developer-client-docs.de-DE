---
title: PidTagAgingPeriod (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360116"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="c3f46-103">PidTagAgingPeriod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c3f46-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="c3f46-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3f46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3f46-105">Stellt die Anzahl der Zeiteinheiten dar, die verwendet werden, um die Dauer zu bestimmen, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c3f46-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="c3f46-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c3f46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3f46-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="c3f46-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="c3f46-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c3f46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3f46-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="c3f46-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="c3f46-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="c3f46-110">Property type:</span></span>  <br/> |<span data-ttu-id="c3f46-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c3f46-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c3f46-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c3f46-112">Area:</span></span>  <br/> |<span data-ttu-id="c3f46-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="c3f46-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3f46-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c3f46-114">Remarks</span></span>

<span data-ttu-id="c3f46-115">Die Dauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert **wird,** wird durch zwei Eigenschaften bestimmt: PR_AGING_PERIOD **[und PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="c3f46-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="c3f46-116">**PR_AGING_GRANULARITY** stellt die Zeiteinheit dar, in **der PR_AGING_PERIOD** ausgedrückt wird, wenn diese Dauer bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c3f46-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="c3f46-117">Die möglichen Werte **für PR_AGING_GRANULARITY** können einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="c3f46-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="c3f46-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="c3f46-118">**Name**</span></span>|<span data-ttu-id="c3f46-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3f46-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3f46-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="c3f46-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="c3f46-121">**PR_AGING_PERIOD** wird in der Anzahl der Monate definiert.</span><span class="sxs-lookup"><span data-stu-id="c3f46-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="c3f46-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="c3f46-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="c3f46-123">**PR_AGING_PERIOD** wird in der Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="c3f46-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="c3f46-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="c3f46-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="c3f46-125">**PR_AGING_PERIOD** wird in der Anzahl der Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="c3f46-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="c3f46-126">Wenn beispielsweise ein Ordner ein Element erst archiviert, nachdem sich das Element zwei Wochen  lang im  Ordner befindet, ist **PR_AGING_GRANULARITY** AG_WEEKS und PR_AGING_PERIOD 2.</span><span class="sxs-lookup"><span data-stu-id="c3f46-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c3f46-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3f46-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3f46-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c3f46-128">Protocol specifications</span></span>

<span data-ttu-id="c3f46-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3f46-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3f46-130">Stellt Eigenschaftensatzdefinitionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c3f46-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="c3f46-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3f46-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3f46-132">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3f46-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="c3f46-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3f46-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3f46-134">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c3f46-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3f46-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c3f46-135">Header files</span></span>

<span data-ttu-id="c3f46-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3f46-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3f46-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c3f46-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3f46-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3f46-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c3f46-139">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c3f46-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3f46-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f46-140">See also</span></span>



[<span data-ttu-id="c3f46-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3f46-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3f46-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c3f46-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3f46-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c3f46-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3f46-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c3f46-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

