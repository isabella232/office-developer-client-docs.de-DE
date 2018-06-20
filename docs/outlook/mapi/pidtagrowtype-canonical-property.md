---
title: Kanonische PidTagRowType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795001"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="e7e56-103">Kanonische PidTagRowType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7e56-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="e7e56-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7e56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7e56-105">Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="e7e56-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7e56-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e7e56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7e56-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="e7e56-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="e7e56-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e7e56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7e56-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="e7e56-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="e7e56-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e7e56-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7e56-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e7e56-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e7e56-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e7e56-112">Area:</span></span>  <br/> |<span data-ttu-id="e7e56-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="e7e56-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7e56-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7e56-114">Remarks</span></span>

<span data-ttu-id="e7e56-115">Diese Eigenschaft wird nur für Tabellen Inhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7e56-115">This property appears only on contents tables.</span></span> <span data-ttu-id="e7e56-116">Eine Kategorie ist nur vorhanden, wenn er Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="e7e56-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="e7e56-117">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e7e56-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e7e56-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="e7e56-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="e7e56-119">Tatsächliche Daten darstellt, anstatt eine Kategoriezeile.</span><span class="sxs-lookup"><span data-stu-id="e7e56-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="e7e56-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e7e56-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="e7e56-121">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7e56-121">Not currently used.</span></span>
    
<span data-ttu-id="e7e56-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e7e56-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="e7e56-123">Die Kategorie erweitert ist. die Benutzeroberfläche wird in der Regel dies mit dem Minuszeichen (-) neben dem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7e56-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="e7e56-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e7e56-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="e7e56-125">Die Kategorie ausgeblendet ist; die Benutzeroberfläche wird dies in der Regel durch das Pluszeichen (+) neben dem.</span><span class="sxs-lookup"><span data-stu-id="e7e56-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e7e56-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7e56-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7e56-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e7e56-127">Protocol specifications</span></span>

<span data-ttu-id="e7e56-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7e56-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7e56-129">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="e7e56-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7e56-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e7e56-130">Header files</span></span>

<span data-ttu-id="e7e56-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7e56-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7e56-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e7e56-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7e56-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7e56-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e7e56-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e7e56-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7e56-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e56-135">See also</span></span>



[<span data-ttu-id="e7e56-136">Kanonische PidTagRowid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7e56-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="e7e56-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7e56-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7e56-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7e56-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7e56-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e7e56-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7e56-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e7e56-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

