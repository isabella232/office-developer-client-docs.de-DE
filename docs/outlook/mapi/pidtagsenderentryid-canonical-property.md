---
title: PidTagSenderEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2e8ecba7c92dcbcb719591464e10fb4af2d2344
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591765"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="c46db-103">PidTagSenderEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c46db-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c46db-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c46db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c46db-105">Eintrags-ID des Absenders der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="c46db-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c46db-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c46db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c46db-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c46db-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c46db-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c46db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c46db-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="c46db-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="c46db-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c46db-110">Data type:</span></span>  <br/> |<span data-ttu-id="c46db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c46db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c46db-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c46db-112">Area:</span></span>  <br/> |<span data-ttu-id="c46db-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="c46db-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c46db-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c46db-114">Remarks</span></span>

<span data-ttu-id="c46db-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c46db-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="c46db-116">Es muss von der ausgehenden Adressbuchhierarchie festgelegt werden nie alle zuvor vorhandenen Werte weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c46db-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="c46db-117">Wenn keine Adressbuchhierarchie alle Eigenschaften des Absenders-Adresse angegeben, versucht die MAPI-Warteschlange werden durch Aufrufen der [IMAPISession::QueryIdentity](imapisession-queryidentity.md) -Methode für die Eintrags-ID ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="c46db-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="c46db-118">Wenn kein Eintrag Bezeichner angegeben wurden, einer Kennung, die Zeichenfolge "Unknown" in dieser Eigenschaft entspricht der MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="c46db-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c46db-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c46db-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c46db-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c46db-120">Protocol specifications</span></span>

<span data-ttu-id="c46db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c46db-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c46db-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c46db-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c46db-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-126">Gibt die Eigenschaften und Operationen, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="c46db-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="c46db-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-128">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="c46db-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c46db-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-130">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="c46db-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c46db-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-132">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="c46db-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c46db-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c46db-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c46db-134">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c46db-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c46db-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c46db-135">Header files</span></span>

<span data-ttu-id="c46db-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c46db-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c46db-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c46db-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c46db-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c46db-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c46db-139">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c46db-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c46db-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c46db-140">See also</span></span>



[<span data-ttu-id="c46db-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c46db-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c46db-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c46db-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c46db-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c46db-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c46db-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c46db-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

