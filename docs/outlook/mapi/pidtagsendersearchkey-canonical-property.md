---
title: PidTagSenderSearchKey (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c36d9744bcf5b1126a0fcc90ae6330f2dc8ef0ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342854"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="1afef-103">PidTagSenderSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1afef-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="1afef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1afef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1afef-105">Enthält den Suchschlüssel des Nachrichtensenders.</span><span class="sxs-lookup"><span data-stu-id="1afef-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1afef-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1afef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1afef-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1afef-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="1afef-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1afef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1afef-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="1afef-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="1afef-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1afef-110">Data type:</span></span>  <br/> |<span data-ttu-id="1afef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1afef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1afef-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1afef-112">Area:</span></span>  <br/> |<span data-ttu-id="1afef-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="1afef-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1afef-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1afef-114">Remarks</span></span>

<span data-ttu-id="1afef-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Nachrichtensender.</span><span class="sxs-lookup"><span data-stu-id="1afef-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="1afef-116">Sie muss vom ausgehenden Transportanbieter festgelegt werden, der keine zuvor vorhandenen Werte weitervermittelt.</span><span class="sxs-lookup"><span data-stu-id="1afef-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="1afef-117">Wenn kein Transportanbieter Absenderadresseneigenschaften angegeben hat, versucht der MAPI-Spooler, sie durch Aufrufen der [IMAPISession::QueryIdentity-Methode](imapisession-queryidentity.md) für einen Eintragsbezeichner zu füllen.</span><span class="sxs-lookup"><span data-stu-id="1afef-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="1afef-118">Wenn keine Eintragsbezeichner angegeben wurden, speichert der MAPI-Spooler einen Schlüssel, der der Zeichenfolge "Unknown" in dieser Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="1afef-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1afef-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1afef-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1afef-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1afef-120">Protocol specifications</span></span>

<span data-ttu-id="1afef-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1afef-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1afef-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1afef-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="1afef-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="1afef-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1afef-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-128">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="1afef-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1afef-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-130">Gibt die Eigenschaften und Vorgänge an, die für Postobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1afef-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="1afef-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-132">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1afef-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="1afef-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afef-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1afef-134">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="1afef-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1afef-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1afef-135">Header files</span></span>

<span data-ttu-id="1afef-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1afef-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1afef-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1afef-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1afef-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1afef-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1afef-139">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1afef-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1afef-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1afef-140">See also</span></span>



[<span data-ttu-id="1afef-141">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1afef-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="1afef-142">PidTagSentRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1afef-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="1afef-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1afef-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1afef-144">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1afef-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1afef-145">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1afef-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1afef-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1afef-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

