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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423622"
---
# <a name="sending-a-message"></a><span data-ttu-id="be3a6-103">Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="be3a6-103">Sending a Message</span></span>

  
  
<span data-ttu-id="be3a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be3a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be3a6-105">Wenn Sie zum Senden einer Nachricht bereit sind, rufen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf.</span><span class="sxs-lookup"><span data-stu-id="be3a6-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="be3a6-106">**SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und legt das MSGFLAG_SUBMIT-Flag in der **PR_MESSAGE_FLAGS** - Eigenschaft der Nachricht ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) fest.</span><span class="sxs-lookup"><span data-stu-id="be3a6-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="be3a6-107">Wenn der Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist, übergibt die Nachricht die Nachricht direkt an den Transport, der sie an das Messagingsystem übermittelt.</span><span class="sxs-lookup"><span data-stu-id="be3a6-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="be3a6-108">Wenn nicht eng gekoppelt, informiert der Nachrichtenspeicheranbieter den MAPI-Spooler, dass die ausgehende Warteschlange geändert wurde, und der MAPI-Spooler überträgt die Nachricht an einen geeigneten Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="be3a6-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="be3a6-109">Wenn Sie Benutzern das Abbrechen eines Sendevorgangs erlauben, rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) auf, um dieses Feature zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="be3a6-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="be3a6-110">**AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="be3a6-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="be3a6-111">Benutzer können das Senden beenden, bis die Nachricht an das zugrunde liegende Messagingsystem gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="be3a6-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="be3a6-112">Wenn **SubmitMessage** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gesendeten Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="be3a6-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="be3a6-113">Bevor Sie versuchen, ein zweites Mal zu senden, schreiben Sie die Nachricht erneut, indem Sie [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::SaveChanges aufrufen.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="be3a6-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="be3a6-114">Zeigt dem Benutzer einen Fehler an, wenn diese **IMAPIProp-Aufrufe** fehlschlagen oder **wenn SubmitMessage** ein zweites Mal fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="be3a6-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="be3a6-115">Geben Sie nach einem erfolgreichen Aufruf von **SubmitMessage** den für die Empfängerliste zugewiesenen Arbeitsspeicher frei, und geben Sie die Nachricht und ihre Anlagen frei.</span><span class="sxs-lookup"><span data-stu-id="be3a6-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="be3a6-116">Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Vorgänge an den Zeigern für diese Objekte zu.</span><span class="sxs-lookup"><span data-stu-id="be3a6-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="be3a6-117">Die einzige Ausnahme ist das Aufrufen **von IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="be3a6-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="be3a6-118">Es sind keine weiteren Aufrufe zulässig, da viele Nachrichtenspeicheranbieter Eingabebezeichner für gesendete Nachrichten ungültig machen.</span><span class="sxs-lookup"><span data-stu-id="be3a6-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

