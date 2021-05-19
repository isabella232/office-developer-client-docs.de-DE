---
title: Unterstützen von formatierten Text in Clientaufgaben für eingehende Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434501"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="5f002-103">Unterstützen von formatierten Text in eingehenden Nachrichten: Clientzu zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="5f002-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="5f002-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f002-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f002-105">Wenn Nachrichten zwischen Messagingsystemen übertragen werden, stellt der MAPI-Spooler sicher, dass die Rich-Text-Formatierung mit dem Nachrichtentext synchronisiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="5f002-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="5f002-106">Der MAPI-Spooler ruft die [RTFSync-Funktion](rtfsync.md) innerhalb einer umschlossenen Version der Nachricht auf, die er an den Transportanbieter übergibt.</span><span class="sxs-lookup"><span data-stu-id="5f002-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="5f002-107">Der Transportanbieter speichert die an der Nachricht vorgenommenen Änderungen, indem er die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aufruft und diese dann an den neuen Empfänger weiter leitet.</span><span class="sxs-lookup"><span data-stu-id="5f002-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="5f002-108">Wenn die **#A0** des Empfängers die Nachricht zum Anzeigen des Texts öffnet, muss sie den Text mit der Formatierung synchronisieren und entweder PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) öffnen, je nachdem, welche Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5f002-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="5f002-109">**Um eine Nachricht zu öffnen, verwenden RTF-bewusste Clients**</span><span class="sxs-lookup"><span data-stu-id="5f002-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="5f002-110">Rufen **Sie RTFSync** auf, um den Nachrichtentext mit der Formatierung zu synchronisieren, wenn der Nachrichtenspeicher nicht RTF-bewusst ist.</span><span class="sxs-lookup"><span data-stu-id="5f002-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="5f002-111">Das RTF_SYNC_BODY_CHANGED sollte im  _ulFlags-Parameter_ übergeben werden, wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) -Eigenschaft fehlt oder auf FALSE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5f002-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="5f002-112">Clients, die mit RTF-benachrichtigungsspeichern arbeiten, müssen den **RTFSync-Aufruf** nicht senden, da der Nachrichtenspeicher ihn übernimmt.</span><span class="sxs-lookup"><span data-stu-id="5f002-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="5f002-113">Rufen [Sie IMAPIProp::SaveChanges auf,](imapiprop-savechanges.md) wenn der Nachrichtentext aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f002-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="5f002-114">Rufen [Sie IMAPIProp::OpenProperty auf,](imapiprop-openproperty.md) um die **PR_RTF_COMPRESSED** öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f002-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="5f002-115">Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, sollten Sie die **PR_BODY** öffnen, um den Nachrichteninhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5f002-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="5f002-116">Rufen Sie [die WrapCompressedRTFStream-Funktion auf,](wrapcompressedrtfstream.md) um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f002-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="5f002-117">Zeigen Sie dem Benutzer die nicht komprimierten RTF-Daten oder die Nur-Text-Daten an.</span><span class="sxs-lookup"><span data-stu-id="5f002-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="5f002-118">**RTFSync** gibt einen booleschen Wert zurück, der angibt, ob die Nachricht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f002-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="5f002-119">Wenn dieser Wert TRUE zurückgibt, rufen **Sie SaveChanges** an einem bestimmten Punkt auf, um das Update dauerhaft zu machen.</span><span class="sxs-lookup"><span data-stu-id="5f002-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="5f002-120">Der Aufruf muss nicht unmittelbar nach der Rückgabe von **RTFSync** vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5f002-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5f002-121">Da so viele Komponenten den formatierten Text verarbeiten, bevor Sie ihn erhalten, besteht die Möglichkeit einer Beschädigung.</span><span class="sxs-lookup"><span data-stu-id="5f002-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="5f002-122">Diese Beschädigung kann vom Nachrichtenspeicheranbieter, einer Drittanbieteranwendung, einem Gateway oder einem Übertragungsfehler stammen.</span><span class="sxs-lookup"><span data-stu-id="5f002-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

