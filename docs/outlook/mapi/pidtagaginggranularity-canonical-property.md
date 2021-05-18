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
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325585"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="5b03f-103">PidTagAgingGranularity (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b03f-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="5b03f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b03f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b03f-105">Stellt die Zeiteinheit dar, die zum Bestimmen der Dauer verwendet wird, die ein Element in einem Ordner verbleibt, bevor das Element archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="5b03f-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b03f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b03f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b03f-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5b03f-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="5b03f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5b03f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b03f-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="5b03f-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="5b03f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b03f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b03f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5b03f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5b03f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b03f-112">Area:</span></span>  <br/> |<span data-ttu-id="5b03f-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="5b03f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b03f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b03f-114">Remarks</span></span>

<span data-ttu-id="5b03f-115">Die möglichen Werte **für PR_AGING_GRANULARITY** können einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="5b03f-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="5b03f-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b03f-116">**Name**</span></span>|<span data-ttu-id="5b03f-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5b03f-117">**Value**</span></span>|<span data-ttu-id="5b03f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b03f-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b03f-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="5b03f-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="5b03f-120">0</span><span class="sxs-lookup"><span data-stu-id="5b03f-120">0</span></span>  <br/> |<span data-ttu-id="5b03f-121">**PR_AGING_PERIOD** wird in der Anzahl der Monate definiert.</span><span class="sxs-lookup"><span data-stu-id="5b03f-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="5b03f-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="5b03f-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="5b03f-123">1</span><span class="sxs-lookup"><span data-stu-id="5b03f-123">1</span></span>  <br/> |<span data-ttu-id="5b03f-124">**PR_AGING_PERIOD** wird in der Anzahl der Wochen definiert.</span><span class="sxs-lookup"><span data-stu-id="5b03f-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="5b03f-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="5b03f-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="5b03f-126">2</span><span class="sxs-lookup"><span data-stu-id="5b03f-126">2</span></span>  <br/> |<span data-ttu-id="5b03f-127">**PR_AGING_PERIOD** wird in der Anzahl der Tage definiert.</span><span class="sxs-lookup"><span data-stu-id="5b03f-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="5b03f-128">Die Dauer, die ein Element in einem Ordner verbleibt, bevor das Element archiviert [wird,](pidtagagingperiod-canonical-property.md) wird durch zwei Eigenschaften bestimmt: PR_AGING_PERIOD **und PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="5b03f-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="5b03f-129">**PR_AGING_PERIOD** gibt die Anzahl der Zeiteinheiten an, die das Element im Ordner verbleibt, bevor es archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="5b03f-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5b03f-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b03f-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b03f-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5b03f-131">Protocol specifications</span></span>

<span data-ttu-id="5b03f-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b03f-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b03f-133">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b03f-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b03f-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b03f-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b03f-135">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b03f-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="5b03f-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b03f-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b03f-137">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5b03f-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b03f-138">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5b03f-138">Header files</span></span>

<span data-ttu-id="5b03f-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b03f-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b03f-140">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b03f-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b03f-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b03f-141">Mapitags.h</span></span>
  
> <span data-ttu-id="5b03f-142">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5b03f-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b03f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b03f-143">See also</span></span>



[<span data-ttu-id="5b03f-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b03f-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b03f-145">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5b03f-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b03f-146">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b03f-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b03f-147">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b03f-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

