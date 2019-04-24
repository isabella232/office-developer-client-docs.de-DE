---
title: Senden einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339746"
---
# <a name="sending-a-message"></a><span data-ttu-id="cd932-103">Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="cd932-103">Sending a Message</span></span>

  
  
<span data-ttu-id="cd932-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd932-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd932-105">Wenn Sie bereit sind, eine Nachricht zu senden, rufen Sie die zugehörige [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="cd932-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="cd932-106">**SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und legt das MSGFLAG_SUBMIT-Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="cd932-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="cd932-107">Wenn der Nachrichtenspeicher Anbieter eng mit einem Transportanbieter gekoppelt ist, gibt er die Nachricht direkt an den Transport, der Sie an das Messagingsystem übermittelt.</span><span class="sxs-lookup"><span data-stu-id="cd932-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="cd932-108">Wenn nicht eng gekoppelt, informiert der Nachrichtenspeicher Anbieter die MAPI-Spooler, dass die ausgehende Warteschlange geändert wurde und der MAPI-Spooler die Nachricht an einen geeigneten Transportanbieter überträgt.</span><span class="sxs-lookup"><span data-stu-id="cd932-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="cd932-109">Wenn Sie Benutzern das Abbrechen eines Sendevorgangs gestatten, rufen Sie [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) auf, um dieses Feature zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="cd932-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="cd932-110">**AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="cd932-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="cd932-111">Benutzer können das Senden von Ereignissen beenden, bis die Nachricht an das zugrunde liegende Messagingsystem gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd932-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="cd932-112">Wenn **SUBMITMESSAGE** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gesendeten Daten jetzt verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="cd932-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="cd932-113">Bevor Sie versuchen, ein zweites Mal zu senden, schreiben Sie die Nachricht erneut, indem Sie [IMAPIProp::](imapiprop-setprops.md) SetProps und [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cd932-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="cd932-114">Zeigt dem Benutzer einen Fehler an, wenn diese **IMAPIProp** -Aufrufe fehlschlagen oder wenn **SubmitMessage** ein zweites Mal fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cd932-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="cd932-115">Geben Sie nach einem erfolgreichen Anruf bei **SubmitMessage**den Speicherplatz frei, der für die Empfängerliste reserviert wurde, und geben Sie die Nachricht und ihre Anlagen frei.</span><span class="sxs-lookup"><span data-stu-id="cd932-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="cd932-116">Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Vorgänge für die Zeiger für diese Objekte zu.</span><span class="sxs-lookup"><span data-stu-id="cd932-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="cd932-117">Die einzige Ausnahme ist das Aufrufen von **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="cd932-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="cd932-118">Es sind keine weiteren Anrufe zulässig, da viele Nachrichtenspeicher Anbieter Eintragsbezeichner für gesendete Nachrichten ungültig machen.</span><span class="sxs-lookup"><span data-stu-id="cd932-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

