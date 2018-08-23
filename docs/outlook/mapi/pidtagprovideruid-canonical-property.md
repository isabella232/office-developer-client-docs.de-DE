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
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581055"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="1629d-103">PidTagProviderUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1629d-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="1629d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1629d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1629d-105">Enthält eine **MAPIUID** Struktur des Dienstanbieters, der eine Nachricht behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="1629d-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1629d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1629d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1629d-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="1629d-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="1629d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1629d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1629d-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="1629d-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="1629d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1629d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1629d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1629d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1629d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1629d-112">Area:</span></span>  <br/> |<span data-ttu-id="1629d-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="1629d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1629d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1629d-114">Remarks</span></span>

<span data-ttu-id="1629d-115">Diese Eigenschaft wird von allen Dienstanbietern berechnet.</span><span class="sxs-lookup"><span data-stu-id="1629d-115">This property is computed by all service providers.</span></span> <span data-ttu-id="1629d-116">Sie enthält eine [MAPIUID](mapiuid.md) Struktur zugeordnet und in der Regel hartcodierte vom Anbieter.</span><span class="sxs-lookup"><span data-stu-id="1629d-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="1629d-117">Es wird in der Regel von einer Clientanwendung verwendet, die nur Address Book Container von einem bestimmten Anbieter bereitgestellt wird, interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="1629d-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="1629d-118">Diese Eigenschaft wird nur als ein Eintrag in der Spalte in der Tabelle Anbieter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1629d-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1629d-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1629d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1629d-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1629d-120">Header files</span></span>

<span data-ttu-id="1629d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1629d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1629d-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1629d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1629d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1629d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1629d-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1629d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1629d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1629d-125">See also</span></span>



[<span data-ttu-id="1629d-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1629d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1629d-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1629d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1629d-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1629d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1629d-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1629d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

