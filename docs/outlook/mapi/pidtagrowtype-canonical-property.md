---
title: PidTagRowType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383065"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="a13e7-103">PidTagRowType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a13e7-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="a13e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a13e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a13e7-105">Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="a13e7-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a13e7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a13e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a13e7-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="a13e7-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="a13e7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a13e7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a13e7-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="a13e7-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="a13e7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a13e7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a13e7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a13e7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a13e7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a13e7-112">Area:</span></span>  <br/> |<span data-ttu-id="a13e7-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="a13e7-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a13e7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a13e7-114">Remarks</span></span>

<span data-ttu-id="a13e7-115">Diese Eigenschaft wird nur für Tabellen Inhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a13e7-115">This property appears only on contents tables.</span></span> <span data-ttu-id="a13e7-116">Eine Kategorie ist nur vorhanden, wenn er Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="a13e7-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="a13e7-117">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="a13e7-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="a13e7-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="a13e7-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="a13e7-119">Tatsächliche Daten darstellt, anstatt eine Kategoriezeile.</span><span class="sxs-lookup"><span data-stu-id="a13e7-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="a13e7-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="a13e7-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="a13e7-121">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a13e7-121">Not currently used.</span></span>
    
<span data-ttu-id="a13e7-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="a13e7-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="a13e7-123">Die Kategorie erweitert ist. die Benutzeroberfläche wird in der Regel dies mit dem Minuszeichen (-) neben dem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a13e7-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="a13e7-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="a13e7-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="a13e7-125">Die Kategorie ausgeblendet ist; die Benutzeroberfläche wird dies in der Regel durch das Pluszeichen (+) neben dem.</span><span class="sxs-lookup"><span data-stu-id="a13e7-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a13e7-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a13e7-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a13e7-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a13e7-127">Protocol specifications</span></span>

<span data-ttu-id="a13e7-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a13e7-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a13e7-129">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="a13e7-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a13e7-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a13e7-130">Header files</span></span>

<span data-ttu-id="a13e7-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a13e7-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a13e7-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a13e7-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a13e7-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a13e7-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a13e7-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a13e7-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a13e7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a13e7-135">See also</span></span>



[<span data-ttu-id="a13e7-136">PidTagRowid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a13e7-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="a13e7-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a13e7-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a13e7-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a13e7-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a13e7-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a13e7-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a13e7-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a13e7-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

