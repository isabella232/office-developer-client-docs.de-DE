---
title: Anzeigen einer Ordnerinhaltstabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412394"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="6747c-103">Anzeigen einer Ordnerinhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="6747c-103">Displaying a folder contents table</span></span>

<span data-ttu-id="6747c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6747c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6747c-105">Das Inhaltsverzeichnis eines Ordners enthält Zusammenfassende Informationen zu allen nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6747c-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="6747c-106">Zusammenfassungsinformationen zu neuen eingehenden Nachrichten werden im Inhaltsverzeichnis des Empfangsordners für die Nachrichtenklasse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6747c-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="6747c-107">Um diese Informationen benutzern zur Verfügung zu stellen, rufen Sie die Tabelle ab, und zeigen Sie die Spalten und Zeilen entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="6747c-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="6747c-108">**So zeigen Sie eine Ordnerinhaltstabelle an**</span><span class="sxs-lookup"><span data-stu-id="6747c-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="6747c-109">Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Ordners, der die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="6747c-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="6747c-110">Rufen Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners auf, um die Inhaltstabelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6747c-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="6747c-111">Beschränken Sie die Ansicht der Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Tabelle aufrufen, um bestimmte Spalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6747c-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="6747c-112">Beschränken Sie die Ansicht der Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) der Tabelle aufrufen, um bestimmte Zeilen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="6747c-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="6747c-113">Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen möchten, die noch gelesen werden müssen:</span><span class="sxs-lookup"><span data-stu-id="6747c-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="6747c-114">Erstellen Sie eine Eigenschaftseinschränkung in einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) die der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft mit der gewünschten Nachrichtenklasse entspricht.</span><span class="sxs-lookup"><span data-stu-id="6747c-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="6747c-115">Erstellen Sie eine Bitmaskeneinschränkung in einer [SBitMaskRestriction-Struktur,](sbitmaskrestriction.md) die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als Eigenschaftstag und den MSGFLAG_UNREAD-Wert als Maske verwendet.</span><span class="sxs-lookup"><span data-stu-id="6747c-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="6747c-116">Erstellen Sie eine Einschränkung in einer [SAndRestriction-Struktur,](sandrestriction.md) die der Eigenschaft und den Bitmaskeneinschränkungen beitritt.</span><span class="sxs-lookup"><span data-stu-id="6747c-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="6747c-117">Sortieren Sie die Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::SortTable-Methode der Tabelle](imapitable-sorttable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6747c-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="6747c-118">Rufen [Sie IMAPITable::QueryRows auf,](imapitable-queryrows.md) um alle Zeilen aus der Inhaltstabelle zur Verarbeitung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6747c-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

