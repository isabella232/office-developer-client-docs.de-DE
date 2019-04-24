---
title: Kanonische Pidtagaginggranularity (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325585"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="0b877-103">Kanonische Pidtagaginggranularity (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b877-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="0b877-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b877-105">Stellt die Zeiteinheit dar, die verwendet wird, um zu bestimmen, wie lange ein Element in einem Ordner verbleiben soll, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0b877-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b877-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0b877-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b877-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="0b877-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="0b877-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0b877-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b877-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="0b877-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="0b877-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0b877-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b877-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b877-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b877-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0b877-112">Area:</span></span>  <br/> |<span data-ttu-id="0b877-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0b877-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b877-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b877-114">Remarks</span></span>

<span data-ttu-id="0b877-115">Die möglichen Werte für **PR_AGING_GRANULARITY** können eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="0b877-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="0b877-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="0b877-116">**Name**</span></span>|<span data-ttu-id="0b877-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0b877-117">**Value**</span></span>|<span data-ttu-id="0b877-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b877-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b877-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="0b877-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="0b877-120">0</span><span class="sxs-lookup"><span data-stu-id="0b877-120">0</span></span>  <br/> |<span data-ttu-id="0b877-121">**PR_AGING_PERIOD** ist in der Anzahl der Monate definiert.</span><span class="sxs-lookup"><span data-stu-id="0b877-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="0b877-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="0b877-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="0b877-123">1</span><span class="sxs-lookup"><span data-stu-id="0b877-123">1</span></span>  <br/> |<span data-ttu-id="0b877-124">**PR_AGING_PERIOD** ist in der Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="0b877-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="0b877-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="0b877-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="0b877-126">2</span><span class="sxs-lookup"><span data-stu-id="0b877-126">2</span></span>  <br/> |<span data-ttu-id="0b877-127">**PR_AGING_PERIOD** wird in Tagen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b877-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="0b877-128">Die Zeitdauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird, wird durch zwei Eigenschaften bestimmt: [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) und **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="0b877-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="0b877-129">**PR_AGING_PERIOD** stellt die Anzahl der Zeiteinheiten dar, die das Element im Ordner verbleiben soll, bevor es archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0b877-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0b877-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b877-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b877-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0b877-131">Protocol specifications</span></span>

<span data-ttu-id="0b877-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b877-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b877-133">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0b877-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b877-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b877-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b877-135">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b877-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0b877-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b877-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b877-137">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0b877-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b877-138">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0b877-138">Header files</span></span>

<span data-ttu-id="0b877-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0b877-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b877-140">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0b877-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b877-141">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0b877-141">Mapitags.h</span></span>
  
> <span data-ttu-id="0b877-142">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0b877-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b877-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b877-143">See also</span></span>



[<span data-ttu-id="0b877-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b877-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b877-145">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b877-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b877-146">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0b877-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b877-147">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0b877-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

