---
title: PidTagSenderEmailAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82c0e386ab9231d1066dbdc4456c31031d2409c1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386950"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="7fe13-103">PidTagSenderEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7fe13-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="7fe13-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fe13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fe13-105">E-Mail-Adresse des Absenders der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="7fe13-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fe13-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7fe13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fe13-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="7fe13-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="7fe13-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7fe13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7fe13-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="7fe13-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="7fe13-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7fe13-110">Data type:</span></span>  <br/> |<span data-ttu-id="7fe13-111">PT_UNICOIDE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7fe13-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7fe13-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7fe13-112">Area:</span></span>  <br/> |<span data-ttu-id="7fe13-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="7fe13-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fe13-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fe13-114">Remarks</span></span>

<span data-ttu-id="7fe13-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7fe13-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="7fe13-116">Sie müssen von der ausgehenden Adressbuchhierarchie festgelegt werden alle zuvor vorhandenen Werte nie weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7fe13-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="7fe13-117">Wenn keine Adressbuchhierarchie alle Eigenschaften des Absenders-Adresse angegeben, versucht die MAPI-Warteschlange werden durch Aufrufen der [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode für die Eintrags-ID ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="7fe13-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="7fe13-118">Wenn keine Eintragsbezeichner bereitgestellt wurde, speichert die MAPI-Warteschlange "Unknown" in alle Absender Adresseigenschaften vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="7fe13-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7fe13-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7fe13-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fe13-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7fe13-120">Protocol specifications</span></span>

<span data-ttu-id="7fe13-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7fe13-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7fe13-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7fe13-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7fe13-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="7fe13-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7fe13-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7fe13-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7fe13-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-129">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-130">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7fe13-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="7fe13-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-131">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-132">Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7fe13-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="7fe13-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe13-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe13-134">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="7fe13-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fe13-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7fe13-135">Header files</span></span>

<span data-ttu-id="7fe13-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fe13-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fe13-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7fe13-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7fe13-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7fe13-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7fe13-139">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7fe13-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fe13-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fe13-140">See also</span></span>



[<span data-ttu-id="7fe13-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fe13-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fe13-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fe13-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fe13-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7fe13-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fe13-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7fe13-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

