---
title: Senden von Nachrichten mithilfe von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795489"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="e409e-103">Senden von Nachrichten mithilfe von MAPI</span><span class="sxs-lookup"><span data-stu-id="e409e-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="e409e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e409e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e409e-105">Clientanwendungen rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode, um eine Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e409e-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="e409e-106">**SubmitMessage** ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , um die Nachricht vor der Weiterleitung Steuerelement entweder der MAPI-Warteschlange oder direkt an eines Transportdienstes zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e409e-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="e409e-107">Die MAPI-Warteschlange empfängt die Nachricht, wenn eines der folgenden auftreten:</span><span class="sxs-lookup"><span data-stu-id="e409e-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="e409e-108">Die Nachrichtenanbieter und Adressbuchhierarchie sind nicht eng verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e409e-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="e409e-109">Die Nachricht muss der vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e409e-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="e409e-110">Die eng gekoppelten Nachrichtenspeicher und Transport können nicht alle Empfänger behandeln, die an die Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="e409e-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="e409e-111">Ein eng gekoppelten Nachrichtenspeicher muss eine Nachricht den Status berücksichtigen, bevor sie es für die MAPI-Warteschlange auf eines Transportdienstes heruntergeladen werden anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e409e-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="e409e-112">Es gibt Situationen, in dem möglicherweise eine Meldung angezeigt, die MAPI-Warteschlange erforderlich ist, aber die MAPI-Warteschlange sollte wirklich nicht einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e409e-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="e409e-113">Betrachten Sie beispielsweise die Situation, in dem ein Benutzer eine Nachricht aus dem Posteingang übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e409e-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="e409e-114">Der Client ist eng gekoppelten Speicher und Transport verwendet.</span><span class="sxs-lookup"><span data-stu-id="e409e-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="e409e-115">Wenn der eng gekoppelten Nachrichtenspeicher Speicherort der Nachricht als einzige Kriterium für um dazu, ob die MAPI-Warteschlange zu entscheiden verwendet, um die Nachricht zu verarbeiten, erhält die MAPI-Warteschlange immer die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e409e-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="e409e-116">Um diese Art des Problems zu vermeiden, muss ein eng gekoppelten Nachrichtenspeicher neben den Speicherort für Nachrichten die Nachricht den Status überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e409e-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="e409e-117">Der Transportdienst sollten insbesondere nicht anfordern, dass die MAPI-Warteschlange eine beliebige Nachricht herunterladen, die aktiv übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e409e-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="e409e-118">Die Übertragung Nachricht umfasst die Nachricht Speicheranbieter, mindestens einen Transportanbieter und MAPI.</span><span class="sxs-lookup"><span data-stu-id="e409e-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="e409e-119">Die Themen in diesem Abschnitt enthalten ausführliche Informationen zu speziellen Positionen bei der Übertragung.</span><span class="sxs-lookup"><span data-stu-id="e409e-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e409e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e409e-120">See also</span></span>



[<span data-ttu-id="e409e-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e409e-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e409e-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e409e-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

