---
title: Empfangen von Nachrichten mithilfe von Store Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418729"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="f9563-103">Empfangen von Nachrichten mithilfe von Store Anbietern</span><span class="sxs-lookup"><span data-stu-id="f9563-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="f9563-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9563-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9563-105">Nachrichtenspeicheranbieter müssen eingehende Nachrichtenübermittlungen nicht unterstützen (d. h. sie unterstützen die Möglichkeit für Transportanbieter und den MAPI-Spooler, den Nachrichtenspeicheranbieter als Zustellungspunkt für Nachrichten zu verwenden).</span><span class="sxs-lookup"><span data-stu-id="f9563-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="f9563-106">Wenn ihr Nachrichtenspeicheranbieter eingehende Nachrichtenübermittlungen jedoch nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9563-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="f9563-107">Um eingehende Nachrichtenübermittlungen zu unterstützen, muss Ihr Nachrichtenspeicheranbieter die folgenden Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="f9563-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="f9563-108">Unterstützen Sie [die Methoden IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) damit Clientanwendungen eingehende Nachrichten finden können.</span><span class="sxs-lookup"><span data-stu-id="f9563-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="f9563-109">Unterstützen Sie [die IMsgStore::NotifyNewMail-Methode,](imsgstore-notifynewmail.md) damit der MAPI-Spooler den Nachrichtenspeicheranbieter darüber informieren kann, dass eine neue Nachricht eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="f9563-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="f9563-110">Implementieren Sie Benachrichtigungen, damit Clients sich für neue Nachrichtenbenachrichtigungen registrieren können.</span><span class="sxs-lookup"><span data-stu-id="f9563-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="f9563-111">Benachrichtigungen sind optional, aber Ihr Anbieter sollte sie implementieren.</span><span class="sxs-lookup"><span data-stu-id="f9563-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="f9563-112">Die Reihenfolge der Methodenaufrufe, die auftreten, wenn eine eingehende Nachricht an einen Nachrichtenspeicher zugestellt wird, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f9563-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="f9563-113">Der MAPI-Spooler ruft [IMsgStore::OpenEntry](imsgstore-openentry.md) mit der Posteingangseintrags-ID auf, um eine [IMAPIFolder-Schnittstelle zu](imapifolderimapicontainer.md) erhalten. [](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="f9563-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="f9563-114">Der MAPI-Spooler ruft [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf, um ein neues Nachrichtenobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f9563-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="f9563-115">Der MAPI-Spooler übergibt das Message-Objekt an den Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="f9563-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="f9563-116">Der Transportanbieter füllt die Eigenschaften der Nachricht mit Daten aus dem zugrunde liegenden Messagingsystem ein und ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Nachrichtenobjekts auf.</span><span class="sxs-lookup"><span data-stu-id="f9563-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="f9563-117">Der Nachrichtenspeicheranbieter verwendet seine Benachrichtigungsmethode, um registrierte Clients darüber zu informieren, dass eine neue Nachricht eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="f9563-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="f9563-118">Der MAPI-Spooler ruft die [IMsgStore::NotifyNewMail-Methode des Nachrichtenspeichers](imsgstore-notifynewmail.md) auf.</span><span class="sxs-lookup"><span data-stu-id="f9563-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f9563-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9563-119">See also</span></span>



[<span data-ttu-id="f9563-120">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="f9563-120">Message Store Features</span></span>](message-store-features.md)

