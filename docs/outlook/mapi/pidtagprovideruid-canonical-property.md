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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794835"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="eb3b2-103">PidTagProviderUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="eb3b2-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="eb3b2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb3b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb3b2-105">Enthält eine **MAPIUID** Struktur des Dienstanbieters, der eine Nachricht behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb3b2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="eb3b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb3b2-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="eb3b2-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="eb3b2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="eb3b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb3b2-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="eb3b2-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="eb3b2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="eb3b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb3b2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eb3b2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eb3b2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="eb3b2-112">Area:</span></span>  <br/> |<span data-ttu-id="eb3b2-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="eb3b2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb3b2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb3b2-114">Remarks</span></span>

<span data-ttu-id="eb3b2-115">Diese Eigenschaft wird von allen Dienstanbietern berechnet.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-115">This property is computed by all service providers.</span></span> <span data-ttu-id="eb3b2-116">Sie enthält eine [MAPIUID](mapiuid.md) Struktur zugeordnet und in der Regel hartcodierte vom Anbieter.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="eb3b2-117">Es wird in der Regel von einer Clientanwendung verwendet, die nur Address Book Container von einem bestimmten Anbieter bereitgestellt wird, interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="eb3b2-118">Diese Eigenschaft wird nur als ein Eintrag in der Spalte in der Tabelle Anbieter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb3b2-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eb3b2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eb3b2-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="eb3b2-120">Header files</span></span>

<span data-ttu-id="eb3b2-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb3b2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb3b2-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb3b2-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb3b2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="eb3b2-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb3b2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb3b2-125">See also</span></span>



[<span data-ttu-id="eb3b2-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb3b2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb3b2-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb3b2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb3b2-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="eb3b2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb3b2-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="eb3b2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

