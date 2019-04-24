---
title: Kanonische PidTagSenderEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358912"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="73b5c-103">Kanonische PidTagSenderEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73b5c-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="73b5c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73b5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73b5c-105">Enthält die Eintrags-ID des Nachrichtenabsenders.</span><span class="sxs-lookup"><span data-stu-id="73b5c-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73b5c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="73b5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73b5c-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="73b5c-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="73b5c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="73b5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73b5c-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="73b5c-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="73b5c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="73b5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="73b5c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73b5c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73b5c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="73b5c-112">Area:</span></span>  <br/> |<span data-ttu-id="73b5c-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="73b5c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b5c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73b5c-114">Remarks</span></span>

<span data-ttu-id="73b5c-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73b5c-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="73b5c-116">Er muss vom ausgehenden Transportanbieter festgelegt werden, der niemals zuvor vorhandene Werte weitergeben sollte.</span><span class="sxs-lookup"><span data-stu-id="73b5c-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="73b5c-117">Wenn kein Transportanbieter Eigenschaften für Absenderadressen angegeben hat, versucht der MAPI-Spooler, diese einzufüllen, indem er die [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) -Methode für eine Eintrags-ID aufruft.</span><span class="sxs-lookup"><span data-stu-id="73b5c-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="73b5c-118">Wenn keine Eintrags-IDs angegeben wurden, hat der MAPI-Spooler einen Bezeichner, der der Zeichenfolge "unknown" in dieser Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="73b5c-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73b5c-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="73b5c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73b5c-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="73b5c-120">Protocol specifications</span></span>

<span data-ttu-id="73b5c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="73b5c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73b5c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="73b5c-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="73b5c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-126">Gibt die Eigenschaften und Vorgänge an, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="73b5c-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="73b5c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-128">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="73b5c-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="73b5c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-130">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="73b5c-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="73b5c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-132">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="73b5c-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="73b5c-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b5c-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b5c-134">Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="73b5c-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73b5c-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="73b5c-135">Header files</span></span>

<span data-ttu-id="73b5c-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="73b5c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="73b5c-137">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="73b5c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="73b5c-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="73b5c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="73b5c-139">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="73b5c-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73b5c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73b5c-140">See also</span></span>



[<span data-ttu-id="73b5c-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73b5c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73b5c-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73b5c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73b5c-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="73b5c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73b5c-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="73b5c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

