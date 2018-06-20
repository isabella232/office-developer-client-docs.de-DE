---
title: Kanonische PidTagExpiryUnits-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794348"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="b84fb-103">Kanonische PidTagExpiryUnits-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b84fb-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="b84fb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b84fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b84fb-105">Beschreibt die Zeiteinheit, wenn die Eigenschaft **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b84fb-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b84fb-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b84fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b84fb-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="b84fb-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="b84fb-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b84fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b84fb-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="b84fb-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="b84fb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b84fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="b84fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b84fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b84fb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b84fb-112">Area:</span></span>  <br/> |<span data-ttu-id="b84fb-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="b84fb-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b84fb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b84fb-114">Remarks</span></span>

<span data-ttu-id="b84fb-115">Diese Eigenschaft, wenn festgelegt ist, muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="b84fb-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b84fb-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="b84fb-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="b84fb-117">Beschreibung (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="b84fb-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="b84fb-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84fb-118">0x00000000</span></span>  <br/> |<span data-ttu-id="b84fb-119">Minuten, beispielsweise 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="b84fb-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="b84fb-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b84fb-120">0x00000001</span></span>  <br/> |<span data-ttu-id="b84fb-121">Stunden, beispielsweise 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="b84fb-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b84fb-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b84fb-122">0x00000002</span></span>  <br/> |<span data-ttu-id="b84fb-123">Am Tag, beispielsweise 24 x 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="b84fb-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b84fb-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="b84fb-124">0x00000003</span></span>  <br/> |<span data-ttu-id="b84fb-125">Woche, beispielsweise 7x24x60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="b84fb-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b84fb-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b84fb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b84fb-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b84fb-127">Protocol specifications</span></span>

<span data-ttu-id="b84fb-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b84fb-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b84fb-129">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b84fb-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b84fb-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b84fb-130">Header files</span></span>

<span data-ttu-id="b84fb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b84fb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b84fb-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b84fb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b84fb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b84fb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b84fb-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b84fb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b84fb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b84fb-135">See also</span></span>



[<span data-ttu-id="b84fb-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b84fb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b84fb-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b84fb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b84fb-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b84fb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b84fb-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b84fb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

