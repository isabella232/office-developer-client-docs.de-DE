---
title: Senden von Nachrichten mithilfe von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438722"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="e8574-103">Senden von Nachrichten mithilfe von MAPI</span><span class="sxs-lookup"><span data-stu-id="e8574-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="e8574-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8574-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8574-105">Clientanwendungen rufen die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="e8574-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="e8574-106">**SubmitMessage ruft** [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern, bevor die Steuerung an den MAPI-Spooler oder direkt an einen Transportanbieter übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="e8574-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="e8574-107">Der MAPI-Spooler empfängt die Nachricht, wenn eine der folgenden Fehler auftritt:</span><span class="sxs-lookup"><span data-stu-id="e8574-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="e8574-108">Der Nachrichtenspeicheranbieter und der Transportanbieter sind nicht eng gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="e8574-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="e8574-109">Die Nachricht erfordert eine Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e8574-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="e8574-110">Der eng gekoppelte Nachrichtenspeicher und -transport kann nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="e8574-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="e8574-111">Ein eng gekoppelter Nachrichtenspeicher muss den Status einer Nachricht berücksichtigen, bevor er sie dem MAPI-Spooler zum Herunterladen an einen Transportanbieter präsentiert.</span><span class="sxs-lookup"><span data-stu-id="e8574-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="e8574-112">Es gibt Situationen, in denen eine Nachricht möglicherweise den MAPI-Spooler erfordert, aber der MAPI-Spooler sollte wirklich nicht beteiligt sein.</span><span class="sxs-lookup"><span data-stu-id="e8574-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="e8574-113">Betrachten Sie beispielsweise die Situation, in der ein Benutzer eine Nachricht aus dem Posteingang sendet.</span><span class="sxs-lookup"><span data-stu-id="e8574-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="e8574-114">Der Client verwendet einen eng gekoppelten Speicher und Transport.</span><span class="sxs-lookup"><span data-stu-id="e8574-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="e8574-115">Wenn der eng gekoppelte Nachrichtenspeicher den Speicherort der Nachricht als einziges Kriterium für die Entscheidung verwendet, ob der MAPI-Spooler die Nachricht verarbeiten soll, erhält der MAPI-Spooler immer die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e8574-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="e8574-116">Um diese Art von Problem zu vermeiden, muss ein eng gekoppelter Nachrichtenspeicher zusätzlich zum Nachrichtenspeicherort den Nachrichtenstatus überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e8574-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="e8574-117">Insbesondere sollte der Transportanbieter nicht anfordern, dass der MAPI-Spooler aktiv übermittelte Nachrichten herunterloaden muss.</span><span class="sxs-lookup"><span data-stu-id="e8574-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="e8574-118">Der Nachrichtenübermittlungsprozess umfasst den Nachrichtenspeicheranbieter, einen oder mehrere Transportanbieter und MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8574-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="e8574-119">Die Themen in diesem Abschnitt enthalten detaillierte Informationen zu bestimmten Rollen im Nachrichtenübermittlungsprozess.</span><span class="sxs-lookup"><span data-stu-id="e8574-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8574-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8574-120">See also</span></span>



[<span data-ttu-id="e8574-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e8574-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e8574-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e8574-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

