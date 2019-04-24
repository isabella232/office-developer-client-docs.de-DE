---
title: Kanonische Pidtagnull (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329267"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="5ba03-103">Kanonische Pidtagnull (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5ba03-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="5ba03-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ba03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ba03-105">Stellt einen NULL-Wert oder eine Einstellung einer Eigenschaft dar oder reserviert Array Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="5ba03-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ba03-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5ba03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ba03-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="5ba03-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="5ba03-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5ba03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ba03-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="5ba03-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="5ba03-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5ba03-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ba03-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="5ba03-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="5ba03-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5ba03-112">Area:</span></span>  <br/> |<span data-ttu-id="5ba03-113">Standard</span><span class="sxs-lookup"><span data-stu-id="5ba03-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ba03-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ba03-114">Remarks</span></span>

<span data-ttu-id="5ba03-115">Diese Eigenschaft wird verwendet, um Platz in Arrays von [SPropValue](spropvalue.md) -Strukturen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="5ba03-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="5ba03-116">Sie wird in einem Array von [SPropTagArray](sproptagarray.md) -Strukturen verwendet, um die Methode aufzufordern, Platz im zurückgegebenen Array von **SPropValue** -Strukturen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="5ba03-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="5ba03-117">Dadurch können berechnete Eigenschaften auf kostengünstige Weise ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="5ba03-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="5ba03-118">Weitere Informationen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5ba03-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ba03-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5ba03-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ba03-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5ba03-120">Protocol specifications</span></span>

<span data-ttu-id="5ba03-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ba03-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ba03-122">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5ba03-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ba03-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5ba03-123">Header files</span></span>

<span data-ttu-id="5ba03-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5ba03-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ba03-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5ba03-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ba03-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5ba03-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5ba03-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5ba03-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ba03-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ba03-128">See also</span></span>



[<span data-ttu-id="5ba03-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ba03-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ba03-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ba03-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ba03-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5ba03-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ba03-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5ba03-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

