---
title: Kanonische Pidtagrecordkey (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355265"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="18df9-103">Kanonische Pidtagrecordkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="18df9-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="18df9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18df9-105">Enthält einen eindeutigen, Binär-vergleichbaren Bezeichner für ein bestimmtes Objekt.</span><span class="sxs-lookup"><span data-stu-id="18df9-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18df9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18df9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18df9-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="18df9-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="18df9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="18df9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18df9-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="18df9-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="18df9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18df9-110">Data type:</span></span>  <br/> |<span data-ttu-id="18df9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="18df9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="18df9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18df9-112">Area:</span></span>  <br/> |<span data-ttu-id="18df9-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18df9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18df9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18df9-114">Remarks</span></span>

<span data-ttu-id="18df9-115">Diese Eigenschaft erleichtert das Auffinden von Verweisen auf ein Objekt, wie beispielsweise die Suche nach der Zeile in einer Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="18df9-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="18df9-116">Diese Eigenschaft kann nicht zum Öffnen eines Objekts verwendet werden. Verwenden Sie dazu die Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="18df9-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="18df9-117">Ein Attachment-Unterobjekt sollte innerhalb einer Nachricht durch diese Eigenschaft eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="18df9-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="18df9-118">Dieser Bezeichner ist das einzige Anlagen Merkmal, das garantiert bleiben muss, nachdem die Nachricht geschlossen und erneut geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="18df9-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="18df9-119">Der Informationsspeicher Anbieter muss diese Eigenschaft in allen Sitzungen aufbewahren, um diese Garantie sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="18df9-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="18df9-120">Bei Ordnern enthält diese Eigenschaft einen Schlüssel, der in der Ordner Hierarchietabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18df9-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="18df9-121">In der Regel ist dies derselbe Wert wie der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="18df9-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="18df9-122">Für Nachrichtenspeicher ist diese Eigenschaft mit der **PR_STORE_RECORD_KEY** ([pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))-Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="18df9-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="18df9-123">In einem Nachrichtenspeicherobjekt sollte diese Eigenschaft für alle Speicheranbieter eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="18df9-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="18df9-124">Eine Möglichkeit hierfür besteht darin, den Wert der **PR_MDB_PROVIDER** ([pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))-Eigenschaft für den Store (eindeutig für diesen Anbietertyp) mit einer [GUID](guid.md) -Struktur oder einem anderen Wert zu kombinieren, der eindeutig für den jeweiligen Nachrichtenspeicher ist.</span><span class="sxs-lookup"><span data-stu-id="18df9-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="18df9-125">Diese Eigenschaft steht immer über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="18df9-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="18df9-126">Einige Anbieter können diese sofort nach der Instanziierung zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="18df9-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="18df9-127">Ein Client oder Dienstanbieter kann Werte dieser Eigenschaft mithilfe von memcmp vergleichen.</span><span class="sxs-lookup"><span data-stu-id="18df9-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="18df9-128">Dies ist für Eintrags-ID-Werte nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="18df9-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="18df9-129">Diese Eigenschaft ist jedoch garantiert innerhalb desselben Nachrichtenspeichers oder Adressbuch Containers eindeutig. zwei Objekte aus unterschiedlichen Containern können denselben Wert dieser Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18df9-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="18df9-130">Eine Unterscheidung zwischen dem Record-und dem Suchschlüssel besteht darin, dass der Record-Schlüssel spezifisch für das Objekt ist, wohingegen der Suchschlüssel in andere Objekte kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="18df9-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="18df9-131">Beispielsweise können zwei Kopien des Objekts denselben **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Wert aufweisen, aber Sie müssen unterschiedliche Werte für diese Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18df9-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="18df9-132">In der folgenden Tabelle sind wichtige Unterschiede zwischen **PR_ENTRYID**, **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="18df9-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="18df9-133">**Merkmal**</span><span class="sxs-lookup"><span data-stu-id="18df9-133">**Characteristic**</span></span>|<span data-ttu-id="18df9-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="18df9-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="18df9-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="18df9-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="18df9-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="18df9-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18df9-137">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="18df9-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="18df9-138">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-138">No</span></span>  <br/> |<span data-ttu-id="18df9-139">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-139">Yes</span></span>  <br/> |<span data-ttu-id="18df9-140">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-140">No</span></span>  <br/> |
|<span data-ttu-id="18df9-141">Erforderliche Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="18df9-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="18df9-142">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-142">Yes</span></span>  <br/> |<span data-ttu-id="18df9-143">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-143">Yes</span></span>  <br/> |<span data-ttu-id="18df9-144">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-144">No</span></span>  <br/> |
|<span data-ttu-id="18df9-145">Erforderlich für Nachrichtenspeicher Objekte</span><span class="sxs-lookup"><span data-stu-id="18df9-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="18df9-146">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-146">Yes</span></span>  <br/> |<span data-ttu-id="18df9-147">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-147">Yes</span></span>  <br/> |<span data-ttu-id="18df9-148">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-148">No</span></span>  <br/> |
|<span data-ttu-id="18df9-149">Erforderlich für Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="18df9-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="18df9-150">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-150">Yes</span></span>  <br/> |<span data-ttu-id="18df9-151">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-151">No</span></span>  <br/> |<span data-ttu-id="18df9-152">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-152">No</span></span>  <br/> |
|<span data-ttu-id="18df9-153">Erstellbarer Client</span><span class="sxs-lookup"><span data-stu-id="18df9-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="18df9-154">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-154">No</span></span>  <br/> |<span data-ttu-id="18df9-155">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-155">No</span></span>  <br/> |<span data-ttu-id="18df9-156">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-156">Yes</span></span>  <br/> |
|<span data-ttu-id="18df9-157">Verfügbar vor einem Aufruf von **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="18df9-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="18df9-158">Leicht</span><span class="sxs-lookup"><span data-stu-id="18df9-158">Maybe</span></span>  <br/> |<span data-ttu-id="18df9-159">Leicht</span><span class="sxs-lookup"><span data-stu-id="18df9-159">Maybe</span></span>  <br/> |<span data-ttu-id="18df9-160">Nachrichten ja andere vielleicht</span><span class="sxs-lookup"><span data-stu-id="18df9-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="18df9-161">Geändert in einem Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="18df9-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="18df9-162">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-162">Yes</span></span>  <br/> |<span data-ttu-id="18df9-163">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-163">Yes</span></span>  <br/> |<span data-ttu-id="18df9-164">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-164">No</span></span>  <br/> |
|<span data-ttu-id="18df9-165">Von einem Client nach einer Kopie änderbar</span><span class="sxs-lookup"><span data-stu-id="18df9-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="18df9-166">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-166">No</span></span>  <br/> |<span data-ttu-id="18df9-167">Nein</span><span class="sxs-lookup"><span data-stu-id="18df9-167">No</span></span>  <br/> |<span data-ttu-id="18df9-168">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-168">Yes</span></span>  <br/> |
|<span data-ttu-id="18df9-169">Innerhalb von...</span><span class="sxs-lookup"><span data-stu-id="18df9-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="18df9-170">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="18df9-170">Entire world</span></span>  <br/> |<span data-ttu-id="18df9-171">Anbieterinstanz</span><span class="sxs-lookup"><span data-stu-id="18df9-171">Provider instance</span></span>  <br/> |<span data-ttu-id="18df9-172">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="18df9-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="18df9-173">Vergleichbare Binärdatei (wie bei memcmp)</span><span class="sxs-lookup"><span data-stu-id="18df9-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="18df9-174">No--verwenden Sie **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="18df9-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="18df9-175">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-175">Yes</span></span>  <br/> |<span data-ttu-id="18df9-176">Ja</span><span class="sxs-lookup"><span data-stu-id="18df9-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="18df9-177">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18df9-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18df9-178">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18df9-178">Protocol specifications</span></span>

<span data-ttu-id="18df9-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18df9-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18df9-180">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18df9-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18df9-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18df9-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18df9-182">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="18df9-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="18df9-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18df9-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18df9-184">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="18df9-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18df9-185">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="18df9-185">Header files</span></span>

<span data-ttu-id="18df9-186">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="18df9-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="18df9-187">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="18df9-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="18df9-188">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="18df9-188">Mapitags.h</span></span>
  
> <span data-ttu-id="18df9-189">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="18df9-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18df9-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18df9-190">See also</span></span>



[<span data-ttu-id="18df9-191">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18df9-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18df9-192">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18df9-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18df9-193">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18df9-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18df9-194">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18df9-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

