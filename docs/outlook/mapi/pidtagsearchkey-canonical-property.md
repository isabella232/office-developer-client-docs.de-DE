---
title: Kanonische Pidtagsearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345465"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="41407-103">Kanonische Pidtagsearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41407-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="41407-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41407-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41407-105">Enthält einen binären-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="41407-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41407-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="41407-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41407-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="41407-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="41407-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="41407-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41407-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="41407-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="41407-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="41407-110">Data type:</span></span>  <br/> |<span data-ttu-id="41407-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="41407-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="41407-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41407-112">Area:</span></span>  <br/> |<span data-ttu-id="41407-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41407-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41407-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41407-114">Remarks</span></span>

<span data-ttu-id="41407-115">Diese Eigenschaft stellt eine Ablaufverfolgung für verwandte Objekte wie Nachrichtenkopien bereit und erleichtert das Auffinden unerwünschter Vorkommnisse wie doppelter Empfänger.</span><span class="sxs-lookup"><span data-stu-id="41407-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="41407-116">MAPI verwendet bestimmte Regeln zum Erstellen von Such Schlüsseln für Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="41407-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="41407-117">Der Suchschlüssel wird durch Verkettung des Adresstyps (in Großbuchstaben), des Doppelpunktzeichens ":", der e-Mail-Adresse in kanonischer Form und des abschließenden NULL-Zeichens gebildet.</span><span class="sxs-lookup"><span data-stu-id="41407-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="41407-118">Kanonische Form hier bedeuten, dass die Groß-/Kleinschreibung vertrauliche Adressen in der richtigen Groß-/Kleinschreibung angezeigt werden und Adressen, bei denen die Groß-/Kleinschreibung nicht beachtet wird, in Großbuchstaben umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="41407-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="41407-119">Dies ist wichtig, um Korrelationen zwischen Nachrichten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="41407-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="41407-120">Bei Message-Objekten ist diese Eigenschaft über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode unmittelbar nach der Erstellung der Nachricht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41407-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="41407-121">Für andere Objekte ist Sie nach dem ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41407-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="41407-122">Da diese Eigenschaft veränderbar ist, ist es unzuverlässig, Sie über getProps abzurufen, bis ein **SaveChanges** -Aufruf alle Werte festgelegt hat, die von der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode gesetzt oder geändert wurden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="41407-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="41407-123">Bei Profilen liefert MAPI auch einen hartcodierten Profil Abschnitt namens **MUID_PROFILE_INSTANCE**mit dieser Eigenschaft als einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="41407-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="41407-124">Dieser Schlüssel ist unter allen jemals erstellten Profilen eindeutig und kann zuverlässiger sein als die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft, die beispielsweise gelöscht und mit demselben Namen neu erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="41407-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="41407-125">In der folgenden Tabelle sind wichtige Unterschiede zwischen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) und dieser Eigenschaft zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="41407-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="41407-126">**Merkmal**</span><span class="sxs-lookup"><span data-stu-id="41407-126">**Characteristic**</span></span>|<span data-ttu-id="41407-127">PR_ENTRYID \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="41407-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="41407-128">PR_RECORD_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="41407-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="41407-129">PR_SEARCH_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="41407-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41407-130">Erforderlich für Attachment-Objekte</span><span class="sxs-lookup"><span data-stu-id="41407-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="41407-131">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-131">No</span></span>  <br/> |<span data-ttu-id="41407-132">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-132">Yes</span></span>  <br/> |<span data-ttu-id="41407-133">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-133">No</span></span>  <br/> |
|<span data-ttu-id="41407-134">Erforderliche Ordnerobjekte</span><span class="sxs-lookup"><span data-stu-id="41407-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="41407-135">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-135">Yes</span></span>  <br/> |<span data-ttu-id="41407-136">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-136">Yes</span></span>  <br/> |<span data-ttu-id="41407-137">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-137">No</span></span>  <br/> |
|<span data-ttu-id="41407-138">Erforderlich für Nachrichtenspeicher Objekte</span><span class="sxs-lookup"><span data-stu-id="41407-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="41407-139">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-139">Yes</span></span>  <br/> |<span data-ttu-id="41407-140">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-140">Yes</span></span>  <br/> |<span data-ttu-id="41407-141">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-141">No</span></span>  <br/> |
|<span data-ttu-id="41407-142">Erforderlich für Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="41407-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="41407-143">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-143">Yes</span></span>  <br/> |<span data-ttu-id="41407-144">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-144">No</span></span>  <br/> |<span data-ttu-id="41407-145">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-145">No</span></span>  <br/> |
|<span data-ttu-id="41407-146">Erstellbarer Client</span><span class="sxs-lookup"><span data-stu-id="41407-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="41407-147">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-147">No</span></span>  <br/> |<span data-ttu-id="41407-148">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-148">No</span></span>  <br/> |<span data-ttu-id="41407-149">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-149">Yes</span></span>  <br/> |
|<span data-ttu-id="41407-150">Verfügbar vor **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="41407-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="41407-151">Abhängig von der Anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="41407-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="41407-152">Abhängig von der Anbieterimplementierung</span><span class="sxs-lookup"><span data-stu-id="41407-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="41407-153">Für Nachrichten, ja.</span><span class="sxs-lookup"><span data-stu-id="41407-153">For messages, Yes.</span></span> <span data-ttu-id="41407-154">Für andere ist es von der Anbieterimplementierung abhängig.</span><span class="sxs-lookup"><span data-stu-id="41407-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="41407-155">Geändert in einem Kopiervorgang</span><span class="sxs-lookup"><span data-stu-id="41407-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="41407-156">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-156">Yes</span></span>  <br/> |<span data-ttu-id="41407-157">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-157">Yes</span></span>  <br/> |<span data-ttu-id="41407-158">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-158">No</span></span>  <br/> |
|<span data-ttu-id="41407-159">Nach einer Kopie nach dem Client änderbar</span><span class="sxs-lookup"><span data-stu-id="41407-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="41407-160">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-160">No</span></span>  <br/> |<span data-ttu-id="41407-161">Nein</span><span class="sxs-lookup"><span data-stu-id="41407-161">No</span></span>  <br/> |<span data-ttu-id="41407-162">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-162">Yes</span></span>  <br/> |
|<span data-ttu-id="41407-163">Innerhalb von...</span><span class="sxs-lookup"><span data-stu-id="41407-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="41407-164">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="41407-164">Entire world</span></span>  <br/> |<span data-ttu-id="41407-165">Anbieterinstanz</span><span class="sxs-lookup"><span data-stu-id="41407-165">Provider instance</span></span>  <br/> |<span data-ttu-id="41407-166">Ganze Welt</span><span class="sxs-lookup"><span data-stu-id="41407-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="41407-167">Vergleichbare Binärdatei (wie bei memcmp)</span><span class="sxs-lookup"><span data-stu-id="41407-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="41407-168">No--verwenden Sie [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="41407-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="41407-169">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-169">Yes</span></span>  <br/> |<span data-ttu-id="41407-170">Ja</span><span class="sxs-lookup"><span data-stu-id="41407-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="41407-171">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41407-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41407-172">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="41407-172">Protocol specifications</span></span>

<span data-ttu-id="41407-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41407-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41407-174">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="41407-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41407-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41407-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41407-176">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="41407-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="41407-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41407-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41407-178">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="41407-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41407-179">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="41407-179">Header files</span></span>

<span data-ttu-id="41407-180">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="41407-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="41407-181">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="41407-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="41407-182">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="41407-182">Mapitags.h</span></span>
  
> <span data-ttu-id="41407-183">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="41407-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41407-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41407-184">See also</span></span>



[<span data-ttu-id="41407-185">Kanonische Pidtagresponsibility (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41407-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="41407-186">Kanonische Pidtagstorerecordkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41407-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="41407-187">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41407-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41407-188">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41407-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41407-189">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41407-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41407-190">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41407-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

