---
title: Bereitstellen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795315"
---
# <a name="posting-a-message"></a><span data-ttu-id="d733d-103">Bereitstellen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="d733d-103">Posting a message</span></span>

<span data-ttu-id="d733d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d733d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d733d-105">Bereitstellen einer Nachricht ähnelt dem Senden einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d733d-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="d733d-106">Der Hauptunterschied ist das Ziel.</span><span class="sxs-lookup"><span data-stu-id="d733d-106">The main difference is the destination.</span></span> <span data-ttu-id="d733d-107">Statt weitergeleitet werden ein oder mehrere Empfänger über eine oder mehrere von Messagingsystemen, bleibt eine bereitgestellte Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="d733d-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="d733d-108">Zum Übermitteln einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="d733d-108">To post a message</span></span>
  
1. <span data-ttu-id="d733d-109">Öffnen Sie den Zielordner durch Aufrufen von [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d733d-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="d733d-110">Wenn der Zielordner des Posteingangs ist, suchen Sie die Eintrags-ID durch Aufrufen von [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)an **OpenEntry** übergeben.</span><span class="sxs-lookup"><span data-stu-id="d733d-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="d733d-111">Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) , um die Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d733d-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="d733d-112">Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d733d-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="d733d-113">Das Flag MSGFLAG_READ in der Eigenschaft **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d733d-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d733d-114">Die **PR_SENDER** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d733d-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="d733d-115">Die **PR_SENT_REPRESENTING** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d733d-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="d733d-116">Die Eigenschaft **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d733d-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d733d-117">Das **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die Eigenschaft **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d733d-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d733d-118">Die Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d733d-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d733d-119">Die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d733d-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d733d-120">Alle Eigenschaften, die von der Nachrichtenklasse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d733d-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="d733d-121">Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d733d-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="d733d-122">Falls erforderlich, erstellen Sie eine Anlage, legen Sie dessen Eigenschaften und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="d733d-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="d733d-123">Weitere Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="d733d-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="d733d-124">Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d733d-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="d733d-125">Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Zielordners angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d733d-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="d733d-126">Beachten Sie, dass Sie keine Empfängerliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="d733d-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="d733d-127">Stattdessen legen Sie verschiedene Eigenschaften, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="d733d-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="d733d-128">Wenn eine Nachricht speichern zeitweise bevor er in der Inhaltstabelle des Ordners "sichtbar" angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen und anschließend in den Zielordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="d733d-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

