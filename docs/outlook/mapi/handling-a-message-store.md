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
# <a name="handling-a-message-store"></a><span data-ttu-id="724a5-103">Behandeln eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="724a5-103">Handling a message store</span></span>
  
<span data-ttu-id="724a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="724a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="724a5-105">Die Verarbeitung eines Nachrichtenspeichers ist ein wichtiger Bestandteil der Aufgaben eines clients.</span><span class="sxs-lookup"><span data-stu-id="724a5-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="724a5-106">Zu diesen Aufgaben gehören das Öffnen, Kopieren, Verschieben, Hinzufügen und Löschen von Ordnern und Nachrichten, das Anzeigen verschiedener Tabellen, das Festlegen von Eigenschaften und das Steuern von Zugriffsebenen.</span><span class="sxs-lookup"><span data-stu-id="724a5-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="724a5-107">[Öffnen eines Nachrichtenspeichers:](opening-a-message-store.md)Beschreibt, wie Sie einen oder mehrere Nachrichtenspeicher während einer Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="724a5-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="724a5-108">[Öffnen des Standardnachrichtenspeichers](opening-the-default-message-store.md): Beschreibt das Öffnen des Standardnachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="724a5-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="724a5-109">[Überprüfen und Initialisieren eines Nachrichtenspeichers:](validating-and-initializing-a-message-store.md)Beschreibt, wie ein Nachrichtenspeicher initialisiert und überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="724a5-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="724a5-110">[Durchsuchen eines Nachrichtenspeichers:](searching-a-message-store.md)Beschreibt, wie Sie einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="724a5-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="724a5-111">[Auswählen eines Empfangsordners](selecting-a-receive-folder.md): Beschreibt die Schritte zum Erstellen eines Empfangsordners.</span><span class="sxs-lookup"><span data-stu-id="724a5-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="724a5-112">[Öffnen eines Nachrichtenspeicherordners:](opening-a-message-store-folder.md)Beschreibt das Öffnen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="724a5-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="724a5-113">[Anzeigen eines Ordnerinhaltsverzeichnisses:](displaying-a-folder-contents-table.md)Beschreibt, wie die Ordnerinhaltstabelle angezeigt wird, die Zusammenfassungsinformationen zu allen nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="724a5-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="724a5-114">[Durchlaufen des Posteingangsordners](traversing-the-inbox-folder.md): Beschreibt, wie alle Nachrichten im Posteingang durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="724a5-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="724a5-115">[Kopieren oder Verschieben einer Nachricht oder eines Ordners](copying-or-moving-a-message-or-a-folder.md): Beschreibt, wie Sie eine oder mehrere Nachrichten kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="724a5-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="724a5-116">[Öffnen einer Nachricht](opening-a-message.md): Beschreibt, wie eine Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="724a5-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="724a5-117">[Suchen des Symbols für eine Nachricht](finding-the-icon-for-a-message.md): Beschreibt, wie Sie ein Symbol finden, das einer Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="724a5-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="724a5-118">[Öffnen eines Ansichtsdeskriptors](opening-a-view-descriptor.md): Beschreibt das Öffnen eines Ansichtsdeskriptors.</span><span class="sxs-lookup"><span data-stu-id="724a5-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="724a5-119">[Löschen einer Nachricht](deleting-a-message.md): Beschreibt, wie eine Nachricht gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="724a5-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="724a5-120">[Speichern einer Nachricht im Posteingang](saving-a-message-in-the-inbox.md): Beschreibt, wie eine Nachricht im Posteingang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="724a5-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="724a5-121">[Suchen nach gesendeten oder gespeicherten Nachrichten](finding-sent-or-saved-messages.md): Beschreibt, wie Alle ausgehenden Nachrichten gefunden werden, die gespeichert oder gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="724a5-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="724a5-122">[Nachverfolgen von Unterhaltungen](tracking-conversations.md): Beschreibt, wie Unterhaltungen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="724a5-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

