---
title: PidTagAgingGranularity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1b5b36c3a05ef17e319ef236b032b7d07ce8fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589420"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="b1103-103">PidTagAgingGranularity (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1103-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="b1103-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1103-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1103-105">Stellt die Zeiteinheit, die verwendet wird, bei der Bestimmung der Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b1103-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1103-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1103-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1103-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b1103-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="b1103-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b1103-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1103-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="b1103-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="b1103-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1103-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1103-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1103-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1103-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1103-112">Area:</span></span>  <br/> |<span data-ttu-id="b1103-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="b1103-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1103-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b1103-114">Remarks</span></span>

<span data-ttu-id="b1103-115">Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="b1103-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="b1103-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1103-116">**Name**</span></span>|<span data-ttu-id="b1103-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b1103-117">**Value**</span></span>|<span data-ttu-id="b1103-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1103-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1103-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="b1103-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="b1103-120">0</span><span class="sxs-lookup"><span data-stu-id="b1103-120">0</span></span>  <br/> |<span data-ttu-id="b1103-121">**PR_AGING_PERIOD** ist in der Anzahl von Monaten definiert.</span><span class="sxs-lookup"><span data-stu-id="b1103-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="b1103-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="b1103-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="b1103-123">1</span><span class="sxs-lookup"><span data-stu-id="b1103-123">1</span></span>  <br/> |<span data-ttu-id="b1103-124">**PR_AGING_PERIOD** ist in die Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="b1103-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="b1103-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="b1103-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="b1103-126">2</span><span class="sxs-lookup"><span data-stu-id="b1103-126">2</span></span>  <br/> |<span data-ttu-id="b1103-127">**PR_AGING_PERIOD** ist in der Anzahl der Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="b1103-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="b1103-128">Die Zeitdauer, die ein Element in einem Ordner bleibt, bevor das Element archiviert wird, wird durch die beiden Eigenschaften [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) und **PR_AGING_GRANULARITY**bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b1103-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="b1103-129">**PR_AGING_PERIOD** stellt die Anzahl der Einheiten, die das Element im Ordner bleibt, bevor es archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b1103-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1103-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1103-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1103-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1103-131">Protocol specifications</span></span>

<span data-ttu-id="b1103-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1103-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1103-133">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b1103-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1103-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1103-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1103-135">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="b1103-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="b1103-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1103-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1103-137">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b1103-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1103-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b1103-138">Header files</span></span>

<span data-ttu-id="b1103-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1103-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1103-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b1103-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1103-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1103-141">Mapitags.h</span></span>
  
> <span data-ttu-id="b1103-142">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b1103-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1103-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1103-143">See also</span></span>



[<span data-ttu-id="b1103-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1103-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1103-145">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1103-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1103-146">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1103-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1103-147">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1103-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

