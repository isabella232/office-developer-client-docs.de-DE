---
title: Kanonische PidTagEntryId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328588"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="cb413-103">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb413-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cb413-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb413-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb413-105">Enthält eine MAPI-Eintrags-ID zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb413-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb413-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cb413-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb413-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cb413-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cb413-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cb413-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb413-109">0X0fff dar</span><span class="sxs-lookup"><span data-stu-id="cb413-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="cb413-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cb413-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb413-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb413-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb413-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cb413-112">Area:</span></span>  <br/> |<span data-ttu-id="cb413-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb413-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb413-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb413-114">Remarks</span></span>

<span data-ttu-id="cb413-115">Diese Eigenschaft identifiziert ein Objekt für **OpenEntry** zum Instanziieren und ermöglicht den Zugriff auf alle Eigenschaften über die entsprechende abgeleitete Schnittstelle von **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="cb413-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="cb413-116">Diese Eigenschaft ist eine der Basis Adresseigenschaften für alle Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="cb413-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="cb413-117">Diese Eigenschaft kann einen langfristigen oder einen kurzfristigen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb413-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="cb413-118">Kurzfristige Bezeichner sind einfacher und schneller zu konstruieren, sind jedoch in ihrem Umfang und ihrer Dauer begrenzt, in der Regel für die aktuelle Sitzung und Workstation.</span><span class="sxs-lookup"><span data-stu-id="cb413-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="cb413-119">Sie werden häufig für Objekte temporärer Art wie Tabellenzeilen oder Dialogfeld Einträge verwendet und dann abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cb413-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="cb413-120">Langfristige Bezeichner werden für Objekte mit einer breiteren und langlebigen Art verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb413-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="cb413-121">Diese Eigenschaft steht immer über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cb413-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="cb413-122">Einige Dienstanbieter können diese sofort nach der Instanziierung zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="cb413-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="cb413-123">Der Anbieter muss immer eine langfristige Eintrags-ID aus \*\*\*\* GetProps zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cb413-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="cb413-124">Um einen kurzfristigen Bezeichner zu langfristig zu konvertieren, öffnen Sie daher einfach das Objekt, und rufen Sie dessen this-Eigenschaft \*\*\*\* über GetProps ab.</span><span class="sxs-lookup"><span data-stu-id="cb413-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="cb413-125">In der folgenden Tabelle sind wichtige Unterschiede zwischen dieser Eigenschaft, **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="cb413-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="cb413-126">**Merkmal**</span><span class="sxs-lookup"><span data-stu-id="cb413-126">**Characteristic**</span></span>|<span data-ttu-id="cb413-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="cb413-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="cb413-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="cb413-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="cb413-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="cb413-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb413-130">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="cb413-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="cb413-131">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-131">No</span></span>  <br/> |<span data-ttu-id="cb413-132">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-132">Yes</span></span>  <br/> |<span data-ttu-id="cb413-133">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-133">No</span></span>  <br/> |
|<span data-ttu-id="cb413-134">Erforderliche Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="cb413-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="cb413-135">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-135">Yes</span></span>  <br/> |<span data-ttu-id="cb413-136">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-136">Yes</span></span>  <br/> |<span data-ttu-id="cb413-137">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-137">No</span></span>  <br/> |
|<span data-ttu-id="cb413-138">Erforderlich für Nachrichtenspeicher Objekte</span><span class="sxs-lookup"><span data-stu-id="cb413-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="cb413-139">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-139">Yes</span></span>  <br/> |<span data-ttu-id="cb413-140">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-140">Yes</span></span>  <br/> |<span data-ttu-id="cb413-141">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-141">No</span></span>  <br/> |
|<span data-ttu-id="cb413-142">Erforderlich für Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="cb413-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="cb413-143">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-143">Yes</span></span>  <br/> |<span data-ttu-id="cb413-144">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-144">No</span></span>  <br/> |<span data-ttu-id="cb413-145">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-145">No</span></span>  <br/> |
|<span data-ttu-id="cb413-146">Erstellt von Client</span><span class="sxs-lookup"><span data-stu-id="cb413-146">Created by client</span></span>  <br/> |<span data-ttu-id="cb413-147">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-147">No</span></span>  <br/> |<span data-ttu-id="cb413-148">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-148">No</span></span>  <br/> |<span data-ttu-id="cb413-149">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-149">Yes</span></span>  <br/> |
|<span data-ttu-id="cb413-150">Verfügbar vor dem Aufruf \*\*\*\* von SaveChanges</span><span class="sxs-lookup"><span data-stu-id="cb413-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="cb413-151">Abhängig von der Anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="cb413-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="cb413-152">Abhängig von der Anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="cb413-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="cb413-153">Für Nachrichten, ja.</span><span class="sxs-lookup"><span data-stu-id="cb413-153">For messages, Yes.</span></span> <span data-ttu-id="cb413-154">Für andere ist abhängig von der Anbieterimplementierung.</span><span class="sxs-lookup"><span data-stu-id="cb413-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="cb413-155">Geändert in einem Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="cb413-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="cb413-156">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-156">Yes</span></span>  <br/> |<span data-ttu-id="cb413-157">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-157">Yes</span></span>  <br/> |<span data-ttu-id="cb413-158">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-158">No</span></span>  <br/> |
|<span data-ttu-id="cb413-159">Nach einer Kopie nach dem Client änderbar</span><span class="sxs-lookup"><span data-stu-id="cb413-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="cb413-160">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-160">No</span></span>  <br/> |<span data-ttu-id="cb413-161">Nein</span><span class="sxs-lookup"><span data-stu-id="cb413-161">No</span></span>  <br/> |<span data-ttu-id="cb413-162">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-162">Yes</span></span>  <br/> |
|<span data-ttu-id="cb413-163">Eindeutig innerhalb</span><span class="sxs-lookup"><span data-stu-id="cb413-163">Unique within</span></span>  <br/> |<span data-ttu-id="cb413-164">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="cb413-164">Entire world</span></span>  <br/> |<span data-ttu-id="cb413-165">Anbieterinstanz</span><span class="sxs-lookup"><span data-stu-id="cb413-165">Provider instance</span></span>  <br/> |<span data-ttu-id="cb413-166">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="cb413-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="cb413-167">Vergleichbare Binärdatei (wie bei memcmp)</span><span class="sxs-lookup"><span data-stu-id="cb413-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="cb413-168">Keine Verwendung [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="cb413-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="cb413-169">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-169">Yes</span></span>  <br/> |<span data-ttu-id="cb413-170">Ja</span><span class="sxs-lookup"><span data-stu-id="cb413-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cb413-171">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cb413-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb413-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cb413-172">Protocol specifications</span></span>

<span data-ttu-id="cb413-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-174">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cb413-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb413-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-176">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="cb413-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cb413-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-178">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="cb413-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="cb413-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-180">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="cb413-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="cb413-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-182">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="cb413-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="cb413-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-184">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="cb413-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="cb413-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-186">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="cb413-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cb413-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb413-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb413-188">Gibt das Schema und die Methoden an, die zum Anfordern von Verfügbarkeitsinformationen für Benutzer und Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb413-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb413-189">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cb413-189">Header files</span></span>

<span data-ttu-id="cb413-190">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cb413-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb413-191">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cb413-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb413-192">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cb413-192">Mapitags.h</span></span>
  
> <span data-ttu-id="cb413-193">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cb413-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb413-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb413-194">See also</span></span>



[<span data-ttu-id="cb413-195">Kanonische Pidtagstoreentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb413-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="cb413-196">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb413-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb413-197">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb413-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb413-198">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cb413-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb413-199">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cb413-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

