---
title: PidTagEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f3d49faba9d1e9cc8609ee55f7fb3c329e9ae947
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593039"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="168bd-103">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="168bd-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="168bd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="168bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="168bd-105">Enthält eine MAPI-Eintrags-ID, die zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="168bd-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="168bd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="168bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="168bd-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="168bd-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="168bd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="168bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="168bd-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="168bd-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="168bd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="168bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="168bd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="168bd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="168bd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="168bd-112">Area:</span></span>  <br/> |<span data-ttu-id="168bd-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="168bd-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="168bd-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="168bd-114">Remarks</span></span>

<span data-ttu-id="168bd-115">Diese Eigenschaft gibt ein Objekt für **OpenEntry** zum Instanziieren und ermöglicht den Zugriff auf alle seine Eigenschaften über die entsprechenden abgeleiteten Schnittstelle des **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="168bd-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="168bd-116">Diese Eigenschaft ist eine der Eigenschaften für alle Benutzer messaging Basisadresse.</span><span class="sxs-lookup"><span data-stu-id="168bd-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="168bd-117">Diese Eigenschaft kann eine langfristige oder einen kurzfristigen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="168bd-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="168bd-118">Kurzfristige Bezeichner sind schneller und einfacher, Konstrukt, aber in deren Bereich und die Dauer, in der Regel auf der aktuellen Sitzung und Arbeitsstation beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="168bd-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="168bd-119">Sie sind häufig verwendet, um Objekte vorübergehender Art, wie Zeilen der Tabelle oder Einträgen im Dialogfeld, und klicken Sie dann abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="168bd-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="168bd-120">Langfristige-IDs werden für eine umfassende und langfristig Art-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="168bd-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="168bd-121">Diese Eigenschaft ist immer über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="168bd-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="168bd-122">Einige Dienstanbieter können sie sofort nach der Instanziierung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="168bd-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="168bd-123">Der Anbieter muss immer eine langfristige Eintrags-ID aus **GetProps**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="168bd-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="168bd-124">Aus diesem Grund um einen kurzfristigen Bezeichner in langfristige konvertieren, einfach öffnen Sie das Objekt und seine dies abrufen-Eigenschaft über **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="168bd-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="168bd-125">In der folgenden Tabelle werden wichtige Unterschiede zwischen den diese Eigenschaft **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="168bd-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="168bd-126">**Merkmale**</span><span class="sxs-lookup"><span data-stu-id="168bd-126">**Characteristic**</span></span>|<span data-ttu-id="168bd-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="168bd-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="168bd-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="168bd-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="168bd-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="168bd-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="168bd-130">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="168bd-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="168bd-131">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-131">No</span></span>  <br/> |<span data-ttu-id="168bd-132">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-132">Yes</span></span>  <br/> |<span data-ttu-id="168bd-133">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-133">No</span></span>  <br/> |
|<span data-ttu-id="168bd-134">Auf Ordnerobjekten erforderlich</span><span class="sxs-lookup"><span data-stu-id="168bd-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="168bd-135">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-135">Yes</span></span>  <br/> |<span data-ttu-id="168bd-136">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-136">Yes</span></span>  <br/> |<span data-ttu-id="168bd-137">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-137">No</span></span>  <br/> |
|<span data-ttu-id="168bd-138">Erforderlich für Nachricht Store-Objekte</span><span class="sxs-lookup"><span data-stu-id="168bd-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="168bd-139">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-139">Yes</span></span>  <br/> |<span data-ttu-id="168bd-140">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-140">Yes</span></span>  <br/> |<span data-ttu-id="168bd-141">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-141">No</span></span>  <br/> |
|<span data-ttu-id="168bd-142">Klicken Sie auf Status Objekte erforderlich</span><span class="sxs-lookup"><span data-stu-id="168bd-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="168bd-143">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-143">Yes</span></span>  <br/> |<span data-ttu-id="168bd-144">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-144">No</span></span>  <br/> |<span data-ttu-id="168bd-145">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-145">No</span></span>  <br/> |
|<span data-ttu-id="168bd-146">Vom Client erstellt</span><span class="sxs-lookup"><span data-stu-id="168bd-146">Created by client</span></span>  <br/> |<span data-ttu-id="168bd-147">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-147">No</span></span>  <br/> |<span data-ttu-id="168bd-148">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-148">No</span></span>  <br/> |<span data-ttu-id="168bd-149">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-149">Yes</span></span>  <br/> |
|<span data-ttu-id="168bd-150">Vor dem Aufruf von **SaveChanges** verfügbar</span><span class="sxs-lookup"><span data-stu-id="168bd-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="168bd-151">Hängt vom anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="168bd-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="168bd-152">Hängt vom anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="168bd-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="168bd-153">Für Nachrichten, Ja.</span><span class="sxs-lookup"><span data-stu-id="168bd-153">For messages, Yes.</span></span> <span data-ttu-id="168bd-154">Für andere hängt von anbieterimplementierung.</span><span class="sxs-lookup"><span data-stu-id="168bd-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="168bd-155">Geändert in einen Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="168bd-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="168bd-156">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-156">Yes</span></span>  <br/> |<span data-ttu-id="168bd-157">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-157">Yes</span></span>  <br/> |<span data-ttu-id="168bd-158">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-158">No</span></span>  <br/> |
|<span data-ttu-id="168bd-159">Vom Client beim Kopieren eines veränderbar</span><span class="sxs-lookup"><span data-stu-id="168bd-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="168bd-160">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-160">No</span></span>  <br/> |<span data-ttu-id="168bd-161">Nein</span><span class="sxs-lookup"><span data-stu-id="168bd-161">No</span></span>  <br/> |<span data-ttu-id="168bd-162">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-162">Yes</span></span>  <br/> |
|<span data-ttu-id="168bd-163">Innerhalb eindeutig</span><span class="sxs-lookup"><span data-stu-id="168bd-163">Unique within</span></span>  <br/> |<span data-ttu-id="168bd-164">Weltweit</span><span class="sxs-lookup"><span data-stu-id="168bd-164">Entire world</span></span>  <br/> |<span data-ttu-id="168bd-165">Providerinstanz</span><span class="sxs-lookup"><span data-stu-id="168bd-165">Provider instance</span></span>  <br/> |<span data-ttu-id="168bd-166">Weltweit</span><span class="sxs-lookup"><span data-stu-id="168bd-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="168bd-167">Binär (mit Memcmp) vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="168bd-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="168bd-168">Keine Verwendung [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="168bd-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="168bd-169">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-169">Yes</span></span>  <br/> |<span data-ttu-id="168bd-170">Ja</span><span class="sxs-lookup"><span data-stu-id="168bd-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="168bd-171">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="168bd-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="168bd-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="168bd-172">Protocol specifications</span></span>

<span data-ttu-id="168bd-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-174">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="168bd-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="168bd-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-176">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="168bd-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="168bd-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-178">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="168bd-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="168bd-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-180">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="168bd-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="168bd-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-182">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="168bd-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="168bd-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-184">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="168bd-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="168bd-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-186">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="168bd-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="168bd-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="168bd-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="168bd-188">Gibt an, das Schema und die Methoden, die zum Anfordern von Informationen zur Verfügbarkeit für Benutzer und Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="168bd-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="168bd-189">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="168bd-189">Header files</span></span>

<span data-ttu-id="168bd-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="168bd-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="168bd-191">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="168bd-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="168bd-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="168bd-192">Mapitags.h</span></span>
  
> <span data-ttu-id="168bd-193">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="168bd-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="168bd-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="168bd-194">See also</span></span>



[<span data-ttu-id="168bd-195">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="168bd-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="168bd-196">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="168bd-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="168bd-197">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="168bd-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="168bd-198">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="168bd-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="168bd-199">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="168bd-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

