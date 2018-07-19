---
title: Erneutes Senden einer Nachricht nicht zugestellte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795377"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="c0c89-103">Erneutes Senden einer Nachricht nicht zugestellte</span><span class="sxs-lookup"><span data-stu-id="c0c89-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="c0c89-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0c89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0c89-105">Ein Transportdienstes sendet einen non-Delivery Report (NDR), wenn sie erfolgreich eine Nachricht übermitteln ist nicht möglich, die Sie gesendet haben.</span><span class="sxs-lookup"><span data-stu-id="c0c89-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="c0c89-106">Es ist Aufgabe der Client unabhängig davon, ob Benutzer versuchen können diese noch nicht übermittelten Nachrichten erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="c0c89-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="c0c89-107">Wenn Sie unterstützen können Erneutes Senden von Nachrichten, Sie entweder mithilfe eines Formulars bereitgestellt von MAPI oder implementieren Sie eine eigene.</span><span class="sxs-lookup"><span data-stu-id="c0c89-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="c0c89-108">Das MAPI-Formular zeigt die Namen der fehlgeschlagene Empfänger und den Grund für das Fehlschlagen der Übermittlung, wenn möglich, und enthält eine Schaltfläche, die bei Auswahl dieser Option ermöglicht einem Benutzer, die Nachricht erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="c0c89-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="c0c89-109">Wenn eine aktuellste Nachricht empfangen wird, sollte es genau wie die ursprüngliche Nachricht aussehen.</span><span class="sxs-lookup"><span data-stu-id="c0c89-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="c0c89-110">Der Empfänger sollte zur Unterscheidung zwischen einer Nachricht, die auf der ersten Versuch der Übertragung oder ein nachfolgender Versuch bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c0c89-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="c0c89-111">Antworten auf diese Nachricht sollte funktionieren, als ob die Nachricht erfolgreich beim ersten gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="c0c89-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="c0c89-112">Eine nicht zugestellte Nachricht erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="c0c89-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="c0c89-113">Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) zum Erstellen einer neuen Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="c0c89-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="c0c89-114">Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, ausgenommen die ** PR_MESSAGE_RECIPIENTS **-Eigenschaft ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) und die Eigenschaften **PR_SENDER** und **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="c0c89-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="c0c89-115">Nehmen Sie die folgende Eigenschaft Änderungen vor:</span><span class="sxs-lookup"><span data-stu-id="c0c89-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="c0c89-116">Legen Sie mit des Berichts **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ** PR_ORIG_MESSAGE_CLASS **-Eigenschaft ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0c89-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="c0c89-117">Legen Sie das MSGFLAG_RESEND-Flag in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0c89-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="c0c89-118">**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) auf die ursprüngliche Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0c89-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="c0c89-119">Legen Sie für jeden Empfänger MAPI_SUBMITTED in der Eigenschaft **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0c89-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="c0c89-120">Duplizieren Sie jeden fehlerhaften Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c0c89-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="c0c89-121">Ändern Sie die **PR_RECIPIENT_TYPE** -Eigenschaft für das duplizierte Empfänger in MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="c0c89-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="c0c89-122">Aus diesem Grund für jeden fehlerhaften Empfänger befinden sich jetzt zwei Einträge in der Tabelle Empfänger: eine Vorlage mit **PR_RECIPIENT_TYPE** auf den ursprünglichen Wert festgelegt und das andere mit **PR_RECIPIENT_TYPE** auf MAPI_P1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0c89-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="c0c89-123">Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md) So richten Sie bei Bedarf nachverfolgen Unterhaltung ein.</span><span class="sxs-lookup"><span data-stu-id="c0c89-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="c0c89-124">Rufen Sie die neue Nachricht [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode, um die Empfängerliste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c0c89-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="c0c89-125">Rufen Sie [IMessage::SubmitMessage](imessage-submitmessage.md) zum Speichern und senden Sie die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c0c89-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

