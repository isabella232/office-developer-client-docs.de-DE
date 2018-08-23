---
title: PidTagSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595391"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="39cec-103">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="39cec-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="39cec-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39cec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39cec-105">Enthält einen binären vergleichbaren Schlüssel, der für eine Suche korrelierte Objekte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39cec-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39cec-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="39cec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39cec-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="39cec-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="39cec-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="39cec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39cec-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="39cec-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="39cec-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="39cec-110">Data type:</span></span>  <br/> |<span data-ttu-id="39cec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39cec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39cec-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="39cec-112">Area:</span></span>  <br/> |<span data-ttu-id="39cec-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39cec-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39cec-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="39cec-114">Remarks</span></span>

<span data-ttu-id="39cec-115">Diese Eigenschaft bietet eine Verfolgung für verknüpfte Objekte, wie Nachrichtenkopien, und suchen unerwünschte vorkommen, wie etwa doppelte Empfänger erleichtert.</span><span class="sxs-lookup"><span data-stu-id="39cec-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="39cec-116">MAPI verwendet spezielle Regeln zum Erstellen von Search-Schlüssel für Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="39cec-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="39cec-117">Die suchen-Taste wird durch Verketten den Adresstyp (in Großbuchstaben) gebildet Doppelpunkt ":", die e-Mail-Adresse in kanonische Form und abschließendes Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="39cec-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="39cec-118">Kanonische Form hier bedeutet, dass die Groß-/Kleinschreibung beachtet Adressen werden in die Groß-/Kleinschreibung angezeigt und Adressen, die Groß-/ nicht Kleinschreibung in Großbuchstaben umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="39cec-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="39cec-119">Dies ist wichtig, können Sie die Korrelation zwischen Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39cec-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="39cec-120">Für die Message-Objekte ist diese Eigenschaft über die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode unmittelbar nach Erstellung der Nachricht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39cec-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="39cec-121">Bei anderen Objekten ist es nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39cec-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="39cec-122">Da diese Eigenschaft schreibgeschützt ist, ist es unzuverlässig über **GetProps** erhalten, bis das Gespräch **SaveChanges** Commit für alle Werte festgelegt oder geändert werden, von der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="39cec-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="39cec-123">Für Profile stellt MAPI auch einen hartcodiert und Profilabschnitt mit dem Namen **MUID_PROFILE_INSTANCE**, und diese Eigenschaft als ihre einzige Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="39cec-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="39cec-124">Dieser Schlüssel ist sichergestellt, dass für alle Profile jemals erstellten eindeutig sein und dürfen zuverlässiger als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die kann, beispielsweise gelöscht und neu erstellt, mit dem gleichen Namen.</span><span class="sxs-lookup"><span data-stu-id="39cec-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="39cec-125">In der folgenden Tabelle werden die wichtigen Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und diese Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="39cec-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="39cec-126">**Merkmale**</span><span class="sxs-lookup"><span data-stu-id="39cec-126">**Characteristic**</span></span>|<span data-ttu-id="39cec-127">PR_ENTRYID \*\*\*</span><span class="sxs-lookup"><span data-stu-id="39cec-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="39cec-128">PR_RECORD_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="39cec-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="39cec-129">PR_SEARCH_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="39cec-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39cec-130">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="39cec-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="39cec-131">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-131">No</span></span>  <br/> |<span data-ttu-id="39cec-132">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-132">Yes</span></span>  <br/> |<span data-ttu-id="39cec-133">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-133">No</span></span>  <br/> |
|<span data-ttu-id="39cec-134">Auf Ordnerobjekten erforderlich</span><span class="sxs-lookup"><span data-stu-id="39cec-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="39cec-135">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-135">Yes</span></span>  <br/> |<span data-ttu-id="39cec-136">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-136">Yes</span></span>  <br/> |<span data-ttu-id="39cec-137">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-137">No</span></span>  <br/> |
|<span data-ttu-id="39cec-138">Erforderlich für Nachricht Store-Objekte</span><span class="sxs-lookup"><span data-stu-id="39cec-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="39cec-139">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-139">Yes</span></span>  <br/> |<span data-ttu-id="39cec-140">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-140">Yes</span></span>  <br/> |<span data-ttu-id="39cec-141">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-141">No</span></span>  <br/> |
|<span data-ttu-id="39cec-142">Klicken Sie auf Status Objekte erforderlich</span><span class="sxs-lookup"><span data-stu-id="39cec-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="39cec-143">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-143">Yes</span></span>  <br/> |<span data-ttu-id="39cec-144">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-144">No</span></span>  <br/> |<span data-ttu-id="39cec-145">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-145">No</span></span>  <br/> |
|<span data-ttu-id="39cec-146">Vom Client erstellbare</span><span class="sxs-lookup"><span data-stu-id="39cec-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="39cec-147">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-147">No</span></span>  <br/> |<span data-ttu-id="39cec-148">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-148">No</span></span>  <br/> |<span data-ttu-id="39cec-149">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-149">Yes</span></span>  <br/> |
|<span data-ttu-id="39cec-150">Bevor Sie **SaveChanges** verfügbar</span><span class="sxs-lookup"><span data-stu-id="39cec-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="39cec-151">Je nach anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="39cec-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="39cec-152">Je nach anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="39cec-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="39cec-153">Für Nachrichten, Ja.</span><span class="sxs-lookup"><span data-stu-id="39cec-153">For messages, Yes.</span></span> <span data-ttu-id="39cec-154">Für andere hängt die Implementierung des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="39cec-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="39cec-155">Geändert in einen Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="39cec-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="39cec-156">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-156">Yes</span></span>  <br/> |<span data-ttu-id="39cec-157">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-157">Yes</span></span>  <br/> |<span data-ttu-id="39cec-158">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-158">No</span></span>  <br/> |
|<span data-ttu-id="39cec-159">Vom Client beim Kopieren eines veränderbar</span><span class="sxs-lookup"><span data-stu-id="39cec-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="39cec-160">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-160">No</span></span>  <br/> |<span data-ttu-id="39cec-161">Nein</span><span class="sxs-lookup"><span data-stu-id="39cec-161">No</span></span>  <br/> |<span data-ttu-id="39cec-162">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-162">Yes</span></span>  <br/> |
|<span data-ttu-id="39cec-163">Unique innerhalb...</span><span class="sxs-lookup"><span data-stu-id="39cec-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="39cec-164">Weltweit</span><span class="sxs-lookup"><span data-stu-id="39cec-164">Entire world</span></span>  <br/> |<span data-ttu-id="39cec-165">Providerinstanz</span><span class="sxs-lookup"><span data-stu-id="39cec-165">Provider instance</span></span>  <br/> |<span data-ttu-id="39cec-166">Weltweit</span><span class="sxs-lookup"><span data-stu-id="39cec-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="39cec-167">Binär (mit Memcmp) vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="39cec-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="39cec-168">Nein – [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) verwenden</span><span class="sxs-lookup"><span data-stu-id="39cec-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="39cec-169">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-169">Yes</span></span>  <br/> |<span data-ttu-id="39cec-170">Ja</span><span class="sxs-lookup"><span data-stu-id="39cec-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="39cec-171">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39cec-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39cec-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="39cec-172">Protocol specifications</span></span>

<span data-ttu-id="39cec-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39cec-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39cec-174">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="39cec-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39cec-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39cec-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39cec-176">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="39cec-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="39cec-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39cec-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39cec-178">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="39cec-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39cec-179">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="39cec-179">Header files</span></span>

<span data-ttu-id="39cec-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39cec-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="39cec-181">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="39cec-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="39cec-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39cec-182">Mapitags.h</span></span>
  
> <span data-ttu-id="39cec-183">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="39cec-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39cec-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39cec-184">See also</span></span>



[<span data-ttu-id="39cec-185">PidTagResponsibility (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="39cec-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="39cec-186">PidTagStoreRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="39cec-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="39cec-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39cec-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39cec-188">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39cec-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39cec-189">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="39cec-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39cec-190">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="39cec-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

