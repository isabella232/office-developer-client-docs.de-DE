---
title: Unterstützung von formatierten Text in ausgehenden Nachrichten Client Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 975dd172b6ad342351f014d0966d62a150f713c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571290"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="d3b96-103">Unterstützung von formatiertem Text in ausgehenden Nachrichten: Kundenaufgaben</span><span class="sxs-lookup"><span data-stu-id="d3b96-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="d3b96-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3b96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3b96-105">Clientanwendungen legen Sie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, die Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md))-Eigenschaft für eine ausgehende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d3b96-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="d3b96-106">Clients, die nur-Text unterstützen festlegen nur die **PR_BODY** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d3b96-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="d3b96-107">Rich-Text-Format (RTF)-fähigen Clients möglicherweise **PR_BODY** und **PR_RTF_COMPRESSED** Eigenschaften festlegen oder nur **PR_RTF_COMPRESSED**, je nach der Nachricht Speicheranbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3b96-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="d3b96-108">HTML-fähigen Clients festlegen die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d3b96-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="d3b96-109">Es ist wichtig, damit ein Client überprüfen Sie den Nachrichtenspeicher **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um festzustellen, ob der Informationsspeicher RTF unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3b96-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="d3b96-110">Ist der Nachrichtenspeicher nicht RTF-fähigen, legt ein RTF-fähigen Client die **PR_BODY** und die **PR_RTF_COMPRESSED** Eigenschaften für jede ausgehende Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="d3b96-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="d3b96-111">Wenn der Nachrichtenspeicher RTF-fähigen ist, muss nur die **PR_RTF_COMPRESSED** -Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3b96-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="d3b96-112">**Zum Festlegen von PR_RTF_COMPRESSED und stellen Sie sicher, dass die Synchronisierung geschieht als erforderlich, RTF-fähigen clients**</span><span class="sxs-lookup"><span data-stu-id="d3b96-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="d3b96-113">Rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um die **PR_RTF_COMPRESSED** -Eigenschaft festlegen der MAPI_CREATE ist und die MAPI_MODIFY Flags zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d3b96-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="d3b96-114">MAPI_CREATE ist sichergestellt, dass neuen Daten alle alten Daten ersetzt und MAPI_MODIFY ermöglicht es Ihnen, diese Ersetzung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d3b96-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="d3b96-115">Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion, und übergeben Sie STORE_UNCOMPRESSED_RTF des Nachrichtenspeichers das STORE_UNCOMPRESSED_RTF Bit in seiner **PR_STORE_SUPPORT_MASK** -Eigenschaft, um einen nicht komprimierten Version der **PR_RTF_COMPRESSED abrufen festgelegt **Stream von **OpenProperty**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3b96-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="d3b96-116">Schreiben Sie die Meldungsdaten Text in der nicht komprimierten Stream von **WrapCompressedRTFStream**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3b96-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="d3b96-117">Commit, und der nicht komprimierten und komprimierte Streams freigeben.</span><span class="sxs-lookup"><span data-stu-id="d3b96-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="d3b96-118">Zu diesem Zeitpunkt, wenn der Nachricht Speicheranbieter RTF unterstützt, haben Sie alle durchgeführt, die erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d3b96-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="d3b96-119">Sie können die Nachricht Speicheranbieter Synchronisierungsvorgangs und die Erstellung der **PR_BODY** -Eigenschaft behandelt werden sollen bei Bedarf abhängen.</span><span class="sxs-lookup"><span data-stu-id="d3b96-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="d3b96-120">Jedoch müssen der Nachricht Speicheranbieter RTF nicht unterstützt, Sie die [RTFSync](rtfsync.md) -Funktion, um den Text mit der Formatierung synchronisieren aufrufen, das RTF_SYNC_RTF_CHANGED-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3b96-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

