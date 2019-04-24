---
title: Kanonische Pidtagalternaterecipientallowed (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327986"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="897ea-103">Kanonische Pidtagalternaterecipientallowed (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="897ea-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="897ea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="897ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="897ea-105">Enthält TRUE, wenn der Absender die automatische Weiterleitung dieser Nachricht zulässt.</span><span class="sxs-lookup"><span data-stu-id="897ea-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="897ea-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="897ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="897ea-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="897ea-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="897ea-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="897ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="897ea-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="897ea-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="897ea-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="897ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="897ea-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="897ea-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="897ea-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="897ea-112">Area:</span></span>  <br/> |<span data-ttu-id="897ea-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="897ea-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="897ea-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="897ea-114">Remarks</span></span>

<span data-ttu-id="897ea-115">Wenn die automatische Weiterleitung nicht zulässig ist oder kein alternativer Empfänger festgelegt wurde, sollte ein Unzustellbarkeitsbericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="897ea-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="897ea-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="897ea-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="897ea-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="897ea-117">Protocol specifications</span></span>

<span data-ttu-id="897ea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897ea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897ea-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="897ea-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="897ea-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897ea-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897ea-121">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="897ea-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="897ea-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897ea-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897ea-123">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="897ea-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="897ea-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897ea-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897ea-125">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="897ea-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="897ea-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="897ea-126">Header files</span></span>

<span data-ttu-id="897ea-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="897ea-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="897ea-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="897ea-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="897ea-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="897ea-129">Mapitags.h</span></span>
  
> <span data-ttu-id="897ea-130">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="897ea-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="897ea-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="897ea-131">See also</span></span>



[<span data-ttu-id="897ea-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="897ea-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="897ea-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="897ea-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="897ea-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="897ea-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="897ea-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="897ea-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

