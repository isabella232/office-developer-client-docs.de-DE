---
title: Kanonische PidTagSenderName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355069"
---
# <a name="pidtagsendername-canonical-property"></a><span data-ttu-id="37f62-103">Kanonische PidTagSenderName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="37f62-103">PidTagSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="37f62-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37f62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37f62-105">Enthält den Anzeigenamen des Nachrichtenabsenders.</span><span class="sxs-lookup"><span data-stu-id="37f62-105">Contains the message sender's display name.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37f62-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="37f62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37f62-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="37f62-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="37f62-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="37f62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37f62-109">0x0C1A</span><span class="sxs-lookup"><span data-stu-id="37f62-109">0x0C1A</span></span>  <br/> |
|<span data-ttu-id="37f62-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="37f62-110">Data type:</span></span>  <br/> |<span data-ttu-id="37f62-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="37f62-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="37f62-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="37f62-112">Area:</span></span>  <br/> |<span data-ttu-id="37f62-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="37f62-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37f62-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37f62-114">Remarks</span></span>

<span data-ttu-id="37f62-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37f62-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="37f62-116">Er muss vom ausgehenden Transportanbieter festgelegt werden, der niemals zuvor vorhandene Werte weitergeben sollte.</span><span class="sxs-lookup"><span data-stu-id="37f62-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="37f62-117">Wenn kein Transportanbieter Eigenschaften für Absenderadressen angegeben hat, versucht der MAPI-Spooler, diese einzufüllen, indem er die [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) -Methode für eine Eintrags-ID aufruft.</span><span class="sxs-lookup"><span data-stu-id="37f62-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="37f62-118">Wenn keine Eintrags-IDs angegeben wurden, speichert der MAPI-Spooler "unbekannt" in allen Absender Adresseigenschaften vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="37f62-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="37f62-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37f62-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37f62-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="37f62-120">Protocol specifications</span></span>

<span data-ttu-id="37f62-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="37f62-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37f62-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-124">Beschreibt das Format der Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37f62-124">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
<span data-ttu-id="37f62-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-126">Gibt die Eigenschaften und Vorgänge an, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="37f62-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="37f62-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-128">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="37f62-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="37f62-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-130">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="37f62-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="37f62-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-132">Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="37f62-132">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="37f62-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-134">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="37f62-134">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="37f62-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f62-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f62-136">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="37f62-136">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37f62-137">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="37f62-137">Header files</span></span>

<span data-ttu-id="37f62-138">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="37f62-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="37f62-139">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="37f62-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="37f62-140">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="37f62-140">Mapitags.h</span></span>
  
> <span data-ttu-id="37f62-141">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="37f62-141">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37f62-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f62-142">See also</span></span>



[<span data-ttu-id="37f62-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37f62-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37f62-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37f62-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37f62-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="37f62-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37f62-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="37f62-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

