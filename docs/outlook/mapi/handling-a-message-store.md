---
title: Behandeln eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f915a17b8271f7ec4173f507504bf165a6084085
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791811"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="93f63-103">Behandeln eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="93f63-103">Handling a message store</span></span>
  
<span data-ttu-id="93f63-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93f63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93f63-105">Behandeln eines Nachrichtenspeichers stellen einen wichtigen Bestandteil des Clients Reihe von Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="93f63-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="93f63-106">Diese Aufgaben umfassen das Öffnen, kopieren, verschieben, hinzufügen und Löschen von Ordnern und Nachrichten, Anzeigen von verschiedenen Tabellen, Festlegen von Eigenschaften und Zugriffsebenen steuern.</span><span class="sxs-lookup"><span data-stu-id="93f63-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="93f63-107">[Öffnen Sie einen Nachrichtenspeicher](opening-a-message-store.md): Beschreibt, wie Sie eine oder mehrere Nachrichtenspeicher während einer Sitzung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93f63-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="93f63-108">[Öffnen Sie den standardmäßigen Nachrichtenspeicher](opening-the-default-message-store.md): Beschreibt, wie Sie den Standard-Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93f63-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="93f63-109">[Validating und Initialisieren eines Nachrichtenspeichers](validating-and-initializing-a-message-store.md): Initialisieren und Überprüfen eines Nachrichtenspeichers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="93f63-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="93f63-110">[Suchen Sie einen Nachrichtenspeicher](searching-a-message-store.md): Beschreibt, wie Sie sehen Sie sich einen oder mehrere Ordner suchen Sie nach Nachrichten, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="93f63-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="93f63-111">[Auswählen eines Ordners empfangen](selecting-a-receive-folder.md): Beschreibt die Schritte zum Erstellen eines Ordners empfangen.</span><span class="sxs-lookup"><span data-stu-id="93f63-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="93f63-112">[Öffnen Sie einen Speicherordner Nachricht](opening-a-message-store-folder.md): Beschreibt, wie Sie einen Ordner zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93f63-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="93f63-113">[Eine Tabelle der Ordner-Inhalt angezeigt](displaying-a-folder-contents-table.md): Beschreibt, wie der Ordner Inhaltstabelle anzuzeigen, zusammenfassende Informationen zu allen der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="93f63-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="93f63-114">[Durchlaufen Sie den Ordner Posteingang](traversing-the-inbox-folder.md): Beschreibt, wie Sie alle Nachrichten im Posteingang zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="93f63-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="93f63-115">[Kopieren oder Verschieben einer Nachricht oder eines Ordners](copying-or-moving-a-message-or-a-folder.md): Beschreibt, wie Sie eine oder mehrere Nachrichten kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="93f63-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="93f63-116">[Öffnen einer Nachricht](opening-a-message.md): Beschreibt, wie Sie eine Nachricht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93f63-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="93f63-117">[Suchen Sie das Symbol für eine Nachricht](finding-the-icon-for-a-message.md): Beschreibt, wie Sie ein Symbol zu suchen, die eine Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93f63-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="93f63-118">[Öffnen Sie eine Ansicht Beschreibung](opening-a-view-descriptor.md): Beschreibt, wie Sie eine Beschreibung für die Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93f63-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="93f63-119">[Löschen einer Nachricht](deleting-a-message.md): Beschreibt, wie Sie eine Nachricht zu löschen.</span><span class="sxs-lookup"><span data-stu-id="93f63-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="93f63-120">[Speichern einer Nachricht im Posteingang](saving-a-message-in-the-inbox.md): Beschreibt, wie Sie eine Nachricht im Posteingang zu speichern.</span><span class="sxs-lookup"><span data-stu-id="93f63-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="93f63-121">[Suchen von gesendet oder gespeicherte Nachrichten](finding-sent-or-saved-messages.md): Beschreibt, wie Sie alle ausgehende Nachrichten suchen, die gespeichert oder gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="93f63-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="93f63-122">[Nachverfolgen der Unterhaltungen](tracking-conversations.md): Beschreibt, wie Unterhaltungen nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="93f63-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

