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
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407893"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="aaf67-103">Speichern einer Nachricht im Posteingang</span><span class="sxs-lookup"><span data-stu-id="aaf67-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="aaf67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aaf67-105">**So speichern Sie eine Nachricht im Posteingang ohne Empfänger**</span><span class="sxs-lookup"><span data-stu-id="aaf67-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="aaf67-106">Rufen Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner des Posteingangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aaf67-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="aaf67-107">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um den Posteingang zu öffnen und einen Zeiger darauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aaf67-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="aaf67-108">Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode des Posteingangs auf, um die Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aaf67-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="aaf67-109">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Nachricht auf, um die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)), **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_Subject** ([ PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aaf67-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="aaf67-110">Erstellen Sie jede Anlage, legen Sie Ihre Eigenschaften fest, und speichern Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="aaf67-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="aaf67-111">Ausführliche Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="aaf67-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="aaf67-112">Rufen Sie **IMessage:: SaveChanges** auf, um die Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="aaf67-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="aaf67-113">An dieser Stelle wird es in der Inhaltstabelle des Posteingangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aaf67-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="aaf67-114">Wenn Sie eine Nachrichten erkennt speichern möchten, bevor Sie in der Tabelle Inhalt des Posteingangs angezeigt wird, erstellen Sie Sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie Sie dann in den Posteingang.</span><span class="sxs-lookup"><span data-stu-id="aaf67-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  

