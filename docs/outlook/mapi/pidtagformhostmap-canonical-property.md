---
title: PidTagFormHostMap (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433766"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="fe617-103">PidTagFormHostMap (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe617-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="fe617-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe617-105">Enthält eine Hostzuordnung verfügbarer Formulare.</span><span class="sxs-lookup"><span data-stu-id="fe617-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe617-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fe617-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe617-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="fe617-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="fe617-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fe617-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe617-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="fe617-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="fe617-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fe617-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe617-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="fe617-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="fe617-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fe617-112">Area:</span></span>  <br/> |<span data-ttu-id="fe617-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="fe617-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe617-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe617-114">Remarks</span></span>

<span data-ttu-id="fe617-115">Eine Clientanwendung sollte diese Eigenschaft zusammen mit der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft aktualisieren, wenn die zugrunde liegende Struktur in der **IMAPIFormProp-Schnittstelle geändert** wird.</span><span class="sxs-lookup"><span data-stu-id="fe617-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fe617-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe617-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe617-117">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="fe617-117">Header files</span></span>

<span data-ttu-id="fe617-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe617-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe617-119">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fe617-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe617-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe617-120">Mapitags.h</span></span>
  
> <span data-ttu-id="fe617-121">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fe617-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe617-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe617-122">See also</span></span>



[<span data-ttu-id="fe617-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe617-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe617-124">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="fe617-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe617-125">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fe617-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe617-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fe617-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

