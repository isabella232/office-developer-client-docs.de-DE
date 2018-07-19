---
title: Empfangen von Nachrichten durch Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 94ea0fe7fba4e49c1f646d889f3727cf5ef4739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795346"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="d66f5-103">Empfangen von Nachrichten durch Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="d66f5-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="d66f5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d66f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d66f5-105">Nachricht-Anbieter müssen keine eingehenden Nachrichtenübermittlungen unterstützen (d. h., unterstützen die Möglichkeit zu Nachrichten Transportanbieter und die Warteschlange MAPI-Anbieter als Ausgangspunkt Übermittlung von Nachrichten Filiale).</span><span class="sxs-lookup"><span data-stu-id="d66f5-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="d66f5-106">Jedoch, wenn Ihre Nachricht Speicheranbieter eingehende Nachrichtenübermittlungen nicht unterstützt, kann es als Standard-Informationsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d66f5-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="d66f5-107">Zur Unterstützung der eingehenden Nachrichtenübermittlungen muss ein Speicheranbieter Nachricht Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="d66f5-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="d66f5-108">Unterstützt die Methoden [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) -Clientanwendungen eingehende Nachrichten suchen können.</span><span class="sxs-lookup"><span data-stu-id="d66f5-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="d66f5-109">Unterstützung für die [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode, damit die MAPI-Warteschlange den Nachricht Speicheranbieter informieren kann, den eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="d66f5-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="d66f5-110">Implementieren Sie Benachrichtigungen, damit Clients für die Benachrichtigung über eine neue Nachricht registrieren können.</span><span class="sxs-lookup"><span data-stu-id="d66f5-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="d66f5-111">Benachrichtigungen sind optional, jedoch zu Ihrem Anbieter sollte implementieren.</span><span class="sxs-lookup"><span data-stu-id="d66f5-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="d66f5-112">Die Reihenfolge der Methodenaufrufe, die auftritt, wenn eine eingehende Nachricht an einen Nachrichtenspeicher übermittelt werden lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d66f5-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="d66f5-113">Die MAPI-Warteschlange ruft [IMsgStore::OpenEntry](imsgstore-openentry.md) mit der Posteingang [EntryID](entryid.md) eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="d66f5-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="d66f5-114">Die MAPI-Warteschlange ruft [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) zum Abrufen einer neuen Nachricht-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d66f5-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="d66f5-115">Die MAPI-Warteschlange übergibt das Message-Objekt an der Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="d66f5-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="d66f5-116">Der Transportdienst füllt Nachrichteneigenschaften mit Daten aus dem zugrunde liegenden messaging-System und das Meldungsobjekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d66f5-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="d66f5-117">Der Nachricht Speicheranbieter verwendet seine Benachrichtigungsmethode registrierte Clients informiert, die eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="d66f5-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="d66f5-118">Der Nachrichtenspeicher [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode aufgerufen, die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d66f5-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d66f5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d66f5-119">See also</span></span>



[<span data-ttu-id="d66f5-120">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="d66f5-120">Message Store Features</span></span>](message-store-features.md)

