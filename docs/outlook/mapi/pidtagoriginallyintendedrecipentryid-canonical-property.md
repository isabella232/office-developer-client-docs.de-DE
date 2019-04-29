---
title: Kanonische Pidtagoriginallyintendedrecipentryid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430140"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="edc00-103">Kanonische Pidtagoriginallyintendedrecipentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="edc00-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="edc00-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc00-105">Enthält die Eintrags-ID des ursprünglich vorgesehenen Empfängers einer automatisch weitergeleiteten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="edc00-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edc00-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="edc00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edc00-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="edc00-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="edc00-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="edc00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edc00-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="edc00-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="edc00-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="edc00-110">Data type:</span></span>  <br/> |<span data-ttu-id="edc00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edc00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edc00-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="edc00-112">Area:</span></span>  <br/> |<span data-ttu-id="edc00-113">Server</span><span class="sxs-lookup"><span data-stu-id="edc00-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edc00-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edc00-114">Remarks</span></span>

<span data-ttu-id="edc00-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglich beabsichtigten Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="edc00-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="edc00-116">Er muss vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="edc00-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="edc00-117">Diese Eigenschaft entspricht dem Attribut X. 400 pro Empfänger.</span><span class="sxs-lookup"><span data-stu-id="edc00-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edc00-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="edc00-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="edc00-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="edc00-119">Header files</span></span>

<span data-ttu-id="edc00-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="edc00-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="edc00-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="edc00-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="edc00-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="edc00-122">Mapitags.h</span></span>
  
> <span data-ttu-id="edc00-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="edc00-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edc00-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edc00-124">See also</span></span>



[<span data-ttu-id="edc00-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edc00-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edc00-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edc00-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edc00-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="edc00-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edc00-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="edc00-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

