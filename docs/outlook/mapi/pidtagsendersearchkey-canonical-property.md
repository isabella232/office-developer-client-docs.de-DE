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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386089"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="7e636-103">PidTagSenderSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e636-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="7e636-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e636-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e636-105">Enthält den Nachrichtenabsender suchen-Taste.</span><span class="sxs-lookup"><span data-stu-id="7e636-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e636-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7e636-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e636-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="7e636-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="7e636-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7e636-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e636-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="7e636-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="7e636-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7e636-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e636-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7e636-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7e636-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7e636-112">Area:</span></span>  <br/> |<span data-ttu-id="7e636-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="7e636-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e636-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e636-114">Remarks</span></span>

<span data-ttu-id="7e636-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7e636-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="7e636-116">Es muss von der ausgehenden Adressbuchhierarchie festgelegt werden nie alle zuvor vorhandenen Werte weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e636-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="7e636-117">Wenn keine Adressbuchhierarchie alle Eigenschaften des Absenders-Adresse angegeben, versucht die MAPI-Warteschlange werden durch Aufrufen der [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode für die Eintrags-ID ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="7e636-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="7e636-118">Wenn keine Eintragsbezeichner bereitgestellt wurde, speichert die MAPI-Warteschlange einen Schlüssel, der die Zeichenfolge "Unknown" in dieser Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="7e636-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7e636-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7e636-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e636-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7e636-120">Protocol specifications</span></span>

<span data-ttu-id="7e636-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7e636-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e636-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7e636-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7e636-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="7e636-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7e636-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7e636-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7e636-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-130">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e636-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="7e636-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-132">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7e636-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="7e636-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e636-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e636-134">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="7e636-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e636-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7e636-135">Header files</span></span>

<span data-ttu-id="7e636-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e636-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e636-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7e636-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e636-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7e636-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7e636-139">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7e636-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e636-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e636-140">See also</span></span>



[<span data-ttu-id="7e636-141">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e636-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="7e636-142">PidTagSentRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e636-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="7e636-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e636-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e636-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e636-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e636-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7e636-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e636-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7e636-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

