---
title: Kanonische PidTagAlternateRecipient-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea78d9487e4929c2df3d49a9b85ba4aefac90a59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794061"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="8824d-103">Kanonische PidTagAlternateRecipient-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8824d-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="8824d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8824d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8824d-105">Enthält eine Liste der Eintragsbezeichner für den ursprünglichen Empfänger genehmigtes alternativen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="8824d-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8824d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8824d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8824d-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="8824d-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="8824d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="8824d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8824d-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="8824d-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="8824d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8824d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8824d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8824d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8824d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8824d-112">Area:</span></span>  <br/> |<span data-ttu-id="8824d-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="8824d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8824d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8824d-114">Remarks</span></span>

<span data-ttu-id="8824d-115">Diese Eigenschaft wird für die automatische weitergeleiteten Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8824d-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="8824d-116">Sie enthält eine [FLATENTRYLIST](flatentrylist.md) Struktur der alternativen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="8824d-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="8824d-117">Wenn die automatische Weiterleitung nicht zulässig ist oder keine alternativer Empfänger festgelegt wurde, wird ein Unzustellbarkeitsbericht generiert.</span><span class="sxs-lookup"><span data-stu-id="8824d-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8824d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8824d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8824d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8824d-119">Protocol specifications</span></span>

<span data-ttu-id="8824d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8824d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8824d-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8824d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8824d-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8824d-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8824d-123">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="8824d-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8824d-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8824d-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8824d-125">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="8824d-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8824d-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8824d-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8824d-127">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="8824d-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8824d-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8824d-128">Header files</span></span>

<span data-ttu-id="8824d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8824d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8824d-130">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8824d-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="8824d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8824d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="8824d-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8824d-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8824d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8824d-133">See also</span></span>



[<span data-ttu-id="8824d-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="8824d-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="8824d-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8824d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8824d-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8824d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8824d-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8824d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8824d-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8824d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

