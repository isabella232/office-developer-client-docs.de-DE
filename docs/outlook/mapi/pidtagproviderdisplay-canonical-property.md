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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286467"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="f2614-103">Kanonische Pidtagproviderdisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2614-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="f2614-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2614-105">Enthält den herstellerdefinierten Anzeigenamen für einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f2614-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2614-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f2614-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2614-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="f2614-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="f2614-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f2614-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2614-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="f2614-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="f2614-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f2614-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2614-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f2614-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f2614-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f2614-112">Area:</span></span>  <br/> |<span data-ttu-id="f2614-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="f2614-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2614-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2614-114">Remarks</span></span>

<span data-ttu-id="f2614-115">Diese Eigenschaften und **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)) werden nur in Profil Abschnitten definiert, die Dienstanbietern gehören.</span><span class="sxs-lookup"><span data-stu-id="f2614-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="f2614-116">Sie müssen in MAPISVC. INF vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f2614-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2614-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2614-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f2614-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f2614-118">Header files</span></span>

<span data-ttu-id="f2614-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f2614-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2614-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f2614-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2614-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f2614-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f2614-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f2614-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2614-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2614-123">See also</span></span>



[<span data-ttu-id="f2614-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2614-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2614-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2614-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2614-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f2614-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2614-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f2614-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

