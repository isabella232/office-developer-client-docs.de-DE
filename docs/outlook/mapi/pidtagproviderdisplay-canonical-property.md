---
title: Kanonische Pidtagproviderdisplay (-Eigenschaft
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
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="f6343-103">Kanonische Pidtagproviderdisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6343-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="f6343-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6343-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6343-105">Enthält den herstellerdefinierten Anzeigenamen für einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f6343-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6343-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f6343-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6343-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="f6343-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="f6343-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f6343-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6343-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="f6343-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="f6343-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f6343-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6343-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f6343-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f6343-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f6343-112">Area:</span></span>  <br/> |<span data-ttu-id="f6343-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="f6343-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6343-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6343-114">Remarks</span></span>

<span data-ttu-id="f6343-115">Diese Eigenschaften und **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)) werden nur in Profil Abschnitten definiert, die Dienstanbietern gehören.</span><span class="sxs-lookup"><span data-stu-id="f6343-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="f6343-116">Sie müssen in MAPISVC. INF vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f6343-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f6343-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6343-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f6343-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f6343-118">Header files</span></span>

<span data-ttu-id="f6343-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f6343-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6343-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f6343-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6343-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f6343-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f6343-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f6343-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6343-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6343-123">See also</span></span>



[<span data-ttu-id="f6343-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6343-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6343-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6343-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6343-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f6343-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6343-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f6343-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

