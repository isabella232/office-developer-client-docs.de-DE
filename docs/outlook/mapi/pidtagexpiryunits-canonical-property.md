---
title: PidTagExpiryUnits (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316408"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="15b58-103">PidTagExpiryUnits (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="15b58-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="15b58-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15b58-105">Beschreibt die Zeiteinheit, in der **die PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) -Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="15b58-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15b58-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="15b58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15b58-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="15b58-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="15b58-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="15b58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15b58-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="15b58-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="15b58-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="15b58-110">Data type:</span></span>  <br/> |<span data-ttu-id="15b58-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15b58-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15b58-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="15b58-112">Area:</span></span>  <br/> |<span data-ttu-id="15b58-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="15b58-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15b58-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15b58-114">Remarks</span></span>

<span data-ttu-id="15b58-115">Diese Eigenschaft muss, falls festgelegt, einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="15b58-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15b58-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="15b58-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="15b58-117">Beschreibung (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="15b58-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="15b58-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15b58-118">0x00000000</span></span>  <br/> |<span data-ttu-id="15b58-119">Minuten, z. B. 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="15b58-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="15b58-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b58-120">0x00000001</span></span>  <br/> |<span data-ttu-id="15b58-121">Stunden, z. B. 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="15b58-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="15b58-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="15b58-122">0x00000002</span></span>  <br/> |<span data-ttu-id="15b58-123">Tag, z. B. 24 x 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="15b58-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="15b58-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="15b58-124">0x00000003</span></span>  <br/> |<span data-ttu-id="15b58-125">Woche, z. B. 7x24x60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="15b58-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="15b58-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="15b58-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15b58-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="15b58-127">Protocol specifications</span></span>

<span data-ttu-id="15b58-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15b58-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15b58-129">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="15b58-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15b58-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="15b58-130">Header files</span></span>

<span data-ttu-id="15b58-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15b58-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="15b58-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="15b58-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="15b58-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15b58-133">Mapitags.h</span></span>
  
> <span data-ttu-id="15b58-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="15b58-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15b58-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15b58-135">See also</span></span>



[<span data-ttu-id="15b58-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15b58-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15b58-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="15b58-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15b58-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="15b58-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15b58-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="15b58-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

