---
title: Behandeln des Adressbuchs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ef441b4315ef21f8b16dc062596bc7f1e526e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791820"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="ad6ae-103">Behandeln des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="ad6ae-103">Handling the address book</span></span>
  
<span data-ttu-id="ad6ae-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad6ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad6ae-105">Behandeln von MAPI-Adressbuch z�hlen Extrahieren von Eintr�gen f�r die Verwendung als Empf�nger der Nachricht, �ndern-Empf�ngereigenschaften, Hinzuf�gen von messaging-Benutzer oder Verteilerlisten, One erstellen und Anzeigen von mindestens eines der Standarddialogfelder Adresse, damit Benutzer Adressinformationen zu durchsuchen und �nderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="ad6ae-106">[Öffnen des Adressbuchs](opening-the-address-book.md): Beschreibt, wie Sie MAPI verwenden, um ein Adressbuch zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="ad6ae-107">[Das Dialogfeld allgemeine Adresse anzuzeigen](displaying-the-common-address-dialog-box.md): Beschreibt, wie andere Adresse Adressbuch Container angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="ad6ae-108">[Öffnen Sie ein Adressbuchcontainer](opening-an-address-book-container.md): Beschreibt, wie Sie andere Adresse Adressbuch Container zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="ad6ae-109">[Optionen für das Adressbuch Einstellung](setting-address-book-options.md): Beschreibt, wie Sie die Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="ad6ae-110">[Erstellen eines Empfängers](creating-a-recipient.md): Beschreibt, wie Sie Empfänger zu erstellen, wenn die Adressierung von Nachrichten und Hinzufügen von Einträgen zur änderbare Address Book Container.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="ad6ae-111">[Erstellen einer Verteilerliste](creating-a-distribution-list.md): Beschreibt, wie Sie erstellt eine Verteilerliste in einem Container geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="ad6ae-112">[Kopieren eines Empfängers](copying-a-recipient.md): Beschreibt, wie Sie Empfänger aus einem Container in ein anderes oder den gleichen Container kopieren.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="ad6ae-113">[Löschen eines Empfängers](deleting-a-recipient.md): Beschreibt, wie Sie einen oder mehrere Einträge im Adressbuch aus einem änderbare Container zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="ad6ae-114">[Vorbereiten eines Empfängers](preparing-a-recipient.md): Beschreibt, wie Sie vorbereitet Empfänger ihre kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner konvertieren und möglicherweise hinzufügen, ändern oder Neuanordnen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="ad6ae-115">[Zugreifen auf die Mitglieder von Verteilerlisten](accessing-the-members-of-a-distribution-list.md): Beschreibt, wie Sie die Mitglieder einer Verteilerliste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="ad6ae-116">[Abrufen von Eigenschaften für Recipient](retrieving-recipient-properties.md): Beschreibt, wie Sie eine oder mehrere Eigenschaften eines Eintrags Empfängeradresse Adressbuch zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="ad6ae-117">[Suchen im Adressbuch](searching-the-address-book.md): Beschreibt die zwei Stufen von MAPI-Suchfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="ad6ae-118">[Verwenden Sie ein Dialogfeld für erweiterte Suche](using-an-advanced-search-dialog-box.md): Beschreibt, wie Sie eine erweiterte Suche-Funktionalität in einer Adressbuchcontainer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="ad6ae-119">[Auflösen von Namen Empfänger](resolving-a-recipient-name.md): Beschreibt, wie Sie einen Namen in einem Adressbuch aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="ad6ae-120">[Verteilerlisten erweitern](expanding-distribution-lists.md): Beschreibt, wie Sie auffordern, MAPI, um eine Verteilerliste zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="ad6ae-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

