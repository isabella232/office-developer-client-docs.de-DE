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
ms.openlocfilehash: 8d9f6311b19ddb489885004a9e507f780d9f1ea9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795220"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="f7b88-103">Kanonische PidTagStoreSupportMask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7b88-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="f7b88-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7b88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7b88-105">Enthält einer Bitmaske aus Flags dieser Client Applications Abfrage aus, um die Eigenschaften eines Nachrichtenspeichers bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7b88-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f7b88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7b88-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="f7b88-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="f7b88-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f7b88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7b88-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="f7b88-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="f7b88-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f7b88-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7b88-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f7b88-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f7b88-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f7b88-112">Area:</span></span>  <br/> |<span data-ttu-id="f7b88-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="f7b88-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7b88-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7b88-114">Remarks</span></span>

<span data-ttu-id="f7b88-115">Diese Eigenschaft gibt die Funktionen des einen Nachrichtenspeicher für Clientanwendungen, die planen sie eine Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="f7b88-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="f7b88-116">Die Kennzeichen unterstützen Entscheidungen durch einen Client oder einem anderen Speicher, z. B., ob **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder nur **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) gesendet.</span><span class="sxs-lookup"><span data-stu-id="f7b88-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="f7b88-117">Ein Client sollte niemals **PR_STORE_SUPPORT_MASK**festgelegt. Beim Festlegen dieses Kennzeichen gibt MAPI_E_COMPUTED zurück.</span><span class="sxs-lookup"><span data-stu-id="f7b88-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="f7b88-118">Für die Bitmaske **PR_STORE_SUPPORT_MASK** kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f7b88-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="f7b88-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="f7b88-120">(131072, 0 x 00020000) Der Nachrichtenspeicher unterstützt Eigenschaften, die ANSI (8-Bit) Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7b88-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="f7b88-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="f7b88-122">(32, 0 x 00000020) Nachrichtenspeicher werden Anlagen (OLE oder nicht-OLE) von Nachrichten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7b88-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="f7b88-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="f7b88-124">(1024, 0 x 00000400) Der Nachrichtenspeicher unterstützt kategorisierte Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="f7b88-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="f7b88-126">(16, 0 x 00000010) Der Nachrichtenspeicher unterstützt die Erstellung von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f7b88-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="f7b88-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="f7b88-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="f7b88-128">(1, 0 x 00000001) Für die Objekte im Nachrichtenspeicher Eintragsbezeichner sind eindeutig, d. h., während der Lebensdauer des Speichers niemals wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="f7b88-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="f7b88-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="f7b88-130">(65536, 0 x 00010000) Der Nachrichtenspeicher unterstützt HTML-Nachrichten, die in der Eigenschaft **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f7b88-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="f7b88-131">Wenn Ihre Entwicklungsumgebung ein MAPIDEFS verwendet wird. H-Datei, die nicht STORE_HTML_OK enthalten, verwenden Sie stattdessen den Wert 0 x 00010000.</span><span class="sxs-lookup"><span data-stu-id="f7b88-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="f7b88-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="f7b88-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="f7b88-133">(2097152, 0x00200000) In einem gepackten PST-Speicher, dass beim Empfang einer neuen Nachricht an den Speicher der Speicher Regeln und Spam-Filter Verarbeitung der Nachricht getrennt aufwendet.</span><span class="sxs-lookup"><span data-stu-id="f7b88-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="f7b88-134">Der Informationsspeicher ruft [IMAPISupport::Notify](imapisupport-notify.md), Einstellung **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und klicken Sie dann die Details der neuen Nachricht an dem listening Client übergibt.</span><span class="sxs-lookup"><span data-stu-id="f7b88-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="f7b88-135">Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="f7b88-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="f7b88-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="f7b88-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="f7b88-137">(524288, 0x00080000) Dieses Kennzeichen ist reserviert und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7b88-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="f7b88-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="f7b88-139">(8, 0 x 00000008) Der Nachrichtenspeicher unterstützt die Änderung der vorhandenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f7b88-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="f7b88-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="f7b88-141">(512, 0 x 00000200) Der Nachrichtenspeicher mehrwertige Eigenschaften unterstützt, die Stabilität der Reihenfolge der Wert in einer mehrwertigen Eigenschaft in der gesamten Speichervorgang garantiert Vorgang und unterstützt die Instanziierung von mehrwertigen Eigenschaften in Tabellen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="f7b88-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="f7b88-143">(256, 0 x 00000100) Der Nachrichtenspeicher unterstützt Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="f7b88-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="f7b88-145">(64, 0 x 00000040) Der Nachrichtenspeicher unterstützt OLE-Anlagen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="f7b88-146">OLE-Daten können über einen **IStorage** -Schnittstelle, z. B., die über die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f7b88-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="f7b88-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f7b88-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="f7b88-148">(16384, 0x00004000) Der Ordner in diesem Zertifikatspeicher sind öffentliche (mehrere Benutzer) wird nicht private (möglicherweise mit mehreren Instanzen, aber nicht mehrere Benutzer).</span><span class="sxs-lookup"><span data-stu-id="f7b88-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="f7b88-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="f7b88-150">(8388608, 0 x 00800000) Der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher ist verantwortlich für die pushen von Änderungen durch Benachrichtigungen an den Indexer Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f7b88-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="f7b88-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="f7b88-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="f7b88-152">(2, 0 x 00000002) Alle Schnittstellen für den Nachrichtenspeicher verfügen über eine nur-Lese-Zugriffsebene.</span><span class="sxs-lookup"><span data-stu-id="f7b88-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="f7b88-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="f7b88-154">(4096, 0 x 00001000) Der Nachrichtenspeicher unterstützt Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="f7b88-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="f7b88-156">(2048, 0x00000800) Der Nachrichtenspeicher unterstützt Rich Text Format (RTF)-Nachrichten, die in der Regel komprimiert und der Informationsspeicher selbst behält **PR_BODY** **PR_RTF_COMPRESSED** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f7b88-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="f7b88-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="f7b88-158">(268435456, 0 x 10000000) Gibt an, dass Regeln in diesem PST-Speicher gespeichert werden soll, auch wenn es sich nicht um die Standard-Informationsspeichers ist.</span><span class="sxs-lookup"><span data-stu-id="f7b88-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="f7b88-159">Wenn **STORE_RULES_OK** in Verbindung mit **NON_EMS_XP_SAVE**verwendet wird, sind Regeln in einem nicht standardmäßigen PST umfließendem Informationsspeicher ausführen können.</span><span class="sxs-lookup"><span data-stu-id="f7b88-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="f7b88-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="f7b88-161">(4, 0 x 00000004) Der Nachrichtenspeicher unterstützt Suchergebnisse Ordner.</span><span class="sxs-lookup"><span data-stu-id="f7b88-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="f7b88-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="f7b88-163">(8192, 0 x 00002000) Der Nachrichtenspeicher unterstützt Sortierung Ansichten von Tabellen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="f7b88-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="f7b88-165">(128, 0x00000080) Der Nachrichtenspeicher unterstützt Markierens einer Nachricht für die Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="f7b88-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="f7b88-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="f7b88-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="f7b88-167">(32768, 0x00008000) Nachrichtenspeicher unterstützt das Speichern von RTF-Nachrichten in nicht komprimierten Format.</span><span class="sxs-lookup"><span data-stu-id="f7b88-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="f7b88-168">Ein nicht komprimierter RTF-Stream wird durch den Wert **DwMagicUncompressedRTF** im Streamheader identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f7b88-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="f7b88-169">Der Wert **DwMagicUncompressedRTF** ist in der RTFLIB definiert. H-Datei.</span><span class="sxs-lookup"><span data-stu-id="f7b88-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="f7b88-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="f7b88-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="f7b88-171">(262144, 0 x 00040000) Gibt an, dass der Nachrichtenspeicher Unicode-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7b88-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="f7b88-172">Ein Client kann für das Vorhandensein des Flags entscheiden, ob anfordern oder Unicode-Informationen im Speicher speichern aussehen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="f7b88-173">Eine RTF-Version einer Nachricht kann immer gespeichert werden, selbst wenn der Nachrichtenspeicher RTF nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7b88-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="f7b88-174">Wenn das Bit STORE_RTF_OK für einen bestimmten Speicher nicht festgelegt ist, müssen einen Client RTF-Versionen verwalten die [RTFSync](rtfsync.md) -Funktion, um die **PR_BODY** und **PR_RTF_COMPRESSED** Versionen für Textinhalt synchronisiert halten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="f7b88-175">RTF wird immer in **PR_RTF_COMPRESSED**, gespeichert, ob es tatsächlich oder nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7b88-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7b88-176">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f7b88-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7b88-177">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f7b88-177">Protocol specifications</span></span>

<span data-ttu-id="f7b88-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b88-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b88-179">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7b88-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b88-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b88-181">Beschreibt das Format von Nachrichten, die zum Senden von Informationen im Zusammenhang mit der Freigabe von Ordnern auf dem Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7b88-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7b88-182">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f7b88-182">Header files</span></span>

<span data-ttu-id="f7b88-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7b88-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7b88-184">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f7b88-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7b88-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7b88-185">Mapitags.h</span></span>
  
> <span data-ttu-id="f7b88-186">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f7b88-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7b88-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7b88-187">See also</span></span>



[<span data-ttu-id="f7b88-188">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7b88-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7b88-189">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7b88-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7b88-190">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f7b88-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7b88-191">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f7b88-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

