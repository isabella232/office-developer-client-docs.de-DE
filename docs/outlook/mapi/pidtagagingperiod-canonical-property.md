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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391178"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="f3372-103">PidTagAgingPeriod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3372-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="f3372-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3372-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3372-105">Stellt die Anzahl der Einheiten, die verwendet werden, um die Dauer zu ermitteln, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f3372-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="f3372-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3372-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3372-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="f3372-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="f3372-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f3372-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3372-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="f3372-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="f3372-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="f3372-110">Property type:</span></span>  <br/> |<span data-ttu-id="f3372-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3372-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3372-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f3372-112">Area:</span></span>  <br/> |<span data-ttu-id="f3372-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="f3372-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3372-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3372-114">Remarks</span></span>

<span data-ttu-id="f3372-115">Die Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird, wird durch die beiden Eigenschaften **PR_AGING_PERIOD** und **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f3372-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="f3372-116">**PR_AGING_GRANULARITY** stellt die Zeiteinheit, in der **PR_AGING_PERIOD** ausgedrückt wird, wenn diese Zeitdauer zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f3372-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="f3372-117">Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="f3372-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="f3372-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3372-118">**Name**</span></span>|<span data-ttu-id="f3372-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3372-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3372-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="f3372-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="f3372-121">**PR_AGING_PERIOD** ist in der Anzahl von Monaten definiert.</span><span class="sxs-lookup"><span data-stu-id="f3372-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="f3372-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="f3372-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="f3372-123">**PR_AGING_PERIOD** ist in die Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="f3372-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="f3372-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="f3372-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="f3372-125">**PR_AGING_PERIOD** ist in der Anzahl der Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="f3372-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="f3372-126">Beispielsweise, wenn ein Ordner Archive eines Elements, nachdem das Element in den Ordner für zwei Wochen zu löschen, und klicken Sie dann auf **PR_AGING_GRANULARITY** wurde ist **AG_WEEKS** und **PR_AGING_PERIOD** 2.</span><span class="sxs-lookup"><span data-stu-id="f3372-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f3372-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3372-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3372-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f3372-128">Protocol specifications</span></span>

<span data-ttu-id="f3372-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3372-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3372-130">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="f3372-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="f3372-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3372-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3372-132">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="f3372-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="f3372-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3372-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3372-134">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f3372-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3372-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f3372-135">Header files</span></span>

<span data-ttu-id="f3372-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3372-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3372-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f3372-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3372-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3372-138">Mapitags.h</span></span>
  
> <span data-ttu-id="f3372-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f3372-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3372-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3372-140">See also</span></span>



[<span data-ttu-id="f3372-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3372-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3372-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3372-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3372-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f3372-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3372-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f3372-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

