---
title: IPM-unterStruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317108"
---
# <a name="ipm-subtree"></a><span data-ttu-id="e5f3b-103">IPM-unterStruktur</span><span class="sxs-lookup"><span data-stu-id="e5f3b-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="e5f3b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5f3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5f3b-105">MAPI erstellt eine Baumstruktur von Ordnern unterhalb des Stammordners eines Nachrichtenspeichers für alle Clients, die Nachrichten an den Menschen senden und von diesen empfangen, statt aus dem Computer, Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="e5f3b-106">Nachrichten, die zwischenmenschlichen Empfängern ausgetauscht werden, werden als zwischenmenschliche Nachrichten bezeichnet, und diese Struktur wird als zwischen Person (IPM, subtree) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="e5f3b-107">Eine IPM-Unterstruktur für einen zustellspeicher besteht aus mindestens den folgenden Ordnern:</span><span class="sxs-lookup"><span data-stu-id="e5f3b-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="e5f3b-108">Posteingang</span><span class="sxs-lookup"><span data-stu-id="e5f3b-108">Inbox</span></span>
    
- <span data-ttu-id="e5f3b-109">Postausgang</span><span class="sxs-lookup"><span data-stu-id="e5f3b-109">Outbox</span></span>
    
- <span data-ttu-id="e5f3b-110">Gesendete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5f3b-110">Sent Items</span></span>
    
- <span data-ttu-id="e5f3b-111">Gelöschte Elemente</span><span class="sxs-lookup"><span data-stu-id="e5f3b-111">Deleted Items</span></span>
    
<span data-ttu-id="e5f3b-112">Hierbei handelt es sich um die Standardnamen und-Rollen für jeden dieser Ordner; ein Client kann eigene Namen angeben, wenn die Standardnamen nicht geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="e5f3b-113">MAPI weist Standardnamen und Zuordnungen für diese Ordner zu, um zu verhindern, dass Nachrichten versehentlich ausgeblendet werden, wenn ein Client die Einrichtung von empfangenden Ordnern für Nachrichten vernachlässigt.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="e5f3b-114">In einem Microsoft Office Outlook-Kontext besteht eine IPM-Unterstruktur aus zusätzlichen Standardordnern für Kalender, Kontakte, Aufgaben, Notizen und Journal.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="e5f3b-115">Der Posteingang enthält in der Regel eingehende Nachrichten, und der postAusgang enthält ausgehende Nachrichten (also Nachrichten, die darauf warten, gesendet zu werden).</span><span class="sxs-lookup"><span data-stu-id="e5f3b-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="e5f3b-116">Der Ordner "Gesendete Elemente" enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft auf die Eintrags-ID dieses Ordners festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="e5f3b-117">Der Ordner Gelöschte Elemente enthält Nachrichten, die zum Entfernen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5f3b-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5f3b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5f3b-118">See also</span></span>



[<span data-ttu-id="e5f3b-119">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="e5f3b-119">MAPI Folders</span></span>](mapi-folders.md)

