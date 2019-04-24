---
title: Kanonische Pidtagrowtype (-Eigenschaft
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
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359514"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="76feb-103">Kanonische Pidtagrowtype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="76feb-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="76feb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76feb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76feb-105">Enthält einen Wert, der den Typ einer Zeile in einer Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="76feb-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76feb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="76feb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76feb-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="76feb-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="76feb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="76feb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76feb-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="76feb-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="76feb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="76feb-110">Data type:</span></span>  <br/> |<span data-ttu-id="76feb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76feb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76feb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="76feb-112">Area:</span></span>  <br/> |<span data-ttu-id="76feb-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="76feb-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76feb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76feb-114">Remarks</span></span>

<span data-ttu-id="76feb-115">Diese Eigenschaft wird nur für Inhaltstabellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76feb-115">This property appears only on contents tables.</span></span> <span data-ttu-id="76feb-116">Eine Kategorie ist nur vorhanden, wenn Sie über Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="76feb-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="76feb-117">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="76feb-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="76feb-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="76feb-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="76feb-119">Stellt tatsächliche Daten anstelle einer Kategorieleiste dar.</span><span class="sxs-lookup"><span data-stu-id="76feb-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="76feb-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="76feb-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="76feb-121">Wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="76feb-121">Not currently used.</span></span>
    
<span data-ttu-id="76feb-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="76feb-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="76feb-123">Die Kategorie wurde erweitert; in der Benutzeroberfläche wird dies in der Regel mit dem Minuszeichen (-) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76feb-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="76feb-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="76feb-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="76feb-125">Die Kategorie ist reduziert; in der Benutzeroberfläche wird dies in der Regel mit dem Pluszeichen (+) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76feb-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="76feb-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76feb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76feb-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="76feb-127">Protocol specifications</span></span>

<span data-ttu-id="76feb-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76feb-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76feb-129">Enthält zulässige Vorgänge für die Haupttabellen Objekte.</span><span class="sxs-lookup"><span data-stu-id="76feb-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76feb-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="76feb-130">Header files</span></span>

<span data-ttu-id="76feb-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="76feb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="76feb-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="76feb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="76feb-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="76feb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="76feb-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="76feb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76feb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76feb-135">See also</span></span>



[<span data-ttu-id="76feb-136">Kanonische Pidtagrowid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="76feb-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="76feb-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76feb-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76feb-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76feb-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76feb-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="76feb-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76feb-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="76feb-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

