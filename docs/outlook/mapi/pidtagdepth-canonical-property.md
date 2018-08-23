---
title: PidTagDepth (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 100d59a0fd95fcad1976e82aebf6892227c08ec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564913"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="37fda-103">PidTagDepth (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37fda-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="37fda-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37fda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37fda-105">Enthält eine ganze Zahl, die den relativen Einzug oder Tiefe der ein Objekt in einer Hierarchietabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="37fda-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37fda-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="37fda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37fda-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="37fda-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="37fda-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="37fda-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37fda-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="37fda-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="37fda-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="37fda-110">Data type:</span></span>  <br/> |<span data-ttu-id="37fda-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37fda-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37fda-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="37fda-112">Area:</span></span>  <br/> |<span data-ttu-id="37fda-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="37fda-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37fda-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="37fda-114">Remarks</span></span>

<span data-ttu-id="37fda-115">Diese Eigenschaft kann auch die Kategorisierungsebene einer Zeile in einer Inhaltstabelle oder die Ordnerhierarchie-Tiefe in einer Hierarchietabelle angeben.</span><span class="sxs-lookup"><span data-stu-id="37fda-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="37fda-116">Die Tiefe ist nullbasiert, wobei 0 (null) die am weitesten links Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="37fda-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="37fda-117">In allen Fällen stellt Wert der Eigenschaft um einen relativen Wert statt einen absoluten Wert dar.</span><span class="sxs-lookup"><span data-stu-id="37fda-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="37fda-118">In der Hierarchietabelle befindet sich der Wert für die Tiefe beispielsweise relativ zu den Container, von dem die Hierarchietabelle abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="37fda-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="37fda-119">Die Tiefe stellt eine absolute Tiefe nicht aus dem Stammcontainer dar.</span><span class="sxs-lookup"><span data-stu-id="37fda-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="37fda-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37fda-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37fda-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="37fda-121">Protocol specifications</span></span>

<span data-ttu-id="37fda-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37fda-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37fda-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="37fda-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37fda-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37fda-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37fda-125">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="37fda-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="37fda-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37fda-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37fda-127">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="37fda-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37fda-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="37fda-128">Header files</span></span>

<span data-ttu-id="37fda-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37fda-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="37fda-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="37fda-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="37fda-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="37fda-131">Mapitags.h</span></span>
  
> <span data-ttu-id="37fda-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="37fda-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37fda-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fda-133">See also</span></span>



[<span data-ttu-id="37fda-134">PidTagObjectType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37fda-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="37fda-135">PidTagSelectable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37fda-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="37fda-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37fda-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37fda-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37fda-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37fda-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="37fda-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37fda-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="37fda-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

