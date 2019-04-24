---
title: Kanonische PidTagStoreSupportMask-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340971"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="50165-103">Kanonische PidTagStoreSupportMask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50165-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="50165-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50165-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50165-105">Enthält eine Bitmaske von Flags, die von Clientanwendungen abgefragt werden, um die Merkmale eines Nachrichtenspeichers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="50165-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50165-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="50165-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50165-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="50165-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="50165-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="50165-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50165-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="50165-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="50165-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="50165-110">Data type:</span></span>  <br/> |<span data-ttu-id="50165-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="50165-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="50165-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="50165-112">Area:</span></span>  <br/> |<span data-ttu-id="50165-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="50165-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50165-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50165-114">Remarks</span></span>

<span data-ttu-id="50165-115">Diese Eigenschaft offenbart die Funktionen eines Nachrichtenspeichers für Clientanwendungen, die eine Nachricht senden möchten.</span><span class="sxs-lookup"><span data-stu-id="50165-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="50165-116">Die Flags können Entscheidungen eines Clients oder eines anderen Speichers unterstützen, beispielsweise ob **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="50165-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="50165-117">Ein Client sollte **PR_STORE_SUPPORT_MASK**nie festlegen; bei dem Versuch, dieses Flag festzulegen, wird MAPI_E_COMPUTED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50165-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="50165-118">Eine oder mehrere der folgenden Flags können für die **PR_STORE_SUPPORT_MASK** -Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="50165-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="50165-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="50165-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="50165-120">(131072, 0x00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die ANSI-Zeichen (8-Bit) enthalten.</span><span class="sxs-lookup"><span data-stu-id="50165-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="50165-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="50165-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="50165-122">(32, 0x00000020) Der Nachrichtenspeicher unterstützt Anlagen (OLE oder nicht-OLE) für Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="50165-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="50165-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="50165-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="50165-124">(1024, 0x00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="50165-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="50165-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="50165-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="50165-126">(16, 0x00000010) Der Nachrichtenspeicher unterstützt das Erstellen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="50165-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="50165-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="50165-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="50165-128">(1, 0x00000001) Eintragsbezeichner für die Objekte im Nachrichtenspeicher sind eindeutig, also nie wieder verwendet während der Lebensdauer des Speichers.</span><span class="sxs-lookup"><span data-stu-id="50165-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="50165-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="50165-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="50165-130">(65536, 0x00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der **PR_BODY_HTML** ([pidtagbodyhtml (](pidtagbodyhtml-canonical-property.md))-Eigenschaft gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="50165-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="50165-131">Wenn in der Entwicklungsumgebung ein MAPIDEFS verwendet wird. H die Datei, die nicht STORE_HTML_OK enthält, verwenden Sie stattdessen den Wert 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="50165-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="50165-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="50165-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="50165-133">(2097152, 0x00200000) Gibt in einem umbrochenen PST-Speicher an, dass beim Eintreffen einer neuen Nachricht im Speicher der speicherregeln und die Spamfilter Verarbeitung für die Nachricht separat ausführt.</span><span class="sxs-lookup"><span data-stu-id="50165-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="50165-134">Der Store ruft [IMAPISupport:: notify](imapisupport-notify.md)auf, legt **Uleventmaskfnevnewmail** in der [Benachrichtigungs](notification.md) Struktur fest, die als Parameter übergeben wird, und übergibt dann die Details der neuen Nachricht an den überwachenden Client.</span><span class="sxs-lookup"><span data-stu-id="50165-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="50165-135">Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an.</span><span class="sxs-lookup"><span data-stu-id="50165-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="50165-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="50165-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="50165-137">(524288, 0x00080000) Dieses Flag ist reserviert und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50165-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="50165-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="50165-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="50165-139">(8, 0x00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="50165-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="50165-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="50165-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="50165-141">(512, 0x00000200) Der Nachrichtenspeicher unterstützt mehrwertige Eigenschaften, garantiert die Stabilität der Wertreihenfolge in einer mehrwertigen Eigenschaft während eines Speichervorgangs und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen.</span><span class="sxs-lookup"><span data-stu-id="50165-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="50165-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="50165-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="50165-143">(256, 0x00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="50165-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="50165-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="50165-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="50165-145">(64, 0x00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen.</span><span class="sxs-lookup"><span data-stu-id="50165-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="50165-146">Auf die OLE-Daten kann über eine **IStorage** -Schnittstelle zugegriffen werden, wie Sie über die **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="50165-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="50165-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="50165-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="50165-148">(16384, 0x00004000) Die Ordner in diesem Speicher sind öffentlich (mehr Benutzer) und nicht privat (möglicherweise mehrere Instanzen, jedoch nicht mehrere Benutzer).</span><span class="sxs-lookup"><span data-stu-id="50165-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="50165-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="50165-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="50165-150">(8388608, 0x00800000) Der MAPI-Protokoll Handler crawlt den Speicher nicht, und der Speicher ist dafür verantwortlich, alle Änderungen durch Benachrichtigungen an den Indexer zu übertragen, damit Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="50165-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="50165-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="50165-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="50165-152">(2, 0x00000002) Alle Schnittstellen für den Nachrichtenspeicher weisen eine schreibgeschützte Zugriffsebene auf.</span><span class="sxs-lookup"><span data-stu-id="50165-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="50165-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="50165-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="50165-154">(4096, 0x00001000) Der Nachrichtenspeicher unterstützt Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="50165-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="50165-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="50165-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="50165-156">(2048, 0x00000800) Der Nachrichtenspeicher unterstützt RTF-Nachrichten (Rich Text Format), in der Regel komprimiert, und der Speicher selbst hält **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="50165-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="50165-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="50165-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="50165-158">(268435456, 0x10000000) Gibt an, dass Regeln in diesem PST-Speicher gespeichert werden sollen, auch wenn es sich nicht um den Standardspeicher handelt.</span><span class="sxs-lookup"><span data-stu-id="50165-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="50165-159">Wenn **STORE_RULES_OK** in Verbindung mit **NON_EMS_XP_SAVE**verwendet wird, können Regeln auf nicht-standardmäßigen PST-umgebrochenen speichern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="50165-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="50165-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="50165-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="50165-161">(4, 0x00000004) Der Nachrichtenspeicher unterstützt Ordner mit Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="50165-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="50165-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="50165-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="50165-163">(8192, 0x00002000) Der Nachrichtenspeicher unterstützt das Sortieren von Tabellen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="50165-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="50165-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="50165-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="50165-165">(128, 0x00000080) Der Nachrichtenspeicher unterstützt das Markieren einer Nachricht für die Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="50165-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="50165-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="50165-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="50165-167">(32768, 0x00008000) Der Nachrichtenspeicher unterstützt das Speichern von RTF-Nachrichten in unkomprimierter Form.</span><span class="sxs-lookup"><span data-stu-id="50165-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="50165-168">Ein unkomprimierter RTF-Datenstrom wird durch den Wert **dwMagicUncompressedRTF** im Stream-Header identifiziert.</span><span class="sxs-lookup"><span data-stu-id="50165-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="50165-169">Der **dwMagicUncompressedRTF** -Wert wird in der RTFLIB definiert. H-Datei.</span><span class="sxs-lookup"><span data-stu-id="50165-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="50165-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="50165-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="50165-171">(262144, 0x00040000) Gibt an, dass der Nachrichtenspeicher Unicode-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50165-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="50165-172">Ein Client kann das Vorhandensein dieser Kennzeichnung überprüfen und entscheiden, ob er Unicode-Informationen abruft oder speichert.</span><span class="sxs-lookup"><span data-stu-id="50165-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="50165-173">Eine RTF-Version einer Nachricht kann immer gespeichert werden, auch wenn der Nachrichtenspeicher nicht im RTF-Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="50165-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="50165-174">Wenn das STORE_RTF_OK-Bit für einen bestimmten Speicher nicht festgelegt ist, muss ein Client, der RTF-Versionen verwaltet, selbst die [RTFSync](rtfsync.md) -Funktion aufrufen, um die **PR_BODY** -und **PR_RTF_COMPRESSED** -Versionen für Textinhalte zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="50165-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="50165-175">RTF wird immer in **PR_RTF_COMPRESSED**gespeichert, unabhängig davon, ob es tatsächlich komprimiert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="50165-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="50165-176">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="50165-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50165-177">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="50165-177">Protocol specifications</span></span>

<span data-ttu-id="50165-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50165-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50165-179">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="50165-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50165-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50165-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50165-181">Beschreibt das Format der Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50165-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50165-182">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="50165-182">Header files</span></span>

<span data-ttu-id="50165-183">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="50165-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="50165-184">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="50165-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="50165-185">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="50165-185">Mapitags.h</span></span>
  
> <span data-ttu-id="50165-186">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="50165-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50165-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50165-187">See also</span></span>



[<span data-ttu-id="50165-188">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50165-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50165-189">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50165-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50165-190">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="50165-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50165-191">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="50165-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

