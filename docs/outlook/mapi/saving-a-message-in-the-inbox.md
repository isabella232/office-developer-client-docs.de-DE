---
title: Speichern einer Nachricht im Posteingang
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795414"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="adc8d-103">Speichern einer Nachricht im Posteingang</span><span class="sxs-lookup"><span data-stu-id="adc8d-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="adc8d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adc8d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="adc8d-105">**Eine Nachricht im Posteingang ohne Empfänger speichern**</span><span class="sxs-lookup"><span data-stu-id="adc8d-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="adc8d-106">Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um die Eintrags-ID des Posteingangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="adc8d-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="adc8d-107">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen des Posteingangs und einen Zeiger darauf abrufen.</span><span class="sxs-lookup"><span data-stu-id="adc8d-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="adc8d-108">Rufen Sie den Posteingang [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="adc8d-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="adc8d-109">Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_SUBJECT** ([ hinzuzufügen. PidTagSubject](pidtagsubject-canonical-property.md)) Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="adc8d-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="adc8d-110">Erstellen Sie jede Anlage, legen Sie dessen Eigenschaften, und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="adc8d-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="adc8d-111">Ausführliche Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="adc8d-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="adc8d-112">Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="adc8d-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="adc8d-113">Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Posteingangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adc8d-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="adc8d-114">Wenn eine Nachricht abwechselnd zu speichern, bevor er in der Inhaltstabelle des Posteingangs angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen, und klicken Sie dann in den Posteingang verschieben.</span><span class="sxs-lookup"><span data-stu-id="adc8d-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

