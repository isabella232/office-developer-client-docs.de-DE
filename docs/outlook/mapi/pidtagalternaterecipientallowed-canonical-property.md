---
title: PidTagAlternateRecipientAllowed (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385956"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="e64d0-103">PidTagAlternateRecipientAllowed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e64d0-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="e64d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e64d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e64d0-105">Enthält True, wenn der Absender automatische Weiterleitung der Nachricht ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e64d0-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e64d0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e64d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e64d0-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e64d0-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="e64d0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e64d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e64d0-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="e64d0-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="e64d0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e64d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="e64d0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e64d0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e64d0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e64d0-112">Area:</span></span>  <br/> |<span data-ttu-id="e64d0-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="e64d0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e64d0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e64d0-114">Remarks</span></span>

<span data-ttu-id="e64d0-115">Wenn die automatische Weiterleitung nicht zulässig ist oder keine alternativer Empfänger vorgesehen ist, sollte ein Unzustellbarkeitsbericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e64d0-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e64d0-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e64d0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e64d0-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e64d0-117">Protocol specifications</span></span>

<span data-ttu-id="e64d0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e64d0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e64d0-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e64d0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e64d0-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e64d0-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e64d0-121">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="e64d0-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e64d0-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e64d0-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e64d0-123">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e64d0-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e64d0-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e64d0-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e64d0-125">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="e64d0-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e64d0-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e64d0-126">Header files</span></span>

<span data-ttu-id="e64d0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e64d0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e64d0-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e64d0-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e64d0-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e64d0-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e64d0-130">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e64d0-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e64d0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e64d0-131">See also</span></span>



[<span data-ttu-id="e64d0-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64d0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e64d0-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64d0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e64d0-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e64d0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e64d0-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e64d0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

