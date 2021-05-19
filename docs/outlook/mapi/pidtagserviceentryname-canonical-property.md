---
title: PidTagServiceEntryName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432471"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="6750b-103">PidTagServiceEntryName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6750b-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="6750b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6750b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6750b-105">Enthält den Namen der Einstiegspunktfunktion für die Konfiguration eines Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="6750b-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6750b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6750b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6750b-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="6750b-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="6750b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6750b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6750b-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="6750b-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="6750b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6750b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6750b-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6750b-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6750b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6750b-112">Area:</span></span>  <br/> |<span data-ttu-id="6750b-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="6750b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6750b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6750b-114">Remarks</span></span>

<span data-ttu-id="6750b-115">Es wird empfohlen, dass Die Implementierungen des Nachrichtendiensts einen Einstiegspunkt für den Nachrichtendienst bereitstellen, der Einstiegspunkt ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6750b-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="6750b-116">Der Einstiegspunkt sollte jedoch nur angegeben werden, wenn die zugehörigen Konfigurationseigenschaften vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6750b-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="6750b-117">Wenn diese Eigenschaften nicht vorhanden sind, geht MAPI davon aus, dass kein Einstiegspunkt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6750b-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="6750b-118">Die Dynamic-Link Library (DLL), in der die Einstiegspunktfunktion angezeigt wird, wird durch die **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) -Eigenschaft benannt.</span><span class="sxs-lookup"><span data-stu-id="6750b-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6750b-119">Weitere Informationen zu Einstiegspunkten für den Nachrichtendienst finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="6750b-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6750b-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6750b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6750b-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6750b-121">Header files</span></span>

<span data-ttu-id="6750b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6750b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6750b-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6750b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6750b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6750b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6750b-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6750b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6750b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6750b-126">See also</span></span>



[<span data-ttu-id="6750b-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6750b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6750b-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6750b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6750b-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6750b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6750b-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6750b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

