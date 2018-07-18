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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1fd1b06bbaa10c2d7c71ee4c161fd6a980da1865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794059"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="fde6d-103">PidTagAgingPeriod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fde6d-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="fde6d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fde6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fde6d-105">Stellt die Anzahl der Einheiten, die verwendet werden, um die Dauer zu ermitteln, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="fde6d-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="fde6d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fde6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fde6d-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="fde6d-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="fde6d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="fde6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fde6d-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="fde6d-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="fde6d-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="fde6d-110">Property type:</span></span>  <br/> |<span data-ttu-id="fde6d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fde6d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fde6d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fde6d-112">Area:</span></span>  <br/> |<span data-ttu-id="fde6d-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="fde6d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fde6d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fde6d-114">Remarks</span></span>

<span data-ttu-id="fde6d-115">Die Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird, wird durch die beiden Eigenschaften **PR_AGING_PERIOD** und **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="fde6d-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="fde6d-116">**PR_AGING_GRANULARITY** stellt die Zeiteinheit, in der **PR_AGING_PERIOD** ausgedrückt wird, wenn diese Zeitdauer zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fde6d-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="fde6d-117">Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="fde6d-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="fde6d-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="fde6d-118">**Name**</span></span>|<span data-ttu-id="fde6d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fde6d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fde6d-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="fde6d-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="fde6d-121">**PR_AGING_PERIOD** ist in der Anzahl von Monaten definiert.</span><span class="sxs-lookup"><span data-stu-id="fde6d-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="fde6d-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="fde6d-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="fde6d-123">**PR_AGING_PERIOD** ist in die Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="fde6d-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="fde6d-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="fde6d-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="fde6d-125">**PR_AGING_PERIOD** ist in der Anzahl der Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="fde6d-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="fde6d-126">Beispielsweise, wenn ein Ordner Archive eines Elements, nachdem das Element in den Ordner für zwei Wochen zu löschen, und klicken Sie dann auf **PR_AGING_GRANULARITY** wurde ist **AG_WEEKS** und **PR_AGING_PERIOD** 2.</span><span class="sxs-lookup"><span data-stu-id="fde6d-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fde6d-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fde6d-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fde6d-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fde6d-128">Protocol specifications</span></span>

<span data-ttu-id="fde6d-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fde6d-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fde6d-130">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="fde6d-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="fde6d-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fde6d-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fde6d-132">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="fde6d-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="fde6d-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fde6d-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fde6d-134">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fde6d-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fde6d-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fde6d-135">Header files</span></span>

<span data-ttu-id="fde6d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fde6d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="fde6d-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fde6d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="fde6d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fde6d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="fde6d-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fde6d-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fde6d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fde6d-140">See also</span></span>



[<span data-ttu-id="fde6d-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fde6d-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fde6d-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fde6d-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fde6d-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fde6d-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fde6d-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fde6d-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

