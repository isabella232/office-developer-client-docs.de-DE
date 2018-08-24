---
title: PidTagProviderItemId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572837"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="2a1f6-103">PidTagProviderItemId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2a1f6-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="2a1f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a1f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a1f6-105">Gibt einen Bezeichner für einen Ordner oder ein Element in einem Speicher an.</span><span class="sxs-lookup"><span data-stu-id="2a1f6-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a1f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2a1f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a1f6-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="2a1f6-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="2a1f6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2a1f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a1f6-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="2a1f6-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="2a1f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2a1f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a1f6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a1f6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a1f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2a1f6-112">Area:</span></span>  <br/> |<span data-ttu-id="2a1f6-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="2a1f6-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a1f6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a1f6-114">Remarks</span></span>

<span data-ttu-id="2a1f6-115">Anbieter können Geben Sie einen Wert für diese Eigenschaft für einen Ordner oder ein Element, jedoch sollten behalten Sie den Wert zwischen Sitzungen identisch.</span><span class="sxs-lookup"><span data-stu-id="2a1f6-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="2a1f6-116">Anbieter mit dieser Eigenschaft können Sie um Suchergebnisse aus einer Suchmaschine zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2a1f6-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a1f6-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a1f6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2a1f6-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2a1f6-118">Header files</span></span>

<span data-ttu-id="2a1f6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a1f6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a1f6-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2a1f6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a1f6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a1f6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2a1f6-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2a1f6-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a1f6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a1f6-123">See also</span></span>



[<span data-ttu-id="2a1f6-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a1f6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a1f6-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a1f6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a1f6-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2a1f6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a1f6-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2a1f6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

