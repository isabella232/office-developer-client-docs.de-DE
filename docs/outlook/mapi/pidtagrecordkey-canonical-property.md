---
title: PidTagRecordKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9add9246cdfb22f7c5ad579f425932f49d4a9ecd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581244"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="7197c-103">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7197c-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="7197c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7197c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7197c-105">Enthält einen binären vergleichbaren eindeutigen Bezeichner für ein bestimmtes Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7197c-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7197c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7197c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7197c-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="7197c-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="7197c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7197c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7197c-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="7197c-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="7197c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7197c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7197c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7197c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7197c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7197c-112">Area:</span></span>  <br/> |<span data-ttu-id="7197c-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7197c-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7197c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7197c-114">Remarks</span></span>

<span data-ttu-id="7197c-115">Diese Eigenschaft erleichtert das Auffinden Verweise auf ein Objekt, wie eine Zeile in einer Inhaltstabelle suchen.</span><span class="sxs-lookup"><span data-stu-id="7197c-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="7197c-116">Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. Verwenden Sie die Eintrags-ID für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="7197c-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="7197c-117">Eine Anlage Unterobjekts sollten innerhalb einer Nachricht von dieser Eigenschaft eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7197c-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="7197c-118">Dieser Bezeichner ist das einzige Anlage Merkmal garantiert gleich bleiben, nachdem die Meldung geschlossen und erneut geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7197c-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="7197c-119">Der Anbieter muss diese Eigenschaft in allen Sitzungen, um sicherzustellen, dass diese Garantie beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7197c-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="7197c-120">Für Ordner enthält diese Eigenschaft einen Schlüssel in der Ordner-Hierarchie-Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="7197c-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="7197c-121">In der Regel ist dies den gleichen Wert wie, die durch die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7197c-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7197c-122">Für Nachrichtenspeicher ist diese Eigenschaft der **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))-Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="7197c-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7197c-123">In einem Message Store-Objekt sollten diese Eigenschaft für alle Anbieter eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7197c-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="7197c-124">Eine Möglichkeit, dies ist den Wert der Eigenschaft **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) für den Speicher (eindeutig für diesen Anbietertyp) mit einer [GUID](guid.md) -Struktur oder einen anderen Wert für den bestimmten Nachrichtenspeicher eindeutig zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7197c-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="7197c-125">Diese Eigenschaft ist immer über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7197c-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="7197c-126">Einige Anbieter können sie sofort nach der Instanziierung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7197c-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="7197c-127">Ein Client oder Dienstanbieter kann Werte aus dieser Eigenschaft mithilfe von Memcmp vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7197c-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="7197c-128">Dies ist nicht möglich, für die Eintrags-ID-Werte.</span><span class="sxs-lookup"><span data-stu-id="7197c-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="7197c-129">Jedoch ist diese Eigenschaft Sicherheit innerhalb der gleichen Nachrichtenspeicher eindeutig sein oder address Book Container. zwei Objekte aus unterschiedlichen Containern können den gleichen Wert dieser Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7197c-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="7197c-130">Eine Unterscheidung zwischen den Schlüsseln Datensatz, und suchen Sie ist, dass der Datensatzschlüssel speziell für das Objekt ist, während die suchen-Taste auf andere Objekte kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7197c-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="7197c-131">Beispielsweise zwei Kopien des Objekts können den gleichen Wert **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) haben jedoch unterschiedliche Werte für diese Eigenschaft aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="7197c-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="7197c-132">In der folgenden Tabelle werden die wichtigen Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) und diese Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="7197c-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="7197c-133">**Merkmale**</span><span class="sxs-lookup"><span data-stu-id="7197c-133">**Characteristic**</span></span>|<span data-ttu-id="7197c-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="7197c-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="7197c-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="7197c-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="7197c-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="7197c-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7197c-137">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="7197c-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="7197c-138">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-138">No</span></span>  <br/> |<span data-ttu-id="7197c-139">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-139">Yes</span></span>  <br/> |<span data-ttu-id="7197c-140">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-140">No</span></span>  <br/> |
|<span data-ttu-id="7197c-141">Auf Ordnerobjekten erforderlich</span><span class="sxs-lookup"><span data-stu-id="7197c-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="7197c-142">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-142">Yes</span></span>  <br/> |<span data-ttu-id="7197c-143">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-143">Yes</span></span>  <br/> |<span data-ttu-id="7197c-144">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-144">No</span></span>  <br/> |
|<span data-ttu-id="7197c-145">Erforderlich für Nachricht Store-Objekte</span><span class="sxs-lookup"><span data-stu-id="7197c-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="7197c-146">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-146">Yes</span></span>  <br/> |<span data-ttu-id="7197c-147">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-147">Yes</span></span>  <br/> |<span data-ttu-id="7197c-148">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-148">No</span></span>  <br/> |
|<span data-ttu-id="7197c-149">Klicken Sie auf Status Objekte erforderlich</span><span class="sxs-lookup"><span data-stu-id="7197c-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="7197c-150">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-150">Yes</span></span>  <br/> |<span data-ttu-id="7197c-151">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-151">No</span></span>  <br/> |<span data-ttu-id="7197c-152">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-152">No</span></span>  <br/> |
|<span data-ttu-id="7197c-153">Vom Client erstellbare</span><span class="sxs-lookup"><span data-stu-id="7197c-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="7197c-154">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-154">No</span></span>  <br/> |<span data-ttu-id="7197c-155">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-155">No</span></span>  <br/> |<span data-ttu-id="7197c-156">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-156">Yes</span></span>  <br/> |
|<span data-ttu-id="7197c-157">Vor einem Aufruf von **SaveChanges** verfügbar</span><span class="sxs-lookup"><span data-stu-id="7197c-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="7197c-158">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="7197c-158">Maybe</span></span>  <br/> |<span data-ttu-id="7197c-159">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="7197c-159">Maybe</span></span>  <br/> |<span data-ttu-id="7197c-160">Nachrichten Ja andere vielleicht</span><span class="sxs-lookup"><span data-stu-id="7197c-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="7197c-161">Geändert in einen Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="7197c-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="7197c-162">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-162">Yes</span></span>  <br/> |<span data-ttu-id="7197c-163">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-163">Yes</span></span>  <br/> |<span data-ttu-id="7197c-164">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-164">No</span></span>  <br/> |
|<span data-ttu-id="7197c-165">Von einem Client beim Kopieren eines veränderbar</span><span class="sxs-lookup"><span data-stu-id="7197c-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="7197c-166">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-166">No</span></span>  <br/> |<span data-ttu-id="7197c-167">Nein</span><span class="sxs-lookup"><span data-stu-id="7197c-167">No</span></span>  <br/> |<span data-ttu-id="7197c-168">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-168">Yes</span></span>  <br/> |
|<span data-ttu-id="7197c-169">Unique innerhalb...</span><span class="sxs-lookup"><span data-stu-id="7197c-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="7197c-170">Weltweit</span><span class="sxs-lookup"><span data-stu-id="7197c-170">Entire world</span></span>  <br/> |<span data-ttu-id="7197c-171">Providerinstanz</span><span class="sxs-lookup"><span data-stu-id="7197c-171">Provider instance</span></span>  <br/> |<span data-ttu-id="7197c-172">Weltweit</span><span class="sxs-lookup"><span data-stu-id="7197c-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="7197c-173">Binär (mit Memcmp) vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="7197c-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="7197c-174">Nein – verwenden Sie **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="7197c-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="7197c-175">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-175">Yes</span></span>  <br/> |<span data-ttu-id="7197c-176">Ja</span><span class="sxs-lookup"><span data-stu-id="7197c-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7197c-177">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7197c-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7197c-178">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7197c-178">Protocol specifications</span></span>

<span data-ttu-id="7197c-179">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7197c-179">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7197c-180">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7197c-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7197c-181">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7197c-181">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7197c-182">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="7197c-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7197c-183">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7197c-183">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7197c-184">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7197c-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7197c-185">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7197c-185">Header files</span></span>

<span data-ttu-id="7197c-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7197c-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="7197c-187">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7197c-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="7197c-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7197c-188">Mapitags.h</span></span>
  
> <span data-ttu-id="7197c-189">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7197c-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7197c-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7197c-190">See also</span></span>



[<span data-ttu-id="7197c-191">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7197c-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7197c-192">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7197c-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7197c-193">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7197c-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7197c-194">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7197c-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

