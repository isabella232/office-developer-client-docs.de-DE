---
title: PidTagNull (kanonische Eigenschaft)
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
ms.openlocfilehash: 55db507055692c9e929b0125abf719d8c03ac967
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794662"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="686fa-103">PidTagNull (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="686fa-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="686fa-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="686fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="686fa-105">Stellt einen null-Wert oder die Einstellung einer Eigenschaft oder Array-Speicherplatz reserviert.</span><span class="sxs-lookup"><span data-stu-id="686fa-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="686fa-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="686fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="686fa-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="686fa-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="686fa-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="686fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="686fa-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="686fa-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="686fa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="686fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="686fa-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="686fa-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="686fa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="686fa-112">Area:</span></span>  <br/> |<span data-ttu-id="686fa-113">Common</span><span class="sxs-lookup"><span data-stu-id="686fa-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="686fa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="686fa-114">Remarks</span></span>

<span data-ttu-id="686fa-115">Diese Eigenschaft wird verwendet, um Speicherplatz in Arrays von [SPropValue](spropvalue.md) Strukturen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="686fa-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="686fa-116">Es wird in ein Array von [SPropTagArray](sproptagarray.md) Strukturen verwendet, anzuweisen, die Methode, um Speicherplatz im zurückgegebenen Array der **SPropValue** Strukturen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="686fa-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="686fa-117">Dies ermöglicht berechnete Eigenschaften in eine kostengünstige Möglichkeit gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="686fa-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="686fa-118">Weitere Informationen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="686fa-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="686fa-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="686fa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="686fa-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="686fa-120">Protocol specifications</span></span>

<span data-ttu-id="686fa-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="686fa-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="686fa-122">Gibt die Eigenschaften und Operationen, die auf Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="686fa-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="686fa-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="686fa-123">Header files</span></span>

<span data-ttu-id="686fa-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="686fa-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="686fa-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="686fa-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="686fa-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="686fa-126">Mapitags.h</span></span>
  
> <span data-ttu-id="686fa-127">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="686fa-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="686fa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="686fa-128">See also</span></span>



[<span data-ttu-id="686fa-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="686fa-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="686fa-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="686fa-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="686fa-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="686fa-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="686fa-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="686fa-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

