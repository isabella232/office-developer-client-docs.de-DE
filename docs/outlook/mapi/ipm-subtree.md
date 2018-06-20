---
title: IPM-Unterstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792740"
---
# <a name="ipm-subtree"></a><span data-ttu-id="94e9f-103">IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="94e9f-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="94e9f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94e9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94e9f-105">MAPI erstellt eine Struktur von Ordnern unter den Stammordner eines Nachrichtenspeichers für alle Clients, die Nachrichten senden und Empfangen von Nachrichten von Menschen, statt die Computer, die Empfänger.</span><span class="sxs-lookup"><span data-stu-id="94e9f-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="94e9f-106">Nachrichten zwischen Empfängern human ausgetauscht werden, werden als Nachrichten zwischen Personen, und diese Struktur ist bezeichnet als zwischen Personen Nachricht oder IPM, subtree.</span><span class="sxs-lookup"><span data-stu-id="94e9f-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="94e9f-107">Eine IPM-Unterstruktur für einen übermittlungsspeicher besteht aus mindestens die folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="94e9f-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="94e9f-108">Posteingang</span><span class="sxs-lookup"><span data-stu-id="94e9f-108">Inbox</span></span>
    
- <span data-ttu-id="94e9f-109">Postausgang</span><span class="sxs-lookup"><span data-stu-id="94e9f-109">Outbox</span></span>
    
- <span data-ttu-id="94e9f-110">Gesendete Elemente</span><span class="sxs-lookup"><span data-stu-id="94e9f-110">Sent Items</span></span>
    
- <span data-ttu-id="94e9f-111">Gelöschte Elemente</span><span class="sxs-lookup"><span data-stu-id="94e9f-111">Deleted Items</span></span>
    
<span data-ttu-id="94e9f-112">Dies sind die Standardnamen und die Rollen für jedes dieser Ordner. ein Client kann einen eigenen Namen angeben, wenn die Standardnamen nicht geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="94e9f-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="94e9f-113">MAPI weist den Standardnamen und Zuordnungen für diese Ordner zu verhindern, dass Nachrichten versehentlich ausgeblendet wird, wenn ein Client bildschirmaktualisierung Empfang von Ordnern für Nachrichten herstellen.</span><span class="sxs-lookup"><span data-stu-id="94e9f-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="94e9f-114">In einem Microsoft Office Outlook-Kontext besteht aus eine IPM-Unterstruktur zusätzliche Standardordner für Kalender, Kontakte, Aufgaben, Notizen und Journal.</span><span class="sxs-lookup"><span data-stu-id="94e9f-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="94e9f-115">Posteingang enthält normalerweise eingehende Nachrichten, und im Ordner Postausgang enthält ausgehende Nachrichten (d. h., Nachrichten gesendet werden).</span><span class="sxs-lookup"><span data-stu-id="94e9f-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="94e9f-116">Ordner Gesendete Objekte enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die Eintrags-ID dieses Ordners die **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))-Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="94e9f-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="94e9f-117">Ordner Gelöschte Elemente enthält Nachrichten, die zur Löschung markiert.</span><span class="sxs-lookup"><span data-stu-id="94e9f-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94e9f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94e9f-118">See also</span></span>



[<span data-ttu-id="94e9f-119">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="94e9f-119">MAPI Folders</span></span>](mapi-folders.md)

