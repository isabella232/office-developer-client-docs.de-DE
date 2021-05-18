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
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421592"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="6f614-103">PidTagProviderDisplay (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6f614-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="6f614-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f614-105">Enthält den vom Hersteller definierten Anzeigenamen für einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="6f614-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f614-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6f614-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f614-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="6f614-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="6f614-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6f614-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f614-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="6f614-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="6f614-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6f614-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f614-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f614-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f614-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6f614-112">Area:</span></span>  <br/> |<span data-ttu-id="6f614-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="6f614-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f614-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f614-114">Remarks</span></span>

<span data-ttu-id="6f614-115">Diese Eigenschaften und **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) werden nur für Profilabschnitte definiert, die zu Dienstanbietern gehören.</span><span class="sxs-lookup"><span data-stu-id="6f614-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="6f614-116">Sie müssen in MAPISVC.INF vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6f614-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f614-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6f614-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6f614-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6f614-118">Header files</span></span>

<span data-ttu-id="6f614-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f614-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f614-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6f614-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f614-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f614-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6f614-122">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6f614-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f614-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f614-123">See also</span></span>



[<span data-ttu-id="6f614-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6f614-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f614-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6f614-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f614-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6f614-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f614-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6f614-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

