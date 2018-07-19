---
title: PidTagProviderDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1546ee1aa970be71d853dba59ce0fab7cc5a4dac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794830"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="da02a-103">PidTagProviderDisplay (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="da02a-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="da02a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da02a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da02a-105">Enthält den herstellerspezifischen Anzeigenamen für einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="da02a-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da02a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="da02a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da02a-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="da02a-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="da02a-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="da02a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da02a-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="da02a-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="da02a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="da02a-110">Data type:</span></span>  <br/> |<span data-ttu-id="da02a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da02a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="da02a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="da02a-112">Area:</span></span>  <br/> |<span data-ttu-id="da02a-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="da02a-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da02a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da02a-114">Remarks</span></span>

<span data-ttu-id="da02a-115">Diese Eigenschaften und **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) sind nur für Profil Abschnitten, Dienstanbieter angehören definiert.</span><span class="sxs-lookup"><span data-stu-id="da02a-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="da02a-116">Sie müssen in MAPISVC.INF vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="da02a-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="da02a-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="da02a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="da02a-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="da02a-118">Header files</span></span>

<span data-ttu-id="da02a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da02a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="da02a-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="da02a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="da02a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da02a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="da02a-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="da02a-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da02a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da02a-123">See also</span></span>



[<span data-ttu-id="da02a-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da02a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da02a-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da02a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da02a-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="da02a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da02a-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="da02a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

