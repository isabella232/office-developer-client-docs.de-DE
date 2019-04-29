---
title: Unterstützung von formatiertem Text in den Client Aufgaben für ausgehende Nachrichten
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
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="b4a67-103">Unterstützung von formatiertem Text in ausgehenden Nachrichten: Aufgaben des Kunden</span><span class="sxs-lookup"><span data-stu-id="b4a67-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="b4a67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4a67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4a67-105">Client Anwendungen legen die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft, die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft oder die **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md))-Eigenschaft für eine ausgehende Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="b4a67-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="b4a67-106">Clients, die nur einfachen Text unterstützen, legen nur die **PR_BODY** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b4a67-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="b4a67-107">Rich Text Format (RTF)-fähige Clients können sowohl **PR_BODY** -als auch **PR_RTF_COMPRESSED** -Eigenschaften oder nur **PR_RTF_COMPRESSED**-abhängig vom verwendeten Nachrichtenspeicher Anbieter festlegen.</span><span class="sxs-lookup"><span data-stu-id="b4a67-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="b4a67-108">HTML-fähige Clients legen die **PR_HTML** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b4a67-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="b4a67-109">Es ist wichtig, dass ein Client die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers überprüft, um zu bestimmen, ob der Speicher RTF unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4a67-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="b4a67-110">Wenn der Nachrichtenspeicher nicht RTF-fähig ist, legt ein RTF-fähiger Client sowohl die **PR_BODY** -als auch die **PR_RTF_COMPRESSED** -Eigenschaft für jede ausgehende Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="b4a67-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="b4a67-111">Wenn der Nachrichtenspeicher RTF-fähig ist, muss nur die **PR_RTF_COMPRESSED** -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b4a67-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="b4a67-112">**Um PR_RTF_COMPRESSED festzulegen und sicherzustellen, dass der Synchronisierungsprozess bei Bedarf erfolgt, werden RTF-fähige Clients**</span><span class="sxs-lookup"><span data-stu-id="b4a67-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="b4a67-113">Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen und sowohl die MAPI_CREATE-als auch die MAPI_MODIFY-Flags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b4a67-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="b4a67-114">MAPI_CREATE stellt sicher, dass alle neuen Daten alle alten Daten ersetzen, und MAPI_MODIFY ermöglicht es Ihnen, diese Ersetzungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b4a67-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="b4a67-115">Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion auf, und übergeben Sie STORE_UNCOMPRESSED_RTF, wenn der Nachrichtenspeicher das STORE_UNCOMPRESSED_RTF-Bit in seiner **PR_STORE_SUPPORT_MASK** -Eigenschaft festlegt, um eine nicht komprimierte Version des PR_RTF_COMPRESSED zu erhalten. \*\* \*\*von OpenProperty \*\*\*\* zurückgegebener Stream.</span><span class="sxs-lookup"><span data-stu-id="b4a67-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="b4a67-116">Schreiben Sie die Nachrichten Textdaten in den unkomprimierten Stream, der von **WrapCompressedRTFStream**zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4a67-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="b4a67-117">Commit und Freigeben der unkomprimierten und komprimierten Streams.</span><span class="sxs-lookup"><span data-stu-id="b4a67-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="b4a67-118">Wenn der Nachrichtenspeicher Anbieter RTF unterstützt, haben Sie jetzt alle erforderlichen Schritte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4a67-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="b4a67-119">Sie können den Synchronisierungsprozess und die Erstellung der **PR_BODY** -Eigenschaft, falls erforderlich, vom Nachrichtenspeicher Anbieter abhängig zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="b4a67-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="b4a67-120">Wenn der Nachrichtenspeicher Anbieter jedoch RTF nicht unterstützt, müssen Sie die [RTFSync](rtfsync.md) -Funktion aufrufen, um den Text mit der Formatierung zu synchronisieren, indem Sie das RTF_SYNC_RTF_CHANGED-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="b4a67-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

