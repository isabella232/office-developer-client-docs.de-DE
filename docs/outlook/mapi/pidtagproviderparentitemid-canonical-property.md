---
title: Kanonische PidTagProviderParentItemId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794833"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="0f67f-103">Kanonische PidTagProviderParentItemId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f67f-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="0f67f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f67f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f67f-105">Gibt einen Bezeichner für das übergeordnete Objekt eines Ordners oder eines Elements in einem Speicher an.</span><span class="sxs-lookup"><span data-stu-id="0f67f-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f67f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f67f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f67f-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="0f67f-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="0f67f-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="0f67f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f67f-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="0f67f-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="0f67f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f67f-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f67f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f67f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f67f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f67f-112">Area:</span></span>  <br/> |<span data-ttu-id="0f67f-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="0f67f-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f67f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f67f-114">Remarks</span></span>

<span data-ttu-id="0f67f-115">Anbieter können, geben Sie einen Wert für diese Eigenschaft für ein übergeordnetes Element eines Ordners oder ein Element, jedoch sollten behalten Sie den Wert zwischen Sitzungen identisch.</span><span class="sxs-lookup"><span data-stu-id="0f67f-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="0f67f-116">Anbieter mit dieser Eigenschaft können Sie um Suchergebnisse aus einer Suchmaschine zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0f67f-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f67f-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f67f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0f67f-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0f67f-118">Header files</span></span>

<span data-ttu-id="0f67f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f67f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f67f-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0f67f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f67f-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f67f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0f67f-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0f67f-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f67f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f67f-123">See also</span></span>



[<span data-ttu-id="0f67f-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f67f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f67f-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f67f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f67f-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f67f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f67f-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f67f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

