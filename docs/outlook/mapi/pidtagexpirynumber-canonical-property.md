---
title: PidTagExpiryNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 087585e936f04f18ad15f390a083213e2285da83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794354"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="55bc5-103">PidTagExpiryNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="55bc5-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="55bc5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55bc5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55bc5-105">Definiert die Ablaufzeit senden in Verbindung mit der **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="55bc5-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55bc5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="55bc5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55bc5-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="55bc5-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="55bc5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="55bc5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55bc5-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="55bc5-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="55bc5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="55bc5-110">Data type:</span></span>  <br/> |<span data-ttu-id="55bc5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55bc5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55bc5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="55bc5-112">Area:</span></span>  <br/> |<span data-ttu-id="55bc5-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="55bc5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55bc5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55bc5-114">Remarks</span></span>

<span data-ttu-id="55bc5-115">Der Wert dieser Eigenschaft muss zwischen 0 und 999, der festgelegt werden, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="55bc5-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55bc5-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55bc5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55bc5-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="55bc5-117">Protocol specifications</span></span>

<span data-ttu-id="55bc5-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55bc5-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55bc5-119">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="55bc5-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55bc5-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="55bc5-120">Header files</span></span>

<span data-ttu-id="55bc5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55bc5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="55bc5-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="55bc5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="55bc5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55bc5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="55bc5-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="55bc5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55bc5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55bc5-125">See also</span></span>



[<span data-ttu-id="55bc5-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55bc5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55bc5-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55bc5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55bc5-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="55bc5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55bc5-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="55bc5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

