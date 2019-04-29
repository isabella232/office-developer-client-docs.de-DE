---
title: Kanonische Pidtagstoreunicodemask (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437938"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="4a3c0-103">Kanonische Pidtagstoreunicodemask (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4a3c0-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="4a3c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a3c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a3c0-105">Enthält eine Bitmaske von Flags, die von Clientanwendungen abgefragt werden sollen, um die Merkmale eines Nachrichtenspeichers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a3c0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a3c0-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="4a3c0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a3c0-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="4a3c0-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="4a3c0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a3c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a3c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a3c0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-112">Area:</span></span>  <br/> |<span data-ttu-id="4a3c0-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="4a3c0-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a3c0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a3c0-114">Remarks</span></span>

<span data-ttu-id="4a3c0-115">Diese Eigenschaft offenbart die Funktionen eines Nachrichtenspeichers für Clientanwendungen, die eine Nachricht senden möchten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="4a3c0-116">Die Flags können Entscheidungen von einem Client oder einem anderen Speicher erleichtern, beispielsweise ob **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="4a3c0-117">Ein Client sollte diese Eigenschaft nie festlegen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-117">A client should never set this property.</span></span> <span data-ttu-id="4a3c0-118">Ein Versuch gibt **MAPI_E_COMPUTED**zurück.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="4a3c0-119">Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4a3c0-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="4a3c0-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="4a3c0-121">(131072, 0x00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die ANSI (8-Bit)-Zeichen (American National Standards Institute) enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="4a3c0-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="4a3c0-123">(32, 0x00000020) Der Nachrichtenspeicher unterstützt das Verknüpfen und einBetten von Objekten (OLE) oder nicht-OLE-Anlagen zu Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="4a3c0-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="4a3c0-125">(1024, 0x00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="4a3c0-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="4a3c0-127">(16, 0x00000010) Der Nachrichtenspeicher unterstützt das Erstellen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="4a3c0-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="4a3c0-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="4a3c0-129">(1, 0x00000001) Eintragsbezeichner für die Objekte im Nachrichtenspeicher sind eindeutig, also nie wieder verwendet während der Lebensdauer des Speichers.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="4a3c0-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="4a3c0-131">(65536, 0x00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der **PR_BODY_HTML** ([pidtagbodyhtml (](pidtagbodyhtml-canonical-property.md))-Eigenschaft gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="4a3c0-132">Beachten Sie, dass **STORE_HTML_OK** in Versionen von MAPIDEFS nicht definiert ist. H, die in Microsoft Exchange 2000 Server und früher enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="4a3c0-133">Wenn in der Entwicklungsumgebung ein MAPIDEFS verwendet wird. H die Datei, die nicht **STORE_HTML_OK**enthält, verwenden Sie stattdessen den Wert "0x00010000".</span><span class="sxs-lookup"><span data-stu-id="4a3c0-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="4a3c0-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="4a3c0-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="4a3c0-135">(2097152, 0x00200000) Gibt in einem umbrochenen PST-Speicher an, dass beim Eintreffen einer neuen Nachricht im Speicher der Store Regeln und die Spamfilter Verarbeitung für die Nachricht separat ausführt.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="4a3c0-136">Der Store ruft [IMAPISupport:: notify](imapisupport-notify.md)auf, legt **Uleventmaskfnevnewmail** in der [Benachrichtigungs](notification.md) Struktur fest, die als Parameter übergeben wird, und übergibt dann die Details der neuen Nachricht an den überwachenden Client.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="4a3c0-137">Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="4a3c0-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="4a3c0-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="4a3c0-139">(524288, 0x00080000) Dieses Flag ist reserviert und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="4a3c0-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="4a3c0-141">(8, 0x00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="4a3c0-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="4a3c0-143">(512, 0x00000200) Der Nachrichtenspeicher unterstützt mehrwertige Eigenschaften, garantiert die Stabilität der Wertreihenfolge in einer mehrwertigen Eigenschaft während eines Speichervorgangs und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="4a3c0-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="4a3c0-145">(256, 0x00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="4a3c0-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="4a3c0-147">(64, 0x00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="4a3c0-148">Auf die OLE-Daten kann über eine **IStorage** -Schnittstelle zugegriffen werden, wie Sie über die **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="4a3c0-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="4a3c0-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="4a3c0-150">(16384, 0x00004000) Die Ordner in diesem Speicher sind öffentlich (mehr Benutzer) und nicht privat (möglicherweise mehrere Instanzen, jedoch nicht mehrere Benutzer).</span><span class="sxs-lookup"><span data-stu-id="4a3c0-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="4a3c0-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="4a3c0-152">(8388608, 0x00800000) Der MAPI-Protokoll Handler crawlt den Speicher nicht, und der Speicher ist dafür verantwortlich, alle Änderungen durch Benachrichtigungen an den Indexer zu übertragen, damit Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="4a3c0-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="4a3c0-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="4a3c0-154">(2, 0x00000002) Alle Schnittstellen für den Nachrichtenspeicher weisen eine schreibgeschützte Zugriffsebene auf.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="4a3c0-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="4a3c0-156">(4096, 0x00001000) Der Nachrichtenspeicher unterstützt Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="4a3c0-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="4a3c0-158">(2048, 0x00000800) Der Nachrichtenspeicher unterstützt RTF-Nachrichten (Rich Text Format), in der Regel komprimiert, und der Speicher selbst hält **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="4a3c0-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="4a3c0-160">(4, 0x00000004) Der Nachrichtenspeicher unterstützt Ordner mit Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="4a3c0-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="4a3c0-162">(8192, 0x00002000) Der Nachrichtenspeicher unterstützt das Sortieren von Tabellen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="4a3c0-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="4a3c0-164">(128, 0x00000080) Der Nachrichtenspeicher unterstützt das Markieren einer Nachricht für die Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="4a3c0-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="4a3c0-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="4a3c0-166">(32768, 0x00008000) Der Nachrichtenspeicher unterstützt das Speichern von überarbeiteten Formulartext Nachrichten (RTF) in nicht komprimierter Form.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="4a3c0-167">Ein unkomprimierter RTF-Datenstrom wird durch den Wert **dwMagicUncompressedRTF** im Stream-Header identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="4a3c0-168">Der **dwMagicUncompressedRTF** -Wert wird in der RTFLIB definiert. H-Datei.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="4a3c0-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="4a3c0-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="4a3c0-170">(262144, 0x00040000) Der Nachrichtenspeicher unterstützt Eigenschaften, die Unicode-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="4a3c0-171">Eine RTF-Version einer Nachricht kann immer gespeichert werden, auch wenn der Nachrichtenspeicher nicht im RTF-Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="4a3c0-172">Wenn das STORE_RTF_OK-Bit für einen bestimmten Speicher nicht festgelegt ist, muss ein Client, der RTF-Versionen verwaltet, selbst die [RTFSync](rtfsync.md) -Funktion aufrufen, um die **PR_BODY** -und **PR_RTF_COMPRESSED** -Versionen für Textinhalte zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="4a3c0-173">RTF wird immer in **PR_RTF_COMPRESSED**gespeichert, unabhängig davon, ob es tatsächlich komprimiert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a3c0-174">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a3c0-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4a3c0-175">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4a3c0-175">Header files</span></span>

<span data-ttu-id="4a3c0-176">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a3c0-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a3c0-177">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a3c0-178">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4a3c0-178">Mapitags.h</span></span>
  
> <span data-ttu-id="4a3c0-179">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4a3c0-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a3c0-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a3c0-180">See also</span></span>



[<span data-ttu-id="4a3c0-181">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a3c0-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a3c0-182">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a3c0-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a3c0-183">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a3c0-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a3c0-184">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a3c0-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

