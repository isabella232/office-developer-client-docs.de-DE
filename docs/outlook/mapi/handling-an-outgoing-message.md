---
title: Behandeln von ausgehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791794"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="bce88-103">Behandeln von ausgehenden Nachrichten</span><span class="sxs-lookup"><span data-stu-id="bce88-103">Handling an outgoing message</span></span>

<span data-ttu-id="bce88-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bce88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bce88-105">Eine ausgehende Nachricht ist eine Nachricht, die an einen oder mehrere Empfänger gesendet werden kann, über eine oder mehrere messaging-Systemen oder in einen Ordner in einem Nachrichtenspeicher veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="bce88-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="bce88-106">Erstellen Sie und senden Sie eine ausgehende Nachricht</span><span class="sxs-lookup"><span data-stu-id="bce88-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="bce88-107">Öffnen Sie die Standard-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bce88-107">Open the default message store.</span></span> <span data-ttu-id="bce88-108">Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md) und [Öffnen Sie die Standard-Informationsspeicher](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="bce88-109">Öffnen Sie den Ordner Postausgang.</span><span class="sxs-lookup"><span data-stu-id="bce88-109">Open the Outbox folder.</span></span> <span data-ttu-id="bce88-110">Weitere Informationen finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="bce88-111">Aufrufen der Ordner Postausgang **IMAPIFolder::CreateMessage** -Methode, um die neue Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bce88-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="bce88-112">Weitere Informationen finden Sie unter [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="bce88-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="bce88-113">Erstellen Sie eine Empfängerliste mit einen oder mehrere aufgelösten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="bce88-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="bce88-114">Weitere Informationen finden Sie unter [Erstellen einer Liste der Empfänger](creating-a-recipient-list.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="bce88-115">Fügen Sie optional einen Betreff hinzu.</span><span class="sxs-lookup"><span data-stu-id="bce88-115">Optionally, add a subject.</span></span> <span data-ttu-id="bce88-116">Weitere Informationen finden Sie unter [Erstellen einer Betreff der Nachricht](creating-a-message-subject.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="bce88-117">Fügen Sie den Nachrichtentext hinzu.</span><span class="sxs-lookup"><span data-stu-id="bce88-117">Add the message text.</span></span> <span data-ttu-id="bce88-118">Weitere Informationen finden Sie unter [Erstellen des Nachrichtentexts](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="bce88-119">Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="bce88-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="bce88-120">Weitere Informationen finden Sie unter [Hinzufügen von Rendern von Informationen in Text formatiert](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="bce88-121">Fügen Sie optional eine oder mehrere Anlagen hinzu.</span><span class="sxs-lookup"><span data-stu-id="bce88-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="bce88-122">Weitere Informationen finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="bce88-123">Legen Sie nach Bedarf weitere Nachrichteneigenschaften und speichern und Senden der Nachricht durch Aufrufen von **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="bce88-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="bce88-124">Weitere Informationen finden Sie unter [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="bce88-125">Die gesendete Nachricht löschen, wenn die **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf TRUE oder verschieben in den Ordner identifiziert durch die **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bce88-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="bce88-126">Weitere Informationen finden Sie in der [Verarbeitung einer Nachricht gesendet](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="bce88-127">Wenn Sie möchten abwechselnd speichern Sie die Nachricht vor dem senden, rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bce88-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="bce88-128">Weitere Informationen finden Sie unter, [Speichern einer Nachricht](saving-a-message.md) oder [Senden einer Nachricht](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="bce88-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bce88-129">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="bce88-129">In this section</span></span>

- <span data-ttu-id="bce88-130">[Erstellen einer Liste der Empfänger](creating-a-recipient-list.md): Beschreibt das Erstellen einer Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="bce88-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="bce88-131">[Erstellen Sie einen Betreff der Nachricht](creating-a-message-subject.md): Beschreibt, wie Sie einen optionalen Betreff für eine Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bce88-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="bce88-132">[Erstellen des Nachrichtentexts](creating-message-text.md): Erstellen des Nachrichtentexts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bce88-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="bce88-133">[Rendern von Informationen zu formatierten Text hinzufügen](adding-rendering-information-to-formatted-text.md): Beschreibt, in dem in formatierten Text eine Anlage gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="bce88-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="bce88-134">[Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md): Beschreibt, wie Anlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="bce88-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="bce88-135">[Speichern einer Nachricht](saving-a-message.md): Beschreibt, wie Clients Nachrichten speichern.</span><span class="sxs-lookup"><span data-stu-id="bce88-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="bce88-136">[Senden einer Nachricht](sending-a-message.md): Beschreibt, wie Sie eine Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="bce88-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="bce88-137">[Verarbeiten einer Nachricht gesendet](processing-a-sent-message.md): Beschreibt, wie Sie gesendete Nachrichten verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="bce88-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

