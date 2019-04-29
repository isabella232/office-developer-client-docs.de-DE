---
title: Kanonische Pidtagproviderparentitemid (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433416"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="cd150-103">Kanonische Pidtagproviderparentitemid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd150-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="cd150-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd150-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd150-105">Gibt einen Bezeichner für das übergeordnete Element eines Ordners oder eines Elements in einem Speicher an.</span><span class="sxs-lookup"><span data-stu-id="cd150-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd150-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cd150-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd150-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="cd150-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="cd150-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cd150-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd150-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="cd150-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="cd150-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cd150-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd150-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cd150-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cd150-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cd150-112">Area:</span></span>  <br/> |<span data-ttu-id="cd150-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="cd150-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd150-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd150-114">Remarks</span></span>

<span data-ttu-id="cd150-115">Speicheranbieter können einen Wert für diese Eigenschaft für ein übergeordnetes Element eines Ordners oder eines Elements angeben, aber den Wert zwischen den Sitzungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cd150-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="cd150-116">Speicheranbieter verwenden Sie diese Eigenschaft, um Suchergebnisse zu identifizieren, die von einer Suchmaschine zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd150-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd150-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd150-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cd150-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cd150-118">Header files</span></span>

<span data-ttu-id="cd150-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cd150-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd150-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cd150-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd150-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cd150-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cd150-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cd150-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd150-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd150-123">See also</span></span>



[<span data-ttu-id="cd150-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd150-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd150-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd150-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd150-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cd150-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd150-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cd150-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

