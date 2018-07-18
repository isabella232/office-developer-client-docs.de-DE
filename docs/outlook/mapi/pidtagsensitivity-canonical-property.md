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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795144"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="feb07-103">PidTagSensitivity (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="feb07-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="feb07-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feb07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feb07-105">Enthält einen Wert, der den Nachrichtenabsender Opinion, der die Vertraulichkeit einer Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="feb07-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="feb07-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="feb07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="feb07-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="feb07-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="feb07-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="feb07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="feb07-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="feb07-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="feb07-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="feb07-110">Data type:</span></span>  <br/> |<span data-ttu-id="feb07-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="feb07-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="feb07-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="feb07-112">Area:</span></span>  <br/> |<span data-ttu-id="feb07-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="feb07-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feb07-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feb07-114">Remarks</span></span>

<span data-ttu-id="feb07-115">Es wird empfohlen, dass Message Objekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="feb07-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="feb07-116">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="feb07-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="feb07-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="feb07-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="feb07-118">Die Nachricht weist keine besondere Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="feb07-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="feb07-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="feb07-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="feb07-120">Die Nachricht ist persönlich.</span><span class="sxs-lookup"><span data-stu-id="feb07-120">The message is personal.</span></span>
    
<span data-ttu-id="feb07-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="feb07-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="feb07-122">Die Nachricht ist privat.</span><span class="sxs-lookup"><span data-stu-id="feb07-122">The message is private.</span></span>
    
<span data-ttu-id="feb07-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="feb07-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="feb07-124">Die Nachricht wird Firma (vertraulich) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="feb07-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="feb07-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="feb07-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="feb07-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="feb07-126">Protocol specifications</span></span>

<span data-ttu-id="feb07-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb07-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb07-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="feb07-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="feb07-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feb07-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feb07-130">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="feb07-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="feb07-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="feb07-131">Header files</span></span>

<span data-ttu-id="feb07-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="feb07-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="feb07-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="feb07-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="feb07-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="feb07-134">Mapitags.h</span></span>
  
> <span data-ttu-id="feb07-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="feb07-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="feb07-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feb07-136">See also</span></span>



[<span data-ttu-id="feb07-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="feb07-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="feb07-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="feb07-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="feb07-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="feb07-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="feb07-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="feb07-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

