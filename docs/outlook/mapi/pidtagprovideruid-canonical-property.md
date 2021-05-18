---
title: PidTagProviderUid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422775"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="c5d36-103">PidTagProviderUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c5d36-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="c5d36-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5d36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5d36-105">Enthält eine **MAPIUID-Struktur** des Dienstanbieters, der eine Nachricht behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="c5d36-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5d36-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c5d36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5d36-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="c5d36-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="c5d36-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c5d36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5d36-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="c5d36-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="c5d36-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c5d36-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5d36-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c5d36-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c5d36-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c5d36-112">Area:</span></span>  <br/> |<span data-ttu-id="c5d36-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="c5d36-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5d36-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5d36-114">Remarks</span></span>

<span data-ttu-id="c5d36-115">Diese Eigenschaft wird von allen Dienstanbietern berechnet.</span><span class="sxs-lookup"><span data-stu-id="c5d36-115">This property is computed by all service providers.</span></span> <span data-ttu-id="c5d36-116">Sie enthält eine [MAPIUID-Struktur,](mapiuid.md) die dem Anbieter zugeordnet ist und in der Regel hart codiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5d36-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="c5d36-117">Sie wird in der Regel von einer Clientanwendung verwendet, die nur an den Adressbuchcontainern interessiert ist, die von einem bestimmten Anbieter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5d36-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="c5d36-118">Diese Eigenschaft wird nur als Spalteneintrag in der Anbietertabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5d36-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5d36-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5d36-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c5d36-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c5d36-120">Header files</span></span>

<span data-ttu-id="c5d36-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5d36-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5d36-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c5d36-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5d36-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5d36-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c5d36-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c5d36-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5d36-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d36-125">See also</span></span>



[<span data-ttu-id="c5d36-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5d36-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5d36-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c5d36-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5d36-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c5d36-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5d36-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c5d36-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

