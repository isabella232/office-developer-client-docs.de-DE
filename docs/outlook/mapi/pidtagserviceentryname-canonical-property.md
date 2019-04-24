---
title: Kanonische Pidtagserviceentryname (-Eigenschaft
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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351072"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="bb093-103">Kanonische Pidtagserviceentryname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb093-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="bb093-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb093-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb093-105">Enthält den Namen der Einstiegspunktfunktion für die Konfiguration eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="bb093-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb093-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bb093-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb093-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="bb093-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="bb093-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bb093-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb093-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="bb093-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="bb093-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bb093-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb093-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bb093-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bb093-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bb093-112">Area:</span></span>  <br/> |<span data-ttu-id="bb093-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="bb093-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb093-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb093-114">Remarks</span></span>

<span data-ttu-id="bb093-115">Es wird empfohlen, dass der Nachrichtendienst Implementierer einen Einstiegspunkt für den Nachrichtendienst bereitstellt, der Einstiegspunkt ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bb093-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="bb093-116">Der Einstiegspunkt sollte jedoch nur angegeben werden, wenn die zugehörigen Konfigurationseigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bb093-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="bb093-117">Wenn diese Eigenschaften nicht vorhanden sind, geht MAPI davon aus, dass kein Einstiegspunkt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb093-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="bb093-118">Die Dynamic Link Library (DLL), in der die Einstiegspunktfunktion angezeigt wird, wird von der **PR_SERVICE_DLL_NAME** ([pidtagservicedllname (](pidtagservicedllname-canonical-property.md))-Eigenschaft benannt.</span><span class="sxs-lookup"><span data-stu-id="bb093-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bb093-119">Weitere Informationen zu Einstiegspunkten für den Nachrichtendienst finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb093-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb093-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb093-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bb093-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bb093-121">Header files</span></span>

<span data-ttu-id="bb093-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bb093-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb093-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bb093-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb093-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bb093-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bb093-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bb093-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb093-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb093-126">See also</span></span>



[<span data-ttu-id="bb093-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb093-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb093-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb093-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb093-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bb093-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb093-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bb093-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

