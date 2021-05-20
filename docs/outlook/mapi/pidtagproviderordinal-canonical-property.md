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
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438351"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="4359f-103">PidTagProviderOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4359f-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="4359f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4359f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4359f-105">Enthält den nullbasierten Index der Position eines Dienstanbieters in der Anbietertabelle.</span><span class="sxs-lookup"><span data-stu-id="4359f-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4359f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4359f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4359f-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="4359f-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="4359f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4359f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4359f-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="4359f-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="4359f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4359f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4359f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4359f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4359f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4359f-112">Area:</span></span>  <br/> |<span data-ttu-id="4359f-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="4359f-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4359f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4359f-114">Remarks</span></span>

<span data-ttu-id="4359f-115">Diese Eigenschaft wird von MAPI berechnet.</span><span class="sxs-lookup"><span data-stu-id="4359f-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="4359f-116">Rufen Sie die Anbietertabelle ab, indem Sie die [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4359f-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="4359f-117">Sortieren Sie die Anbietertabelle für diese Eigenschaft so, dass die Transportreihenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4359f-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4359f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4359f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4359f-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4359f-119">Header files</span></span>

<span data-ttu-id="4359f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4359f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4359f-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4359f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4359f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4359f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4359f-123">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4359f-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4359f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4359f-124">See also</span></span>



[<span data-ttu-id="4359f-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4359f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4359f-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4359f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4359f-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4359f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4359f-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4359f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

