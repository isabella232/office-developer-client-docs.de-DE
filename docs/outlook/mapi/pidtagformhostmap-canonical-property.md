---
title: Kanonische Pidtagformhostmap (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316226"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="e5cae-103">Kanonische Pidtagformhostmap (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5cae-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="e5cae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5cae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5cae-105">Enthält eine Hostkarte der verfügbaren Formulare.</span><span class="sxs-lookup"><span data-stu-id="e5cae-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5cae-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e5cae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5cae-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="e5cae-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="e5cae-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e5cae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5cae-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="e5cae-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="e5cae-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e5cae-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5cae-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="e5cae-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e5cae-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e5cae-112">Area:</span></span>  <br/> |<span data-ttu-id="e5cae-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="e5cae-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5cae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5cae-114">Remarks</span></span>

<span data-ttu-id="e5cae-115">Eine Clientanwendung sollte diese Eigenschaft zusammen mit der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft aktualisieren, wenn die zugrunde liegende Struktur in der **IMAPIFormProp** -Schnittstelle geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e5cae-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e5cae-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e5cae-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e5cae-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e5cae-117">Header files</span></span>

<span data-ttu-id="e5cae-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e5cae-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5cae-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e5cae-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5cae-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e5cae-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e5cae-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e5cae-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5cae-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5cae-122">See also</span></span>



[<span data-ttu-id="e5cae-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5cae-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5cae-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5cae-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5cae-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e5cae-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5cae-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e5cae-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

