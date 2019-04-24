---
title: Veröffentlichen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350750"
---
# <a name="posting-a-message"></a><span data-ttu-id="672e2-103">Veröffentlichen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="672e2-103">Posting a message</span></span>

<span data-ttu-id="672e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="672e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="672e2-105">Das Veröffentlichen einer Nachricht ähnelt dem Senden einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="672e2-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="672e2-106">Der Hauptunterschied ist das Ziel.</span><span class="sxs-lookup"><span data-stu-id="672e2-106">The main difference is the destination.</span></span> <span data-ttu-id="672e2-107">Anstatt an einen oder mehrere Empfänger über ein oder mehrere Messagingsysteme umgeleitet zu werden, verbleibt eine bereitgestellte Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="672e2-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="672e2-108">So veröffentlichen Sie eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="672e2-108">To post a message</span></span>
  
1. <span data-ttu-id="672e2-109">Öffnen Sie den Zielordner, indem Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="672e2-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="672e2-110">Wenn der Zielordner der Posteingang ist, suchen Sie nach der Eintrags \*\*\*\* -ID, die an OpenEntry durch Aufrufen von [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="672e2-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="672e2-111">Rufen Sie [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf, um die Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="672e2-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="672e2-112">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Nachricht auf, um Folgendes festzulegen:</span><span class="sxs-lookup"><span data-stu-id="672e2-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="672e2-113">Das MSGFLAG_READ-flag in der **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="672e2-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="672e2-114">Die **PR_SENDER** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="672e2-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="672e2-115">Die **PR_SENT_REPRESENTING** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="672e2-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="672e2-116">Die **PR_RECEIPT_TIME** ([pidtagreceipttime (](pidtagreceipttime-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="672e2-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="672e2-117">Die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="672e2-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="672e2-118">Die **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="672e2-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="672e2-119">Die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="672e2-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="672e2-120">Alle Eigenschaften, die für die Nachrichtenklasse erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="672e2-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="672e2-121">Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht auf, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="672e2-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="672e2-122">Erstellen Sie bei Bedarf eine Anlage, legen Sie Ihre Eigenschaften fest, und speichern Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="672e2-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="672e2-123">Weitere Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="672e2-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="672e2-124">Rufen Sie **IMessage:: SaveChanges** auf, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="672e2-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="672e2-125">An dieser Stelle wird Sie in der Tabelle Inhalt des Zielordners angezeigt.</span><span class="sxs-lookup"><span data-stu-id="672e2-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="672e2-126">Beachten Sie, dass Sie keine Empfängerliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="672e2-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="672e2-127">Stattdessen legen Sie mehrere Eigenschaften fest, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="672e2-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="672e2-128">Wenn Sie eine Nachricht zeitweise speichern möchten, bevor Sie in der Tabelle Inhalt des sichtbaren Ordners angezeigt wird, erstellen Sie Sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie Sie dann in den Zielordner.</span><span class="sxs-lookup"><span data-stu-id="672e2-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

