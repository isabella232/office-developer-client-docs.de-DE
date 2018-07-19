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
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794416"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="d85e2-103">PidTagFormHostMap (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d85e2-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="d85e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d85e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d85e2-105">Enthält eine Zuordnung Host der verfügbaren Formulare.</span><span class="sxs-lookup"><span data-stu-id="d85e2-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d85e2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d85e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d85e2-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="d85e2-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="d85e2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="d85e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d85e2-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="d85e2-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="d85e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d85e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="d85e2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d85e2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d85e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d85e2-112">Area:</span></span>  <br/> |<span data-ttu-id="d85e2-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="d85e2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d85e2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d85e2-114">Remarks</span></span>

<span data-ttu-id="d85e2-115">Eine Clientanwendung sollten diese Eigenschaft zusammen mit der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aktualisieren, beim Ändern die Struktur der zugrunde liegenden in der **IMAPIFormProp** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d85e2-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d85e2-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d85e2-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d85e2-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d85e2-117">Header files</span></span>

<span data-ttu-id="d85e2-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d85e2-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d85e2-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d85e2-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d85e2-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d85e2-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d85e2-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d85e2-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d85e2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d85e2-122">See also</span></span>



[<span data-ttu-id="d85e2-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d85e2-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d85e2-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d85e2-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d85e2-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d85e2-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d85e2-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d85e2-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

