---
title: PidTagSensitivity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f30a5848e07de03e61d3a63188aa7b608504ff24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573733"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="e6568-103">PidTagSensitivity (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e6568-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="e6568-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6568-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6568-105">Enthält einen Wert, der den Nachrichtenabsender Opinion, der die Vertraulichkeit einer Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="e6568-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6568-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e6568-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6568-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="e6568-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="e6568-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e6568-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6568-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="e6568-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="e6568-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e6568-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6568-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e6568-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e6568-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e6568-112">Area:</span></span>  <br/> |<span data-ttu-id="e6568-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="e6568-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6568-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e6568-114">Remarks</span></span>

<span data-ttu-id="e6568-115">Es wird empfohlen, dass Message Objekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e6568-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="e6568-116">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e6568-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e6568-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="e6568-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="e6568-118">Die Nachricht weist keine besondere Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="e6568-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="e6568-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="e6568-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="e6568-120">Die Nachricht ist persönlich.</span><span class="sxs-lookup"><span data-stu-id="e6568-120">The message is personal.</span></span>
    
<span data-ttu-id="e6568-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="e6568-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="e6568-122">Die Nachricht ist privat.</span><span class="sxs-lookup"><span data-stu-id="e6568-122">The message is private.</span></span>
    
<span data-ttu-id="e6568-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="e6568-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="e6568-124">Die Nachricht wird Firma (vertraulich) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6568-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e6568-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6568-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6568-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e6568-126">Protocol specifications</span></span>

<span data-ttu-id="e6568-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6568-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6568-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e6568-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6568-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6568-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6568-130">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="e6568-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6568-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e6568-131">Header files</span></span>

<span data-ttu-id="e6568-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6568-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6568-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e6568-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6568-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6568-134">Mapitags.h</span></span>
  
> <span data-ttu-id="e6568-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e6568-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6568-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6568-136">See also</span></span>



[<span data-ttu-id="e6568-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6568-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6568-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6568-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6568-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e6568-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6568-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e6568-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

