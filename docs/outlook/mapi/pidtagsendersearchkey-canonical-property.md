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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea0e2b753212acc48c56240b3a72b7f22954802a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795129"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="82b0e-103">PidTagSenderSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82b0e-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="82b0e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82b0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82b0e-105">Enthält den Nachrichtenabsender suchen-Taste.</span><span class="sxs-lookup"><span data-stu-id="82b0e-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82b0e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="82b0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82b0e-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="82b0e-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="82b0e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="82b0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82b0e-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="82b0e-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="82b0e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="82b0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="82b0e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82b0e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82b0e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="82b0e-112">Area:</span></span>  <br/> |<span data-ttu-id="82b0e-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="82b0e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82b0e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82b0e-114">Remarks</span></span>

<span data-ttu-id="82b0e-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="82b0e-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="82b0e-116">Es muss von der ausgehenden Adressbuchhierarchie festgelegt werden nie alle zuvor vorhandenen Werte weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82b0e-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="82b0e-117">Wenn keine Adressbuchhierarchie alle Eigenschaften des Absenders-Adresse angegeben, versucht die MAPI-Warteschlange werden durch Aufrufen der [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode für die Eintrags-ID ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="82b0e-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="82b0e-118">Wenn keine Eintragsbezeichner bereitgestellt wurde, speichert die MAPI-Warteschlange einen Schlüssel, der die Zeichenfolge "Unknown" in dieser Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="82b0e-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82b0e-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82b0e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82b0e-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="82b0e-120">Protocol specifications</span></span>

<span data-ttu-id="82b0e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="82b0e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82b0e-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="82b0e-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="82b0e-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="82b0e-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="82b0e-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="82b0e-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="82b0e-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-130">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="82b0e-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="82b0e-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-132">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="82b0e-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="82b0e-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b0e-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b0e-134">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="82b0e-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82b0e-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="82b0e-135">Header files</span></span>

<span data-ttu-id="82b0e-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82b0e-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="82b0e-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="82b0e-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="82b0e-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82b0e-138">Mapitags.h</span></span>
  
> <span data-ttu-id="82b0e-139">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="82b0e-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82b0e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82b0e-140">See also</span></span>



[<span data-ttu-id="82b0e-141">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82b0e-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="82b0e-142">PidTagSentRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82b0e-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="82b0e-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82b0e-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82b0e-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82b0e-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82b0e-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="82b0e-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82b0e-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="82b0e-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

