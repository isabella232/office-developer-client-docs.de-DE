---
title: Unterstützen von formatierten Text in Clientaufgaben für ausgehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431603"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="38254-103">Unterstützen von formatierten Text in ausgehenden Nachrichten: Clientaufgaben</span><span class="sxs-lookup"><span data-stu-id="38254-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="38254-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38254-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38254-105">Clientanwendungen legen die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft oder die **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) -Eigenschaft für eine ausgehende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="38254-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="38254-106">Clients, die nur Nur-Text unterstützen, legen nur die **PR_BODY** fest.</span><span class="sxs-lookup"><span data-stu-id="38254-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="38254-107">RtF-bewusste Clients (Rich Text  Format) können PR_BODY- und **PR_RTF_COMPRESSED-Eigenschaften** oder nur **PR_RTF_COMPRESSED** festlegen, abhängig vom verwendeten Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="38254-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="38254-108">HTML- aware clients set **the PR_HTML** property.</span><span class="sxs-lookup"><span data-stu-id="38254-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="38254-109">Es ist wichtig, dass ein Client die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft des Nachrichtenspeichers überprüft, um zu bestimmen, ob der Speicher RTF unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38254-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="38254-110">Wenn der Nachrichtenspeicher nicht RTF-bewusst ist, legt  ein RTF-bewusster Client die Eigenschaften PR_BODY und **PR_RTF_COMPRESSED** für jede ausgehende Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="38254-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="38254-111">Wenn der Nachrichtenspeicher RTF-bewusst ist, muss nur **die PR_RTF_COMPRESSED** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="38254-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="38254-112">**Zum Festlegen PR_RTF_COMPRESSED und sicherstellen, dass der Synchronisierungsprozess bei Bedarf ausgeführt wird, müssen RTF-bewusste Clients**</span><span class="sxs-lookup"><span data-stu-id="38254-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="38254-113">Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) auf, um die **PR_RTF_COMPRESSED-Eigenschaft** zu öffnen, indem Sie sowohl die MAPI_CREATE als auch MAPI_MODIFY festlegen.</span><span class="sxs-lookup"><span data-stu-id="38254-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="38254-114">MAPI_CREATE stellt sicher, dass alle neuen Daten alte Daten ersetzen und MAPI_MODIFY sie ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="38254-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="38254-115">Rufen Sie die [WrapCompressedRTFStream-Funktion](wrapcompressedrtfstream.md) auf, und übergeben Sie STORE_UNCOMPRESSED_RTF, wenn der Nachrichtenspeicher das STORE_UNCOMPRESSED_RTF-Bit in seiner **PR_STORE_SUPPORT_MASK-Eigenschaft** fest, um eine nicht komprimierte Version des PR_RTF_COMPRESSED-Datenstroms zu erhalten, der von **OpenProperty** zurückgegeben wird. </span><span class="sxs-lookup"><span data-stu-id="38254-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="38254-116">Schreiben Sie die Nachrichtentextdaten in den nicht komprimierten Datenstrom, der von **WrapCompressedRTFStream zurückgegeben wird.**</span><span class="sxs-lookup"><span data-stu-id="38254-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="38254-117">Commit und Freigabe der nicht komprimierten und komprimierten Datenströme.</span><span class="sxs-lookup"><span data-stu-id="38254-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="38254-118">Wenn der Nachrichtenspeicheranbieter zu diesem Zeitpunkt RTF unterstützt, haben Sie alles erforderliche getan.</span><span class="sxs-lookup"><span data-stu-id="38254-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="38254-119">Sie können vom Nachrichtenspeicheranbieter abhängig sein, um den Synchronisierungsprozess und die Erstellung der **PR_BODY-Eigenschaft** zu verarbeiten, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38254-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="38254-120">Wenn der Nachrichtenspeicheranbieter rtF jedoch nicht unterstützt, müssen Sie die [RTFSync-Funktion](rtfsync.md) aufrufen, um den Text mit der Formatierung zu synchronisieren, indem Sie RTF_SYNC_RTF_CHANGED festlegen.</span><span class="sxs-lookup"><span data-stu-id="38254-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

