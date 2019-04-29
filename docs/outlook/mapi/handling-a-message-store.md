---
title: Behandeln eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407543"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="61756-103">Behandeln eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="61756-103">Handling a message store</span></span>
  
<span data-ttu-id="61756-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61756-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61756-105">Die Behandlung eines Nachrichtenspeichers ist ein wichtiger Teil des Aufgaben Satzes eines beliebigen Clients.</span><span class="sxs-lookup"><span data-stu-id="61756-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="61756-106">Zu diesen Aufgaben gehört das Öffnen, kopieren, bewegen, hinzufügen und Löschen von Ordnern und Nachrichten, das Anzeigen verschiedener Tabellen, das Festlegen von Eigenschaften und das Steuern von Zugriffsebenen.</span><span class="sxs-lookup"><span data-stu-id="61756-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="61756-107">[Öffnen eines Nachrichtenspeichers](opening-a-message-store.md): Beschreibt, wie ein oder mehrere Nachrichtenspeicher während einer Sitzung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="61756-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="61756-108">[Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md): Beschreibt das Öffnen des Standardnachrichten Speichers.</span><span class="sxs-lookup"><span data-stu-id="61756-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="61756-109">Über [prüfen und Initialisieren eines Nachrichtenspeichers](validating-and-initializing-a-message-store.md): Beschreibt, wie ein Nachrichtenspeicher initialisiert und überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="61756-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="61756-110">Durch [Suchen eines Nachrichtenspeichers](searching-a-message-store.md): Beschreibt, wie Sie in einem oder mehreren Ordnern nach Nachrichten suchen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="61756-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="61756-111">[Auswählen eines Empfangs Ordners](selecting-a-receive-folder.md): Beschreibt die Schritte zum Erstellen eines Empfangs Ordners.</span><span class="sxs-lookup"><span data-stu-id="61756-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="61756-112">[Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md): Beschreibt, wie ein Ordner geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61756-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="61756-113">[Anzeigen einer Ordnerinhaltstabelle](displaying-a-folder-contents-table.md): Beschreibt, wie die Tabelle mit den Ordnerinhalten angezeigt wird, die zusammenfassende Informationen zu allen Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="61756-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="61756-114">Durch [laufen des Posteingangsordners](traversing-the-inbox-folder.md): Beschreibt, wie Sie alle Nachrichten im Posteingang durchgehen.</span><span class="sxs-lookup"><span data-stu-id="61756-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="61756-115">[Kopieren oder Verschieben einer Nachricht oder eines Ordners](copying-or-moving-a-message-or-a-folder.md): Beschreibt, wie eine oder mehrere Nachrichten kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="61756-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="61756-116">[Öffnen einer Nachricht](opening-a-message.md): Beschreibt, wie eine Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61756-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="61756-117">[Suchen des Symbols für eine Nachricht](finding-the-icon-for-a-message.md): Beschreibt, wie Sie ein Symbol finden, das einer Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61756-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="61756-118">[Öffnen eines Ansichts Deskriptors](opening-a-view-descriptor.md): Beschreibt, wie ein Ansichts Deskriptor geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61756-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="61756-119">[Löschen einer Nachricht](deleting-a-message.md): Beschreibt das Löschen einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="61756-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="61756-120">[Speichern einer Nachricht im Posteingang](saving-a-message-in-the-inbox.md): Beschreibt, wie eine Nachricht im Posteingang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="61756-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="61756-121">[Suchen nach gesendeten oder gespeicherten Nachrichten](finding-sent-or-saved-messages.md): Beschreibt, wie alle ausgehenden Nachrichten gefunden werden, die gespeichert oder gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="61756-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="61756-122">[Nach](tracking-conversations.md)verfolgen von Unterhaltungen: Beschreibt, wie Konversationen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="61756-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

