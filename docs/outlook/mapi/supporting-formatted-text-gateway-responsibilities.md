---
title: Unterstützung von formatierten Text Gateway Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795663"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="20d61-103">Unterstützung von formatiertem Text: Aufgaben des Gateways</span><span class="sxs-lookup"><span data-stu-id="20d61-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="20d61-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20d61-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="20d61-105">**Zum Verarbeiten von Rich-Text-Format für ausgehende Nachrichten, gateways**</span><span class="sxs-lookup"><span data-stu-id="20d61-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="20d61-106">Rufen Sie nur eine Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft aus dem Nachrichtenspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="20d61-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="20d61-107">Der Hauptvorteil Abrufen nur die **PR_RTF_COMPRESSED** -Eigenschaft ist, dass der Nachrichtentext nicht zwischen Computern gesendet werden, wenn das Gateway und dem Nachrichtenspeicher auf verschiedenen Computern vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="20d61-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="20d61-108">Generieren Sie dem Nachrichtentext aus der formatierte Text entweder durch den Aufruf von RTF-Library-Funktion **HrTextFromCompressedRTFStream** oder, falls die Nachricht lokal gespeichert ist **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="20d61-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="20d61-109">Das Flag RTF_SYNC_RTF_CHANGED sollte in den Aufruf von **RTFSync**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="20d61-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="20d61-110">Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="20d61-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="20d61-111">Stellen Sie den Nachrichtentext, z. B. das Verwerfen nicht unterstützter Zeichen in irgendeiner Weise nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="20d61-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="20d61-112">Stellen Sie sicher, dass **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) und alle RTF Auxilliary Eigenschaften entweder festgelegt sind oder nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20d61-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="20d61-113">Wenn alle Änderungen vorgenommen wurden, rufen Sie mit der RTF_SYNC_RTF_CHANGED und die RTF_SYNC_BODY_CHANGED Flags **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="20d61-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="20d61-114">**RTFSync** wird die RTF Auxilliary Eigenschaften aus dem geänderten Text neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="20d61-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="20d61-115">Stellen Sie alle umkehrbar Änderungen an den Nachrichtentext, wie Anlagen Platzhalter einfügen und nicht zerstörerische Codepages ausführen.</span><span class="sxs-lookup"><span data-stu-id="20d61-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="20d61-116">Senden der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="20d61-116">Send the message.</span></span>
    
 <span data-ttu-id="20d61-117">**Zum Verarbeiten von Rich-Text-Format für eingehende Nachrichten gateways**</span><span class="sxs-lookup"><span data-stu-id="20d61-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="20d61-118">Umgekehrte Modifikationen Text Nachricht, die direkt vorgenommen wurden, bevor die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="20d61-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="20d61-119">Rufen Sie **RTFSync** , wenn die Nachricht die **PR_RTF_COMPRESSED** und die Eigenschaften **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) enthält.</span><span class="sxs-lookup"><span data-stu-id="20d61-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="20d61-120">Aktualisieren Sie die Nachricht im Nachrichtenspeicher mit der **PR_RTF_COMPRESSED** -Eigenschaft, wenn die Meldung Es enthält; Aktualisieren Sie mit der **PR_BODY** -Eigenschaft nur, wenn **PR_RTF_COMPRESSED** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="20d61-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="20d61-121">Verwerfen Sie **PR_BODY** , wenn die Nachricht diese Eigenschaft und die **PR_RTF_COMPRESSED**enthält.</span><span class="sxs-lookup"><span data-stu-id="20d61-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="20d61-122">Gateways Aufrufen **RTFSync** zur Vermeidung der Nachrichtentext und die formatierten Text übertragen, wenn der Nachrichtenspeicher auf einem anderen Computer ist.</span><span class="sxs-lookup"><span data-stu-id="20d61-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="20d61-123">Wenn das Gateway lokal ist, kann die Eigenschaften festgelegt werden und des Nachrichtenspeichers für die Synchronisierung zulassen.</span><span class="sxs-lookup"><span data-stu-id="20d61-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

