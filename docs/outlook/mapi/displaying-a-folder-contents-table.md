---
title: Anzeigen einer Tabelle der Ordner-Inhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580796"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="0d4d3-103">Anzeigen einer Tabelle der Ordner-Inhalt</span><span class="sxs-lookup"><span data-stu-id="0d4d3-103">Displaying a folder contents table</span></span>

<span data-ttu-id="0d4d3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d4d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d4d3-105">Inhaltstabelle eines Ordners enthält zusammenfassende Informationen zu allen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="0d4d3-106">Zusammenfassende Informationen zu neuen eingehenden Nachrichten in der Inhaltstabelle des Ordners "empfangen" für die Nachrichtenklasse wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="0d4d3-107">Um diese Informationen für Benutzer verfügbar machen, Abrufen der Tabelle und die Spalten und Zeilen nach Bedarf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="0d4d3-108">**Zum Anzeigen einer Tabelle der Ordner-Inhalt**</span><span class="sxs-lookup"><span data-stu-id="0d4d3-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="0d4d3-109">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md), die Eintrags-ID des Ordners mit der Tabelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="0d4d3-110">Rufen Sie den Ordner [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode, um seine Inhaltstabelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="0d4d3-111">Beschränken Sie Ihre Ansicht der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode bestimmte Spalten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="0d4d3-112">Beschränken Sie Ihre Ansicht der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, um bestimmte Zeilen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="0d4d3-113">Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen, die noch nicht gelesen werden möchten:</span><span class="sxs-lookup"><span data-stu-id="0d4d3-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="0d4d3-114">Erstellen Sie eine eigenschaftseinschränkung in eine [SPropertyRestriction](spropertyrestriction.md) -Struktur, die die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) mit der gewünschten Nachrichtenklasse entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="0d4d3-115">Erstellen Sie eine Bitmaske Beschränkung in eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur, die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als das Eigenschafts-Tag und den Wert MSGFLAG_UNREAD als Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="0d4d3-116">Erstellen Sie eine Einschränkung in eine [SAndRestriction](sandrestriction.md) -Struktur, die die Einschränkungen-Eigenschaft und Bitmaske teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="0d4d3-117">Sortieren der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [SortTable](imapitable-sorttable.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="0d4d3-118">Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) , um alle Zeilen aus der Inhaltstabelle für die Verarbeitung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d4d3-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

