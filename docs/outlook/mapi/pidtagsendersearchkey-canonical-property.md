---
title: Kanonische Pidtagsendersearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342854"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="8d770-103">Kanonische Pidtagsendersearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d770-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="8d770-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d770-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d770-105">Enthält den Suchschlüssel des Nachrichtenabsenders.</span><span class="sxs-lookup"><span data-stu-id="8d770-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d770-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8d770-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d770-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="8d770-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="8d770-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8d770-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d770-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="8d770-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="8d770-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8d770-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d770-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d770-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d770-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8d770-112">Area:</span></span>  <br/> |<span data-ttu-id="8d770-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="8d770-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d770-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d770-114">Remarks</span></span>

<span data-ttu-id="8d770-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8d770-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="8d770-116">Er muss vom ausgehenden Transportanbieter festgelegt werden, der niemals zuvor vorhandene Werte weitergeben sollte.</span><span class="sxs-lookup"><span data-stu-id="8d770-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="8d770-117">Wenn kein Transportanbieter Eigenschaften für Absenderadressen angegeben hat, versucht der MAPI-Spooler, diese einzufüllen, indem er die [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) -Methode für eine Eintrags-ID aufruft.</span><span class="sxs-lookup"><span data-stu-id="8d770-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="8d770-118">Wenn keine Eintrags-IDs angegeben wurden, speichert der MAPI-Spooler einen Schlüssel, der der Zeichenfolge "unknown" in dieser Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="8d770-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d770-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d770-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d770-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8d770-120">Protocol specifications</span></span>

<span data-ttu-id="8d770-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8d770-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d770-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d770-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d770-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-126">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="8d770-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d770-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-128">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="8d770-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8d770-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-130">Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d770-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8d770-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-132">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d770-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="8d770-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d770-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d770-134">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="8d770-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d770-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8d770-135">Header files</span></span>

<span data-ttu-id="8d770-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8d770-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d770-137">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8d770-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d770-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8d770-138">Mapitags.h</span></span>
  
> <span data-ttu-id="8d770-139">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8d770-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d770-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d770-140">See also</span></span>



[<span data-ttu-id="8d770-141">Kanonische Pidtagsearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d770-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="8d770-142">Kanonische Pidtagsentrepresentingsearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d770-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="8d770-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d770-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d770-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d770-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d770-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8d770-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d770-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8d770-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

