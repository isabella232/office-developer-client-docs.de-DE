---
title: Kanonische Pidtagexpiryunits (-Eigenschaft
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
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316408"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="254c6-103">Kanonische Pidtagexpiryunits (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="254c6-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="254c6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="254c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="254c6-105">Beschreibt die Zeiteinheit, in der die **PR_EXPIRY_NUMBER** ([pidtagexpirynumber (](pidtagexpirynumber-canonical-property.md))-Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="254c6-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="254c6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="254c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="254c6-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="254c6-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="254c6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="254c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="254c6-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="254c6-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="254c6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="254c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="254c6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="254c6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="254c6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="254c6-112">Area:</span></span>  <br/> |<span data-ttu-id="254c6-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="254c6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="254c6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="254c6-114">Remarks</span></span>

<span data-ttu-id="254c6-115">Bei dieser Eigenschaft muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="254c6-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="254c6-116">Pidtagexpiryunits (</span><span class="sxs-lookup"><span data-stu-id="254c6-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="254c6-117">Beschreibung (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="254c6-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="254c6-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="254c6-118">0x00000000</span></span>  <br/> |<span data-ttu-id="254c6-119">Minuten, zum Beispiel 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="254c6-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="254c6-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="254c6-120">0x00000001</span></span>  <br/> |<span data-ttu-id="254c6-121">Stunden, beispielsweise 60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="254c6-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="254c6-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="254c6-122">0x00000002</span></span>  <br/> |<span data-ttu-id="254c6-123">Tag, beispielsweise 24x60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="254c6-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="254c6-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="254c6-124">0x00000003</span></span>  <br/> |<span data-ttu-id="254c6-125">Woche, beispielsweise 7x24x60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="254c6-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="254c6-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="254c6-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="254c6-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="254c6-127">Protocol specifications</span></span>

<span data-ttu-id="254c6-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="254c6-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="254c6-129">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="254c6-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="254c6-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="254c6-130">Header files</span></span>

<span data-ttu-id="254c6-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="254c6-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="254c6-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="254c6-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="254c6-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="254c6-133">Mapitags.h</span></span>
  
> <span data-ttu-id="254c6-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="254c6-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="254c6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="254c6-135">See also</span></span>



[<span data-ttu-id="254c6-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="254c6-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="254c6-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="254c6-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="254c6-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="254c6-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="254c6-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="254c6-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

