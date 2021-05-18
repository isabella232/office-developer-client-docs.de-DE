---
title: PidTagSenderAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1389c1189293955145f14e65f4c0f3e58bec909f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359143"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a><span data-ttu-id="d3530-103">PidTagSenderAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3530-103">PidTagSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="d3530-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3530-105">Enthält den E-Mail-Adresstyp des Absenders.</span><span class="sxs-lookup"><span data-stu-id="d3530-105">Contains the message sender's email address type.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3530-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d3530-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3530-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="d3530-107">PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="d3530-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d3530-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3530-109">0x0C1E</span><span class="sxs-lookup"><span data-stu-id="d3530-109">0x0C1E</span></span>  <br/> |
|<span data-ttu-id="d3530-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d3530-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3530-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d3530-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d3530-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d3530-112">Area:</span></span>  <br/> |<span data-ttu-id="d3530-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="d3530-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3530-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3530-114">Remarks</span></span>

<span data-ttu-id="d3530-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Nachrichtensender.</span><span class="sxs-lookup"><span data-stu-id="d3530-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="d3530-116">Sie muss vom ausgehenden Transportanbieter festgelegt werden, der keine zuvor vorhandenen Werte weitervermittelt.</span><span class="sxs-lookup"><span data-stu-id="d3530-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="d3530-117">Wenn kein Transportanbieter Absenderadresseneigenschaften angegeben hat, versucht der MAPI-Spooler, sie durch Aufrufen der [IMAPISession::QueryIdentity-Methode](imapisession-queryidentity.md) für einen Eintragsbezeichner zu füllen.</span><span class="sxs-lookup"><span data-stu-id="d3530-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="d3530-118">Wenn keine Eintragsbezeichner angegeben wurden, speichert der MAPI-Spooler "Unknown" in allen Absenderadresseneigenschaften vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="d3530-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3530-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3530-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3530-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d3530-120">Protocol specifications</span></span>

<span data-ttu-id="d3530-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d3530-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3530-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d3530-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d3530-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="d3530-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d3530-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-128">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="d3530-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d3530-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-130">Gibt die Eigenschaften und Vorgänge an, die für Postobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d3530-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="d3530-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-132">Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlistenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d3530-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="d3530-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3530-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3530-134">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="d3530-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3530-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d3530-135">Header files</span></span>

<span data-ttu-id="d3530-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3530-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3530-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d3530-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3530-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3530-138">Mapitags.h</span></span>
  
> <span data-ttu-id="d3530-139">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d3530-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3530-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3530-140">See also</span></span>



[<span data-ttu-id="d3530-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3530-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3530-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d3530-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3530-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d3530-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3530-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d3530-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

