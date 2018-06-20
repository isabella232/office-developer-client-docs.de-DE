---
title: Kanonische PidTagServiceEntryName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795150"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="a8a45-103">Kanonische PidTagServiceEntryName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8a45-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="a8a45-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8a45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8a45-105">Enthält den Namen der Funktion Punkt Eintrag für die Konfiguration eines Diensts Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a8a45-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8a45-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a8a45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8a45-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="a8a45-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="a8a45-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a8a45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8a45-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="a8a45-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="a8a45-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a8a45-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8a45-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a8a45-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a8a45-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a8a45-112">Area:</span></span>  <br/> |<span data-ttu-id="a8a45-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="a8a45-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8a45-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8a45-114">Remarks</span></span>

<span data-ttu-id="a8a45-115">Es wird empfohlen, dass Message Service Implementierer einen Nachricht Service Einstiegspunkt bereitstellen, aber der Einstiegspunkt nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a8a45-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="a8a45-116">Der Einstiegspunkt sollten jedoch bereitgestellt werden, nur, wenn die zugehörigen Konfigurationseigenschaften vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a8a45-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="a8a45-117">Wenn diese Eigenschaften nicht vorhanden sind, wird MAPI davon ausgegangen, dass kein Einstiegspunkt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8a45-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="a8a45-118">Die Dynamic Link Library (DLL) in der die Funktion Eintrag angezeigt wird, heißt von der **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a8a45-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a8a45-119">Weitere Informationen zu Nachricht Service Einstiegspunkte finden Sie unter [Implementieren einer Service Provider Eintrag Point-Funktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="a8a45-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8a45-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8a45-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a8a45-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8a45-121">Header files</span></span>

<span data-ttu-id="a8a45-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8a45-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8a45-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a8a45-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8a45-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8a45-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a8a45-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8a45-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8a45-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8a45-126">See also</span></span>



[<span data-ttu-id="a8a45-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8a45-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8a45-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8a45-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8a45-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a8a45-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8a45-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a8a45-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

