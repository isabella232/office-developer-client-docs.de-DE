---
title: Unterstützung von formatierten Text in eingehenden Nachrichten Client Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19795669"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="8af40-103">Unterstützung von formatiertem Text in eingehenden Nachrichten: Kundenaufgaben</span><span class="sxs-lookup"><span data-stu-id="8af40-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="8af40-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8af40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8af40-105">Wie Nachrichten zwischen messaging-Systemen übertragen werden, wird die MAPI-Warteschlange sichergestellt, dass die rich-Text-Formatierung mit den Nachrichtentext synchronisiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="8af40-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="8af40-106">Die MAPI-Warteschlange Ruft die [RTFSync](rtfsync.md) -Funktion aus einer gepackten Version der Nachricht, die an der Adressbuchhierarchie übergeben.</span><span class="sxs-lookup"><span data-stu-id="8af40-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="8af40-107">Der Adressbuchhierarchie speichert die Änderungen an der Nachricht durch Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode ab und leitet sie an den neuen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="8af40-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="8af40-108">Wenn RTF-fähigen Clientanwendung der Empfänger die Nachricht für die Textanzeige geöffnet wird, müssen sie den Text mit der Formatierung synchronisieren und öffnen **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , je nachdem, welche Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8af40-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="8af40-109">**Öffnen eine Nachricht, RTF-fähigen clients**</span><span class="sxs-lookup"><span data-stu-id="8af40-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="8af40-110">Rufen Sie **RTFSync** zum Synchronisieren von des Nachrichtentexts mit der Formatierung an, wenn der Nachrichtenspeicher nicht RTF-kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8af40-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="8af40-111">Das Flag RTF_SYNC_BODY_CHANGED sollte im _UlFlags_ -Parameter übergeben werden, wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))-Eigenschaft ist nicht vorhanden, oder auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8af40-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="8af40-112">Arbeiten mit RTF-fähigen Nachrichtenspeicher Clients müssen nicht die **RTFSync** aufrufen, da der Nachrichtenspeicher davon kümmert.</span><span class="sxs-lookup"><span data-stu-id="8af40-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="8af40-113">Rufen Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , wenn der Nachrichtentext aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8af40-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="8af40-114">Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8af40-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="8af40-115">Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie die Eigenschaft **PR_BODY** stattdessen öffnen, um den Nachrichteninhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8af40-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="8af40-116">Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion, um eine nicht komprimierten Version der komprimierten RTF-Daten zu erstellen, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8af40-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="8af40-117">Der nicht komprimierten RTF-Daten oder die nur-Text-Daten für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8af40-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="8af40-118">**RTFSync** gibt einen booleschen Wert, der angibt, ob die Nachricht wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8af40-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="8af40-119">Wenn dieser Wert "true" zurückgibt, rufen Sie **SaveChanges** zu einem bestimmten Zeitpunkt an das Update dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8af40-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="8af40-120">Der Anruf hat keinen getroffen werden, unmittelbar nachdem **RTFSync** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8af40-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8af40-121">Da so viele Komponenten den formatierten Text behandelt werden, bevor Sie es erhalten, besteht die Möglichkeit, eine Beschädigung.</span><span class="sxs-lookup"><span data-stu-id="8af40-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="8af40-122">Diese Beschädigung konnte der Informationsdienst Nachricht, einer Drittanbieter-Anwendung, ein Gateway oder ein Fehler bei der Übertragung stammen.</span><span class="sxs-lookup"><span data-stu-id="8af40-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

