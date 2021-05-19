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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345465"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="a8ca5-103">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a8ca5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8ca5-105">Enthält einen binär-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ca5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a8ca5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8ca5-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a8ca5-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a8ca5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a8ca5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8ca5-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="a8ca5-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="a8ca5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a8ca5-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8ca5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a8ca5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a8ca5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a8ca5-112">Area:</span></span>  <br/> |<span data-ttu-id="a8ca5-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8ca5-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8ca5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8ca5-114">Remarks</span></span>

<span data-ttu-id="a8ca5-115">Diese Eigenschaft bietet eine Ablaufverfolgung für verwandte Objekte, z. B. Nachrichtenkopien, und erleichtert die Suche nach unerwünschten Vorkommen, z. B. doppelten Empfängern.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="a8ca5-116">MAPI verwendet bestimmte Regeln zum Erstellen von Suchschlüsseln für Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="a8ca5-117">Der Suchschlüssel wird durch Verkettung des Adresstyps (in Großbuchstaben), des Doppelpunktzeichens ":", der E-Mail-Adresse in kanonischer Form und des beendenden Nullzeichens gebildet.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="a8ca5-118">Das kanonische Formular bedeutet hier, dass groß-/kleinschreibungssensitive Adressen im richtigen Fall angezeigt werden, und Adressen, die nicht groß-/kleinschreibungsempfindlich sind, werden in Großbuchstaben konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="a8ca5-119">Dies ist wichtig, um Korrelationen zwischen Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="a8ca5-120">Für Nachrichtenobjekte steht diese Eigenschaft über die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) unmittelbar nach der Nachrichtenerstellung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="a8ca5-121">Für andere Objekte steht sie nach dem ersten Aufruf der [IMAPIProp::SaveChanges-Methode zur](imapiprop-savechanges.md) Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="a8ca5-122">Da diese Eigenschaft änderbar ist, ist es unzuverlässig, sie über **GetProps** zu erhalten, bis ein **SaveChanges-Aufruf** werte festgelegt oder von der [IMAPIProp::SetProps-Methode geändert](imapiprop-setprops.md) hat.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="a8ca5-123">Für Profile bietet MAPI auch einen hart codierten Profilabschnitt namens **MUID_PROFILE_INSTANCE**, mit dieser Eigenschaft als einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="a8ca5-124">Dieser Schlüssel ist unter allen profilen, die jemals erstellt wurden, eindeutig und kann zuverlässiger sein als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die beispielsweise gelöscht und mit demselben Namen neu erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="a8ca5-125">In der folgenden Tabelle werden wichtige Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="a8ca5-126">**Merkmal**</span><span class="sxs-lookup"><span data-stu-id="a8ca5-126">**Characteristic**</span></span>|<span data-ttu-id="a8ca5-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a8ca5-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="a8ca5-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a8ca5-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="a8ca5-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a8ca5-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8ca5-130">Erforderlich für Anlagenobjekte</span><span class="sxs-lookup"><span data-stu-id="a8ca5-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="a8ca5-131">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-131">No</span></span>  <br/> |<span data-ttu-id="a8ca5-132">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-132">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-133">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-133">No</span></span>  <br/> |
|<span data-ttu-id="a8ca5-134">Erforderlich für Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="a8ca5-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="a8ca5-135">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-135">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-136">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-136">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-137">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-137">No</span></span>  <br/> |
|<span data-ttu-id="a8ca5-138">Erforderlich für Nachrichtenspeicherobjekte</span><span class="sxs-lookup"><span data-stu-id="a8ca5-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="a8ca5-139">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-139">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-140">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-140">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-141">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-141">No</span></span>  <br/> |
|<span data-ttu-id="a8ca5-142">Erforderlich für Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="a8ca5-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="a8ca5-143">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-143">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-144">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-144">No</span></span>  <br/> |<span data-ttu-id="a8ca5-145">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-145">No</span></span>  <br/> |
|<span data-ttu-id="a8ca5-146">Nach Client anknabel</span><span class="sxs-lookup"><span data-stu-id="a8ca5-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="a8ca5-147">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-147">No</span></span>  <br/> |<span data-ttu-id="a8ca5-148">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-148">No</span></span>  <br/> |<span data-ttu-id="a8ca5-149">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-149">Yes</span></span>  <br/> |
|<span data-ttu-id="a8ca5-150">Verfügbar vor **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="a8ca5-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="a8ca5-151">Hängt von der Anbieterimplementierung ab</span><span class="sxs-lookup"><span data-stu-id="a8ca5-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="a8ca5-152">Hängt von der Anbieterimplementierung ab</span><span class="sxs-lookup"><span data-stu-id="a8ca5-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="a8ca5-153">Bei Nachrichten ja.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-153">For messages, Yes.</span></span> <span data-ttu-id="a8ca5-154">Für andere hängt es von der Anbieterimplementierung ab.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="a8ca5-155">In einem Kopiervorgang geändert</span><span class="sxs-lookup"><span data-stu-id="a8ca5-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="a8ca5-156">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-156">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-157">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-157">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-158">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-158">No</span></span>  <br/> |
|<span data-ttu-id="a8ca5-159">Vom Client nach einer Kopie ändernd</span><span class="sxs-lookup"><span data-stu-id="a8ca5-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="a8ca5-160">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-160">No</span></span>  <br/> |<span data-ttu-id="a8ca5-161">Nein</span><span class="sxs-lookup"><span data-stu-id="a8ca5-161">No</span></span>  <br/> |<span data-ttu-id="a8ca5-162">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-162">Yes</span></span>  <br/> |
|<span data-ttu-id="a8ca5-163">Eindeutig in ...</span><span class="sxs-lookup"><span data-stu-id="a8ca5-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="a8ca5-164">Gesamte Welt</span><span class="sxs-lookup"><span data-stu-id="a8ca5-164">Entire world</span></span>  <br/> |<span data-ttu-id="a8ca5-165">Anbieterinstanz</span><span class="sxs-lookup"><span data-stu-id="a8ca5-165">Provider instance</span></span>  <br/> |<span data-ttu-id="a8ca5-166">Gesamte Welt</span><span class="sxs-lookup"><span data-stu-id="a8ca5-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="a8ca5-167">Binär vergleichbar (wie bei memcmp)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="a8ca5-168">Nein – Verwenden von [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="a8ca5-169">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-169">Yes</span></span>  <br/> |<span data-ttu-id="a8ca5-170">Ja</span><span class="sxs-lookup"><span data-stu-id="a8ca5-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a8ca5-171">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8ca5-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8ca5-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a8ca5-172">Protocol specifications</span></span>

<span data-ttu-id="a8ca5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ca5-174">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8ca5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ca5-176">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a8ca5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ca5-178">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8ca5-179">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a8ca5-179">Header files</span></span>

<span data-ttu-id="a8ca5-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8ca5-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8ca5-181">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8ca5-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8ca5-182">Mapitags.h</span></span>
  
> <span data-ttu-id="a8ca5-183">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a8ca5-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8ca5-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8ca5-184">See also</span></span>



[<span data-ttu-id="a8ca5-185">PidTagResponsibility (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="a8ca5-186">PidTagStoreRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8ca5-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="a8ca5-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8ca5-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8ca5-188">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a8ca5-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8ca5-189">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a8ca5-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8ca5-190">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a8ca5-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

