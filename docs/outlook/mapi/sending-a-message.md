---
title: Senden einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68a842ccfdaea8ecdb975e1c510711b0e43fd576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795465"
---
# <a name="sending-a-message"></a><span data-ttu-id="ebef0-103">Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ebef0-103">Sending a Message</span></span>

  
  
<span data-ttu-id="ebef0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebef0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebef0-105">Wenn Sie eine Nachricht senden möchten, rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ebef0-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="ebef0-106">**SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und das Flag MSGFLAG_SUBMIT in der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebef0-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ebef0-107">Die Nachricht Speicheranbieter gibt, wenn eng mit eines Transportdienstes verknüpft die Nachricht direkt an die Übertragung, die es an die messaging-System übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ebef0-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="ebef0-108">Wenn dies nicht eng gekoppelt, der Speicheranbieter Nachricht informiert die MAPI-Warteschlange, die die ausgehende Warteschlange geändert hat und die MAPI-Warteschlange übermittelt die Nachricht an einen entsprechenden Transport-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ebef0-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="ebef0-109">Wenn Sie einen Sendevorgang Abbrechen Benutzern ermöglichen, rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) , um dieses Feature zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ebef0-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="ebef0-110">**AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="ebef0-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="ebef0-111">Können Benutzer so beenden Sie einen Send auftritt, bis die Nachricht an die zugrunde liegenden messaging-System erhält.</span><span class="sxs-lookup"><span data-stu-id="ebef0-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="ebef0-112">Wenn **SubmitMessage** MAPI_E_CORRUPT_DATA zurückgibt, wird davon ausgegangen Sie, dass die gesendeten Daten ist jetzt verloren.</span><span class="sxs-lookup"><span data-stu-id="ebef0-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="ebef0-113">Bevor Sie versuchen, ein zweites Mal senden, müssen schreiben Sie die Nachricht erneut durch Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="ebef0-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="ebef0-114">Für den Benutzer ein Fehler angezeigt, wenn diese **IMAPIProp** Aufrufe fehlschlagen oder **SubmitMessage** ein zweites Mal fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ebef0-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="ebef0-115">Freien Sie nach einem erfolgreichen Aufruf von **SubmitMessage**Speicher, für die Empfängerliste zugewiesen wurde, und freigeben Sie die Nachricht und ihre Anhänge.</span><span class="sxs-lookup"><span data-stu-id="ebef0-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="ebef0-116">Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Operationen auf den Zeiger für diese Objekte.</span><span class="sxs-lookup"><span data-stu-id="ebef0-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="ebef0-117">Die einzige Ausnahme ist **IUnknown**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ebef0-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="ebef0-118">Keine anderen Aufrufe sind zulässig, da viele Nachricht Anbieter Eintragsbezeichner für Nachrichten für ungültig erklärt, die gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ebef0-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

