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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387790"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="d7fe7-103">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d7fe7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7fe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7fe7-105">Enthält eine MAPI-Eintrags-ID, die zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7fe7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d7fe7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7fe7-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d7fe7-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d7fe7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d7fe7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7fe7-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="d7fe7-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="d7fe7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d7fe7-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7fe7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7fe7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7fe7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d7fe7-112">Area:</span></span>  <br/> |<span data-ttu-id="d7fe7-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7fe7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7fe7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7fe7-114">Remarks</span></span>

<span data-ttu-id="d7fe7-115">Diese Eigenschaft gibt ein Objekt für **OpenEntry** zum Instanziieren und ermöglicht den Zugriff auf alle seine Eigenschaften über die entsprechenden abgeleiteten Schnittstelle des **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="d7fe7-116">Diese Eigenschaft ist eine der Eigenschaften für alle Benutzer messaging Basisadresse.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="d7fe7-117">Diese Eigenschaft kann eine langfristige oder einen kurzfristigen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="d7fe7-118">Kurzfristige Bezeichner sind schneller und einfacher, Konstrukt, aber in deren Bereich und die Dauer, in der Regel auf der aktuellen Sitzung und Arbeitsstation beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="d7fe7-119">Sie sind häufig verwendet, um Objekte vorübergehender Art, wie Zeilen der Tabelle oder Einträgen im Dialogfeld, und klicken Sie dann abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="d7fe7-120">Langfristige-IDs werden für eine umfassende und langfristig Art-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="d7fe7-121">Diese Eigenschaft ist immer über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="d7fe7-122">Einige Dienstanbieter können sie sofort nach der Instanziierung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="d7fe7-123">Der Anbieter muss immer eine langfristige Eintrags-ID aus **GetProps**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="d7fe7-124">Aus diesem Grund um einen kurzfristigen Bezeichner in langfristige konvertieren, einfach öffnen Sie das Objekt und seine dies abrufen-Eigenschaft über **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="d7fe7-125">In der folgenden Tabelle werden wichtige Unterschiede zwischen den diese Eigenschaft **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="d7fe7-126">**Merkmale**</span><span class="sxs-lookup"><span data-stu-id="d7fe7-126">**Characteristic**</span></span>|<span data-ttu-id="d7fe7-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="d7fe7-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="d7fe7-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="d7fe7-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="d7fe7-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="d7fe7-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7fe7-130">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="d7fe7-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="d7fe7-131">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-131">No</span></span>  <br/> |<span data-ttu-id="d7fe7-132">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-132">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-133">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-133">No</span></span>  <br/> |
|<span data-ttu-id="d7fe7-134">Auf Ordnerobjekten erforderlich</span><span class="sxs-lookup"><span data-stu-id="d7fe7-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="d7fe7-135">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-135">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-136">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-136">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-137">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-137">No</span></span>  <br/> |
|<span data-ttu-id="d7fe7-138">Erforderlich für Nachricht Store-Objekte</span><span class="sxs-lookup"><span data-stu-id="d7fe7-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="d7fe7-139">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-139">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-140">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-140">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-141">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-141">No</span></span>  <br/> |
|<span data-ttu-id="d7fe7-142">Klicken Sie auf Status Objekte erforderlich</span><span class="sxs-lookup"><span data-stu-id="d7fe7-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="d7fe7-143">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-143">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-144">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-144">No</span></span>  <br/> |<span data-ttu-id="d7fe7-145">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-145">No</span></span>  <br/> |
|<span data-ttu-id="d7fe7-146">Vom Client erstellt</span><span class="sxs-lookup"><span data-stu-id="d7fe7-146">Created by client</span></span>  <br/> |<span data-ttu-id="d7fe7-147">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-147">No</span></span>  <br/> |<span data-ttu-id="d7fe7-148">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-148">No</span></span>  <br/> |<span data-ttu-id="d7fe7-149">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-149">Yes</span></span>  <br/> |
|<span data-ttu-id="d7fe7-150">Vor dem Aufruf von **SaveChanges** verfügbar</span><span class="sxs-lookup"><span data-stu-id="d7fe7-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="d7fe7-151">Hängt vom anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="d7fe7-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="d7fe7-152">Hängt vom anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="d7fe7-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="d7fe7-153">Für Nachrichten, Ja.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-153">For messages, Yes.</span></span> <span data-ttu-id="d7fe7-154">Für andere hängt von anbieterimplementierung.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="d7fe7-155">Geändert in einen Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="d7fe7-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="d7fe7-156">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-156">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-157">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-157">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-158">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-158">No</span></span>  <br/> |
|<span data-ttu-id="d7fe7-159">Vom Client beim Kopieren eines veränderbar</span><span class="sxs-lookup"><span data-stu-id="d7fe7-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="d7fe7-160">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-160">No</span></span>  <br/> |<span data-ttu-id="d7fe7-161">Nein</span><span class="sxs-lookup"><span data-stu-id="d7fe7-161">No</span></span>  <br/> |<span data-ttu-id="d7fe7-162">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-162">Yes</span></span>  <br/> |
|<span data-ttu-id="d7fe7-163">Innerhalb eindeutig</span><span class="sxs-lookup"><span data-stu-id="d7fe7-163">Unique within</span></span>  <br/> |<span data-ttu-id="d7fe7-164">Weltweit</span><span class="sxs-lookup"><span data-stu-id="d7fe7-164">Entire world</span></span>  <br/> |<span data-ttu-id="d7fe7-165">Providerinstanz</span><span class="sxs-lookup"><span data-stu-id="d7fe7-165">Provider instance</span></span>  <br/> |<span data-ttu-id="d7fe7-166">Weltweit</span><span class="sxs-lookup"><span data-stu-id="d7fe7-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="d7fe7-167">Binär (mit Memcmp) vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="d7fe7-168">Keine Verwendung [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="d7fe7-169">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-169">Yes</span></span>  <br/> |<span data-ttu-id="d7fe7-170">Ja</span><span class="sxs-lookup"><span data-stu-id="d7fe7-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d7fe7-171">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d7fe7-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7fe7-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d7fe7-172">Protocol specifications</span></span>

<span data-ttu-id="d7fe7-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-174">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7fe7-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-176">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d7fe7-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-178">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="d7fe7-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-180">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d7fe7-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-182">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d7fe7-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-184">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="d7fe7-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-186">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="d7fe7-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7fe7-188">Gibt an, das Schema und die Methoden, die zum Anfordern von Informationen zur Verfügbarkeit für Benutzer und Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7fe7-189">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d7fe7-189">Header files</span></span>

<span data-ttu-id="d7fe7-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7fe7-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7fe7-191">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7fe7-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7fe7-192">Mapitags.h</span></span>
  
> <span data-ttu-id="d7fe7-193">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7fe7-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7fe7-194">See also</span></span>



[<span data-ttu-id="d7fe7-195">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d7fe7-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="d7fe7-196">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7fe7-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7fe7-197">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7fe7-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7fe7-198">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d7fe7-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7fe7-199">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d7fe7-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

