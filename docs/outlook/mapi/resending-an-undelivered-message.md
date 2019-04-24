---
title: Erneutes Senden einer nicht zugestellten Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328679"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="22380-103">Erneutes Senden einer nicht zugestellten Nachricht</span><span class="sxs-lookup"><span data-stu-id="22380-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="22380-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22380-105">Ein Transportanbieter sendet einen Unzustellbarkeitsbericht (NDR), wenn er eine von Ihnen übermittelte Nachricht nicht erfolgreich übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="22380-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="22380-106">Es liegt beim Client, ob Benutzer versuchen können, diese nicht zugestellten Nachrichten erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="22380-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="22380-107">Wenn Sie das erneute Senden von Nachrichten unterstützen, können Sie entweder ein von MAPI bereitgestelltes Formular verwenden oder Ihre eigenen implementieren.</span><span class="sxs-lookup"><span data-stu-id="22380-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="22380-108">Das MAPI-Formular zeigt die Namen der fehlgeschlagenen Empfänger und den Grund für den Übermittlungsfehler an, sofern möglich, und enthält eine Schaltfläche, die es einem Benutzer ermöglicht, die Nachricht erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="22380-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="22380-109">Wenn eine erneut gesendete Nachricht empfangen wird, sollte Sie genau wie die ursprüngliche Nachricht aussehen.</span><span class="sxs-lookup"><span data-stu-id="22380-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="22380-110">Der Empfänger sollte nicht zwischen einer Nachricht unterscheiden können, die beim ersten Übertragungsversuch oder einem nachfolgenden Versuch zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="22380-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="22380-111">Antworten auf diese Nachricht sollten genau so funktionieren, als ob die Nachricht beim ersten Mal erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="22380-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="22380-112">So senden Sie eine nicht zugestellte Nachricht erneut</span><span class="sxs-lookup"><span data-stu-id="22380-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="22380-113">Rufen Sie [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf, um eine neue Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22380-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="22380-114">Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, ohne die \* \* PR_MESSAGE_RECIPIENTS \* \* ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft, und die Eigenschaften **PR_SENDER** und **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="22380-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="22380-115">Nehmen Sie die folgenden Eigenschaftsänderungen vor:</span><span class="sxs-lookup"><span data-stu-id="22380-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="22380-116">Legen Sie **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) auf die \* \* PR_ORIG_MESSAGE_CLASS \* \* ([pidtagoriginalmessageclass (](pidtagoriginalmessageclass-canonical-property.md))-Eigenschaft des Berichts fest.</span><span class="sxs-lookup"><span data-stu-id="22380-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="22380-117">Legen Sie das MSGFLAG_RESEND-Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="22380-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="22380-118">Legen Sie **PR_ORIGINAL_ENTRYID** ([pidtagoriginalentryid (](pidtagoriginalentryid-canonical-property.md)) auf die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft der ursprünglichen Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="22380-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="22380-119">Legen Sie für jeden Empfänger MAPI_SUBMITTED in der **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="22380-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="22380-120">Duplizieren Sie jeden fehlerhaften Empfänger.</span><span class="sxs-lookup"><span data-stu-id="22380-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="22380-121">Ändern Sie die **PR_RECIPIENT_TYPE** -Eigenschaft für den doppelten Empfänger in MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="22380-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="22380-122">Daher gibt es für jeden fehlerhaften Empfänger nun zwei Einträge in der Empfängertabelle: eine mit **PR_RECIPIENT_TYPE** , die auf den ursprünglichen Wert festgelegt ist, und die andere, wobei **PR_RECIPIENT_TYPE** auf MAPI_P1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22380-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="22380-123">Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md) auf, um die Unterhaltungs Verfolgung bei Bedarf einzurichten.</span><span class="sxs-lookup"><span data-stu-id="22380-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="22380-124">Rufen Sie die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode der neuen Nachricht auf, um die Empfängerliste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22380-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="22380-125">Rufen Sie [IMessage:: SubmitMessage](imessage-submitmessage.md) auf, um die neue Nachricht zu speichern und zu senden.</span><span class="sxs-lookup"><span data-stu-id="22380-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

