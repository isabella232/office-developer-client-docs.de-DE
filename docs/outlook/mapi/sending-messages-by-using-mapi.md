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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339753"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="bbf10-103">Senden von Nachrichten mithilfe von MAPI</span><span class="sxs-lookup"><span data-stu-id="bbf10-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="bbf10-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbf10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbf10-105">Client Anwendungen rufen die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um eine Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="bbf10-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="bbf10-106">**SubmitMessage** ruft [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern, bevor die Steuerung an den MAPI-Spooler oder direkt an einen Transportanbieter übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="bbf10-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="bbf10-107">Der MAPI-Spooler empfängt die Nachricht, wenn eine der folgenden Aktionen Eintritt:</span><span class="sxs-lookup"><span data-stu-id="bbf10-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="bbf10-108">Der Nachrichtenspeicher Anbieter und der Transportanbieter sind nicht eng gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="bbf10-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="bbf10-109">Die Nachricht erfordert die Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="bbf10-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="bbf10-110">Der eng gekoppelte Nachrichtenspeicher und der Transport können nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="bbf10-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="bbf10-111">Bei einem eng gekoppelten Nachrichtenspeicher muss der Status einer Nachricht berücksichtigt werden, bevor Sie dem MAPI-Spooler zum Herunterladen an einen Transportanbieter präsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="bbf10-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="bbf10-112">Es gibt Situationen, in denen eine Nachricht möglicherweise die MAPI-Spooler erfordert, aber die MAPI-Spooler sollte wirklich nicht beteiligt sein.</span><span class="sxs-lookup"><span data-stu-id="bbf10-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="bbf10-113">Betrachten Sie beispielsweise die Situation, in der ein Benutzer eine Nachricht aus dem Posteingang übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bbf10-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="bbf10-114">Der Client verwendet einen eng gekoppelten Speicher und Transport.</span><span class="sxs-lookup"><span data-stu-id="bbf10-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="bbf10-115">Wenn der eng gekoppelte Nachrichtenspeicher den Speicherort der Nachricht als alleiniges Kriterium verwendet, um zu entscheiden, ob der MAPI-Spooler die Nachricht verarbeiten darf, wird die Nachricht vom MAPI-Spooler immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbf10-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="bbf10-116">Um diese Art von Problem zu vermeiden, muss ein eng gekoppelter Nachrichtenspeicher zusätzlich zum Nachrichten Speicherort den Nachrichtenstatus überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bbf10-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="bbf10-117">Insbesondere sollte der Transportanbieter nicht anfordern, dass der MAPI-Spooler eine Nachricht herunterlädt, die aktiv übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bbf10-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="bbf10-118">Der Nachrichtenübertragungsprozess umfasst den Nachrichtenspeicher Anbieter, einen oder mehrere Transportanbieter und MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbf10-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="bbf10-119">Die Themen in diesem Abschnitt enthalten detaillierte Informationen zu bestimmten Rollen im Nachrichtenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="bbf10-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbf10-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbf10-120">See also</span></span>



[<span data-ttu-id="bbf10-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="bbf10-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="bbf10-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bbf10-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

