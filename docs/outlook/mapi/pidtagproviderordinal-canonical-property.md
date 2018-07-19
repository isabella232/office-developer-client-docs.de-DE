---
title: PidTagProviderOrdinal (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794843"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="5b83e-103">PidTagProviderOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b83e-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="5b83e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b83e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b83e-105">Den nullbasierten Index des Dienstanbieters Position in der Provider-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="5b83e-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b83e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b83e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b83e-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="5b83e-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="5b83e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5b83e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b83e-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="5b83e-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="5b83e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b83e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b83e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5b83e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5b83e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b83e-112">Area:</span></span>  <br/> |<span data-ttu-id="5b83e-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="5b83e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b83e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b83e-114">Remarks</span></span>

<span data-ttu-id="5b83e-115">Diese Eigenschaft wird von MAPI berechnet.</span><span class="sxs-lookup"><span data-stu-id="5b83e-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="5b83e-116">Aufrufen der [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) -Methode die Provider-Tabelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5b83e-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="5b83e-117">Sortieren der Provider-Tabelle auf diese Eigenschaft, um die Reihenfolge der Transport anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5b83e-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5b83e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b83e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5b83e-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5b83e-119">Header files</span></span>

<span data-ttu-id="5b83e-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b83e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b83e-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b83e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b83e-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b83e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5b83e-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5b83e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b83e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b83e-124">See also</span></span>



[<span data-ttu-id="5b83e-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b83e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b83e-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b83e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b83e-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b83e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b83e-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b83e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

