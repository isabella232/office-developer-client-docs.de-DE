---
title: Unterstützen von Verantwortlichkeiten für formatierte Textgateways
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419429"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="de1ce-103">Unterstützen von formatierten Text: Gateway-Verantwortlichkeiten</span><span class="sxs-lookup"><span data-stu-id="de1ce-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="de1ce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de1ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="de1ce-105">**To handle Rich Text Format for outgoing messages, gateways**</span><span class="sxs-lookup"><span data-stu-id="de1ce-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="de1ce-106">Rufen Sie nur die eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) einer Nachricht aus dem Nachrichtenspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="de1ce-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="de1ce-107">Der Hauptvorteil beim Abrufen nur der **PR_RTF_COMPRESSED-Eigenschaft** ist, dass der Nachrichtentext nicht zwischen Computern gesendet werden muss, wenn das Gateway und der Nachrichtenspeicher auf verschiedenen Computern vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="de1ce-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="de1ce-108">Generieren Sie den Nachrichtentext aus dem formatierten Text entweder durch Aufrufen der RTF-Bibliotheksfunktion **HrTextFromCompressedRTFStream** oder, wenn die Nachricht lokal gespeichert wird, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="de1ce-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="de1ce-109">Das RTF_SYNC_RTF_CHANGED sollte im Aufruf von **RTFSync festgelegt werden.**</span><span class="sxs-lookup"><span data-stu-id="de1ce-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="de1ce-110">Weitere Informationen finden Sie unter [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="de1ce-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="de1ce-111">Nehmen Sie unwiderrufliche Änderungen am Nachrichtentext vor, z. B. das Ablegen nicht unterstützter Zeichen.</span><span class="sxs-lookup"><span data-stu-id="de1ce-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="de1ce-112">Stellen Sie **sicher, PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) und alle #A0 entweder festgelegt oder nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="de1ce-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="de1ce-113">Wenn Änderungen vorgenommen wurden, rufen Sie **RTFSync** auf, RTF_SYNC_RTF_CHANGED und RTF_SYNC_BODY_CHANGED festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="de1ce-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="de1ce-114">**RTFSync** berechnet die rtF-Hilfseigenschaften aus dem geänderten Text neu.</span><span class="sxs-lookup"><span data-stu-id="de1ce-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="de1ce-115">Nehmen Sie umkehrbare Änderungen am Nachrichtentext vor, z. B. das Einfügen von Anlagenplatzhaltern und das Ausführen von nicht destruktiven Codeseitenkonvertierungen.</span><span class="sxs-lookup"><span data-stu-id="de1ce-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="de1ce-116">Senden Sie die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="de1ce-116">Send the message.</span></span>
    
 <span data-ttu-id="de1ce-117">**To handle Rich Text Format for incoming messages, gateways**</span><span class="sxs-lookup"><span data-stu-id="de1ce-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="de1ce-118">Rückgängig machen sie alle Änderungen am Nachrichtentext, die direkt vor dem Senden der Nachricht vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="de1ce-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="de1ce-119">Rufen **Sie RTFSync** auf, wenn die Nachricht die Eigenschaften **PR_RTF_COMPRESSED** und **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) enthält.</span><span class="sxs-lookup"><span data-stu-id="de1ce-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="de1ce-120">Aktualisieren Sie die Nachricht im Nachrichtenspeicher mit **der PR_RTF_COMPRESSED-Eigenschaft,** wenn die Nachricht sie enthält. nur dann mit **der PR_BODY-Eigenschaft** **aktualisieren, PR_RTF_COMPRESSED** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de1ce-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="de1ce-121">Verwerfen **PR_BODY,** wenn die Nachricht sowohl diese Eigenschaft als auch **PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="de1ce-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="de1ce-122">Gateways rufen **RTFSync auf,** um die Übertragung des Nachrichtentexts und des formatierten Texts zu vermeiden, wenn sich der Nachrichtenspeicher auf einem anderen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="de1ce-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="de1ce-123">Wenn das Gateway lokal ist, kann es beide Eigenschaften festlegen und dem Nachrichtenspeicher erlauben, die Synchronisierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="de1ce-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

