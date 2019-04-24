---
title: Kanonische Pidtagdepth (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360851"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="93f6f-103">Kanonische Pidtagdepth (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93f6f-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="93f6f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93f6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93f6f-105">Enthält eine ganze Zahl, die die relative Ebene der Einrückung oder Tiefe eines Objekts in einer Hierarchietabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="93f6f-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93f6f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93f6f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93f6f-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="93f6f-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="93f6f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="93f6f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93f6f-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="93f6f-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="93f6f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93f6f-110">Data type:</span></span>  <br/> |<span data-ttu-id="93f6f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93f6f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93f6f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93f6f-112">Area:</span></span>  <br/> |<span data-ttu-id="93f6f-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="93f6f-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93f6f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93f6f-114">Remarks</span></span>

<span data-ttu-id="93f6f-115">Diese Eigenschaft kann auch die Kategorisierungs Ebene einer Zeile in einer Inhaltstabelle oder die Hierarchietiefe in einer Hierarchietabelle angeben.</span><span class="sxs-lookup"><span data-stu-id="93f6f-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="93f6f-116">Die Tiefe ist nullbasiert, wobei Null die äußerste linke Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="93f6f-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="93f6f-117">In allen Fällen stellt der Eigenschaftswert einen relativen Wert anstelle eines absoluten Werts dar.</span><span class="sxs-lookup"><span data-stu-id="93f6f-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="93f6f-118">In der Hierarchietabelle ist der tiefen Wert beispielsweise relativ zu dem Container, aus dem die Hierarchietabelle abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="93f6f-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="93f6f-119">Die Tiefe stellt keine absolute Tiefe aus dem Stammcontainer dar.</span><span class="sxs-lookup"><span data-stu-id="93f6f-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93f6f-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93f6f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93f6f-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93f6f-121">Protocol specifications</span></span>

<span data-ttu-id="93f6f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f6f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f6f-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="93f6f-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93f6f-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f6f-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f6f-125">Enthält zulässige Vorgänge für die Haupttabellen Objekte.</span><span class="sxs-lookup"><span data-stu-id="93f6f-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="93f6f-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f6f-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f6f-127">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="93f6f-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93f6f-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="93f6f-128">Header files</span></span>

<span data-ttu-id="93f6f-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="93f6f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="93f6f-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="93f6f-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="93f6f-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="93f6f-131">Mapitags.h</span></span>
  
> <span data-ttu-id="93f6f-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="93f6f-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93f6f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93f6f-133">See also</span></span>



[<span data-ttu-id="93f6f-134">Kanonische Pidtagobjecttype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93f6f-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="93f6f-135">Kanonische Pidtagselectable (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93f6f-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="93f6f-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93f6f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93f6f-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93f6f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93f6f-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93f6f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93f6f-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93f6f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

