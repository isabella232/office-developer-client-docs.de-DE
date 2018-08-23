---
title: Bereitstellen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577520"
---
# <a name="posting-a-message"></a><span data-ttu-id="b1932-103">Bereitstellen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="b1932-103">Posting a message</span></span>

<span data-ttu-id="b1932-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1932-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1932-105">Bereitstellen einer Nachricht ähnelt dem Senden einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b1932-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="b1932-106">Der Hauptunterschied ist das Ziel.</span><span class="sxs-lookup"><span data-stu-id="b1932-106">The main difference is the destination.</span></span> <span data-ttu-id="b1932-107">Statt weitergeleitet werden ein oder mehrere Empfänger über eine oder mehrere von Messagingsystemen, bleibt eine bereitgestellte Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="b1932-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="b1932-108">Zum Übermitteln einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="b1932-108">To post a message</span></span>
  
1. <span data-ttu-id="b1932-109">Öffnen Sie den Zielordner durch Aufrufen von [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b1932-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="b1932-110">Wenn der Zielordner des Posteingangs ist, suchen Sie die Eintrags-ID durch Aufrufen von [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)an **OpenEntry** übergeben.</span><span class="sxs-lookup"><span data-stu-id="b1932-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="b1932-111">Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) , um die Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1932-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="b1932-112">Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b1932-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="b1932-113">Das Flag MSGFLAG_READ in der Eigenschaft **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1932-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="b1932-114">Die **PR_SENDER** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1932-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="b1932-115">Die **PR_SENT_REPRESENTING** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1932-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="b1932-116">Die Eigenschaft **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1932-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="b1932-117">Das **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die Eigenschaft **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1932-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="b1932-118">Die Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1932-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="b1932-119">Die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1932-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="b1932-120">Alle Eigenschaften, die von der Nachrichtenklasse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1932-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="b1932-121">Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b1932-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="b1932-122">Falls erforderlich, erstellen Sie eine Anlage, legen Sie dessen Eigenschaften und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="b1932-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="b1932-123">Weitere Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="b1932-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="b1932-124">Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b1932-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="b1932-125">Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Zielordners angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1932-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="b1932-126">Beachten Sie, dass Sie keine Empfängerliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1932-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="b1932-127">Stattdessen legen Sie verschiedene Eigenschaften, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b1932-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="b1932-128">Wenn eine Nachricht speichern zeitweise bevor er in der Inhaltstabelle des Ordners "sichtbar" angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen und anschließend in den Zielordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="b1932-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

