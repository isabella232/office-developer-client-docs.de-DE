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
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412121"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="867e8-103">PidTagProviderItemId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="867e8-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="867e8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="867e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="867e8-105">Gibt einen Bezeichner für einen Ordner oder ein Element in einem Speicher an.</span><span class="sxs-lookup"><span data-stu-id="867e8-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="867e8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="867e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="867e8-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="867e8-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="867e8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="867e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="867e8-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="867e8-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="867e8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="867e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="867e8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="867e8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="867e8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="867e8-112">Area:</span></span>  <br/> |<span data-ttu-id="867e8-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="867e8-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="867e8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="867e8-114">Remarks</span></span>

<span data-ttu-id="867e8-115">Store können einen Wert für diese Eigenschaft für einen Ordner oder ein Element angeben, der Wert sollte jedoch zwischen Sitzungen gleich bleiben.</span><span class="sxs-lookup"><span data-stu-id="867e8-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="867e8-116">Store verwenden diese Eigenschaft, um suchergebnisse zu identifizieren, die von einer Suchmaschine zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="867e8-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="867e8-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="867e8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="867e8-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="867e8-118">Header files</span></span>

<span data-ttu-id="867e8-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="867e8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="867e8-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="867e8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="867e8-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="867e8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="867e8-122">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="867e8-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="867e8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="867e8-123">See also</span></span>



[<span data-ttu-id="867e8-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="867e8-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="867e8-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="867e8-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="867e8-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="867e8-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="867e8-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="867e8-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

