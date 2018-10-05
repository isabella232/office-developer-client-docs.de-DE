---
title: PidTagAlternateRecipient (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392781"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="99974-103">PidTagAlternateRecipient (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="99974-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="99974-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99974-105">Enthält eine Liste der Eintragsbezeichner für den ursprünglichen Empfänger genehmigtes alternativen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="99974-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99974-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="99974-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99974-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="99974-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="99974-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="99974-108">Identifier:</span></span>  <br/> |<span data-ttu-id="99974-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="99974-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="99974-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="99974-110">Data type:</span></span>  <br/> |<span data-ttu-id="99974-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="99974-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="99974-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="99974-112">Area:</span></span>  <br/> |<span data-ttu-id="99974-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="99974-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99974-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99974-114">Remarks</span></span>

<span data-ttu-id="99974-115">Diese Eigenschaft wird für die automatische weitergeleiteten Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="99974-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="99974-116">Sie enthält eine [FLATENTRYLIST](flatentrylist.md) Struktur der alternativen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="99974-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="99974-117">Wenn die automatische Weiterleitung nicht zulässig ist oder keine alternativer Empfänger festgelegt wurde, wird ein Unzustellbarkeitsbericht generiert.</span><span class="sxs-lookup"><span data-stu-id="99974-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99974-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="99974-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99974-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="99974-119">Protocol specifications</span></span>

<span data-ttu-id="99974-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99974-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99974-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="99974-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99974-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99974-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99974-123">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="99974-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="99974-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99974-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99974-125">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="99974-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="99974-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99974-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99974-127">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="99974-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99974-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="99974-128">Header files</span></span>

<span data-ttu-id="99974-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="99974-129">Mapitags.h</span></span>
  
> <span data-ttu-id="99974-130">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="99974-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="99974-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99974-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="99974-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="99974-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99974-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99974-133">See also</span></span>



[<span data-ttu-id="99974-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="99974-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="99974-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99974-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99974-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99974-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99974-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="99974-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99974-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="99974-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

