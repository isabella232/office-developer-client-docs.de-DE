---
title: Behandeln des Adressbuchs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b685244a-fe1b-4416-85d3-4bd86ccbc3aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 464549732562a4a02d081dc5a4c5e573e38cbbce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299419"
---
# <a name="handling-the-address-book"></a><span data-ttu-id="de64a-103">Behandeln des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="de64a-103">Handling the address book</span></span>
  
<span data-ttu-id="de64a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de64a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de64a-105">Behandeln von MAPI-Adressbuch z�hlen Extrahieren von Eintr�gen f�r die Verwendung als Empf�nger der Nachricht, �ndern-Empf�ngereigenschaften, Hinzuf�gen von messaging-Benutzer oder Verteilerlisten, One erstellen und Anzeigen von mindestens eines der Standarddialogfelder Adresse, damit Benutzer Adressinformationen zu durchsuchen und �nderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="de64a-105">Handling the MAPI address book can include extracting entries to be used as message recipients, modifying recipient properties, adding messaging users or distribution lists, creating one-offs, and displaying one or more of the common address dialog boxes to allow users to browse address information and make changes.</span></span>

- <span data-ttu-id="de64a-106">[Öffnen des Adressbuchs](opening-the-address-book.md): Beschreibt, wie MAPI zum Öffnen eines Adressbuchs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de64a-106">[Opening the Address Book](opening-the-address-book.md): Describes how to use MAPI to open an address book.</span></span>
    
- <span data-ttu-id="de64a-107">[Anzeigen des Dialog Felds "allgemeine Adresse](displaying-the-common-address-dialog-box.md)": Beschreibt, wie unterschiedliche Adressbuchcontainer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="de64a-107">[Displaying the Common Address Dialog Box](displaying-the-common-address-dialog-box.md): Describes how to display different address book containers.</span></span>
    
- <span data-ttu-id="de64a-108">[Öffnen eines Adressbuch Containers](opening-an-address-book-container.md): Beschreibt, wie Sie verschiedene Adressbuchcontainer öffnen.</span><span class="sxs-lookup"><span data-stu-id="de64a-108">[Opening an Address Book Container](opening-an-address-book-container.md): Describes how to open different address book containers.</span></span>
    
- <span data-ttu-id="de64a-109">[Festlegen von Adressbuchoptionen](setting-address-book-options.md): Beschreibt, wie die Eigenschaften festgelegt werden, die Optionen für die Verwendung des Adressbuchs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="de64a-109">[Setting Address Book Options](setting-address-book-options.md): Describes how to set the properties that describe options for using the address book.</span></span>
    
- <span data-ttu-id="de64a-110">[Erstellen eines Empfängers](creating-a-recipient.md): Beschreibt, wie Empfänger beim Adressieren von Nachrichten und Hinzufügen von Einträgen zu änderbaren Adressbuch Containern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="de64a-110">[Creating a Recipient](creating-a-recipient.md): Describes how to create recipients when addressing messages and adding entries to modifiable address book containers.</span></span>
    
- <span data-ttu-id="de64a-111">[Erstellen einer Verteilerliste](creating-a-distribution-list.md): Beschreibt das Erstellen einer Verteilerliste in einem änderbaren Container.</span><span class="sxs-lookup"><span data-stu-id="de64a-111">[Creating a Distribution List](creating-a-distribution-list.md): Describes how to create a distribution list into a modifiable container.</span></span>
    
- <span data-ttu-id="de64a-112">[Kopieren eines Empfängers](copying-a-recipient.md): Beschreibt, wie Empfänger aus einem Container in einen anderen oder denselben Container kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="de64a-112">[Copying a Recipient](copying-a-recipient.md): Describes how to copy recipients from one container into another or the same container.</span></span>
    
- <span data-ttu-id="de64a-113">[Löschen eines Empfängers](deleting-a-recipient.md): Beschreibt das Entfernen eines oder mehrerer Adressbucheinträge aus einem änderbaren Container.</span><span class="sxs-lookup"><span data-stu-id="de64a-113">[Deleting a Recipient](deleting-a-recipient.md): Describes how to remove one or more address book entries from a modifiable container.</span></span>
    
- <span data-ttu-id="de64a-114">[Vorbereiten eines Empfängers](preparing-a-recipient.md): Beschreibt, wie Sie Empfänger vorbereiten, indem Sie deren kurzfristige Eintragsbezeichner in langfristige Eintragsbezeichner konvertieren und möglicherweise Eigenschaften hinzufügen, ändern oder neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="de64a-114">[Preparing a Recipient](preparing-a-recipient.md): Describes how to prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span>
    
- <span data-ttu-id="de64a-115">[Zugreifen auf die Mitglieder einer Verteilerliste](accessing-the-members-of-a-distribution-list.md): Beschreibt den Zugriff auf die Mitglieder einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="de64a-115">[Accessing the Members of a Distribution List](accessing-the-members-of-a-distribution-list.md): Describes how to access the members of a distribution list.</span></span>
    
- <span data-ttu-id="de64a-116">[Abrufen von Empfänger Eigenschaften](retrieving-recipient-properties.md): Beschreibt den Zugriff auf eine oder mehrere Eigenschaften eines Empfänger Adressbuch-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="de64a-116">[Retrieving Recipient Properties](retrieving-recipient-properties.md): Describes how to access one or more properties of a recipient address book entry.</span></span>
    
- <span data-ttu-id="de64a-117">Durch [Suchen des Adressbuchs](searching-the-address-book.md): Beschreibung der beiden Ebenen der MAPI-Suchfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="de64a-117">[Searching the Address Book](searching-the-address-book.md): Describes the two levels of MAPI search functionality.</span></span> 
    
- <span data-ttu-id="de64a-118">[Verwenden eines Dialog Felds für die erweiterte Suche](using-an-advanced-search-dialog-box.md): Beschreibt, wie Sie eine erweiterte Suchfunktionalität in einem Adressbuchcontainer ausführen.</span><span class="sxs-lookup"><span data-stu-id="de64a-118">[Using an Advanced Search Dialog Box](using-an-advanced-search-dialog-box.md): Describes how to run an advanced search functionality in an address book container.</span></span>
    
- <span data-ttu-id="de64a-119">[Auflösen eines Empfängernamens](resolving-a-recipient-name.md): Beschreibt, wie ein Name in einem Adressbuch aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="de64a-119">[Resolving a Recipient Name](resolving-a-recipient-name.md): Describes how to resolve a name in an address book.</span></span>
    
- <span data-ttu-id="de64a-120">[Erweitern von Verteilerlisten](expanding-distribution-lists.md): Beschreibt, wie MAPI zum Erweitern einer Verteilerliste aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="de64a-120">[Expanding Distribution Lists](expanding-distribution-lists.md): Describes how to prompt MAPI to expand a distribution list.</span></span>
    

