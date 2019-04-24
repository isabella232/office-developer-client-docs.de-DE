---
title: Behandeln von ausgehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342805"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="741b8-103">Behandeln von ausgehenden Nachrichten</span><span class="sxs-lookup"><span data-stu-id="741b8-103">Handling an outgoing message</span></span>

<span data-ttu-id="741b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="741b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="741b8-105">Eine ausgehende Nachricht ist eine Nachricht, die an einen oder mehrere Empfänger über ein oder mehrere Messagingsysteme gesendet oder in einem Ordner in einem Nachrichtenspeicher bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="741b8-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="741b8-106">Erstellen und Senden einer ausgehenden Nachricht</span><span class="sxs-lookup"><span data-stu-id="741b8-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="741b8-107">Öffnen Sie den Standardnachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="741b8-107">Open the default message store.</span></span> <span data-ttu-id="741b8-108">Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md) und [Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="741b8-109">Öffnen Sie den Ordner Postausgang.</span><span class="sxs-lookup"><span data-stu-id="741b8-109">Open the Outbox folder.</span></span> <span data-ttu-id="741b8-110">Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="741b8-111">Rufen Sie die **IMAPIFolder:: CreateMessage** -Methode des Postausgangs Ordners auf, um die neue Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="741b8-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="741b8-112">Weitere Informationen finden Sie unter [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="741b8-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="741b8-113">Erstellen Sie eine Empfängerliste mit einem oder mehreren gelösten Empfängern.</span><span class="sxs-lookup"><span data-stu-id="741b8-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="741b8-114">Weitere Informationen finden Sie unter [Erstellen einer Empfängerliste](creating-a-recipient-list.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="741b8-115">Optional können Sie einen Betreff hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="741b8-115">Optionally, add a subject.</span></span> <span data-ttu-id="741b8-116">Weitere Informationen finden Sie unter [Erstellen eines Nachrichtenbetreffs](creating-a-message-subject.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="741b8-117">Fügen Sie den Nachrichtentext hinzu.</span><span class="sxs-lookup"><span data-stu-id="741b8-117">Add the message text.</span></span> <span data-ttu-id="741b8-118">Weitere Informationen finden Sie unter [Creating Message Text](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="741b8-119">Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="741b8-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="741b8-120">Weitere Informationen finden Sie unter [Hinzufügen von Renderinformationen zu formatiertEm Text](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="741b8-121">Optional können Sie eine oder mehrere Anlagen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="741b8-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="741b8-122">Weitere Informationen finden Sie unter [Erstellen einer Nachrichtenanlage](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="741b8-123">Legen Sie andere Nachrichteneigenschaften wie gewünscht fest, und speichern und senden Sie dann die Nachricht, indem Sie **IMessage:: SubmitMessage**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="741b8-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="741b8-124">Weitere Informationen finden Sie unter [IMessage:: SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="741b8-125">Löschen Sie die gesendete Nachricht, wenn die **PR\_DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf true festgelegt ist, oder verschieben Sie Sie in den Ordner, der durch die **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="741b8-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="741b8-126">Weitere Informationen finden Sie unter [Verarbeiten einer gesendetEn Nachricht](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="741b8-127">Wenn Sie die Nachricht vor dem Senden erkennt speichern möchten, rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="741b8-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="741b8-128">Weitere Informationen finden Sie unter [Speichern einer Nachricht](saving-a-message.md) oder [Senden einer Nachricht](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="741b8-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="741b8-129">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="741b8-129">In this section</span></span>

- <span data-ttu-id="741b8-130">[Erstellen einer Empfängerliste](creating-a-recipient-list.md): Beschreibt das Erstellen einer Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="741b8-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="741b8-131">[Erstellen eines Nachrichtenbetreffs](creating-a-message-subject.md): Beschreibt, wie ein optionaler Betreff für eine Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="741b8-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="741b8-132">[Erstellen von Nachrichtentext](creating-message-text.md): Beschreibt, wie Nachrichtentext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="741b8-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="741b8-133">[Hinzufügen von Renderinformationen zu formatiertEm Text](adding-rendering-information-to-formatted-text.md): Beschreibt, wo in formatiertem Text eine Anlage gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="741b8-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="741b8-134">[Erstellen einer Nachrichtenanlage](creating-a-message-attachment.md): Beschreibt, wie Anlagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="741b8-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="741b8-135">[Speichern einer Nachricht](saving-a-message.md): Beschreibt, wie Clients Nachrichten speichern.</span><span class="sxs-lookup"><span data-stu-id="741b8-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="741b8-136">[Senden einer Nachricht](sending-a-message.md): Beschreibt, wie eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="741b8-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="741b8-137">[Verarbeiten einer gesendetEn Nachricht](processing-a-sent-message.md): Beschreibt, wie gesendete Nachrichten verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="741b8-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

