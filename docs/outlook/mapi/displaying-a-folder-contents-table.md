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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339935"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="05618-103">Anzeigen einer Ordnerinhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="05618-103">Displaying a folder contents table</span></span>

<span data-ttu-id="05618-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05618-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05618-105">Die Inhaltstabelle eines Ordners enthält zusammenfassende Informationen zu allen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="05618-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="05618-106">Zusammenfassende Informationen zu neuen eingehenden Nachrichten werden in der Tabelle Inhalt des Empfänger Ordners für die Nachrichtenklasse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="05618-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="05618-107">Um diese Informationen Benutzern zur Verfügung zu stellen, rufen Sie die Tabelle ab, und zeigen Sie die Spalten und Zeilen entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="05618-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="05618-108">**So zeigen Sie eine Ordnerinhaltstabelle an**</span><span class="sxs-lookup"><span data-stu-id="05618-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="05618-109">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Ordners, der die Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="05618-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="05618-110">Rufen Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Ordners auf, um die Inhaltstabelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05618-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="05618-111">Schränken Sie die Ansicht der Inhaltstabelle auf Wunsch ein, indem Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Tabelle aufrufen, um bestimmte Spalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05618-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="05618-112">Begrenzen Sie die Ansicht der Inhaltstabelle auf Wunsch, indem Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode der Tabelle zum Filtern bestimmter Zeilen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05618-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="05618-113">Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen möchten, die noch nicht gelesen werden müssen:</span><span class="sxs-lookup"><span data-stu-id="05618-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="05618-114">Erstellen Sie eine Eigenschaftseinschränkung in einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, die mit der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft mit der gewünschten Nachrichtenklasse übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05618-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="05618-115">Erstellen Sie eine Bitmasken Einschränkung in einer [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur, die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als Property-Tag und den MSGFLAG_UNREAD-Wert als Maske verwendet.</span><span class="sxs-lookup"><span data-stu-id="05618-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="05618-116">Erstellen Sie eine Einschränkung in einer [SAndRestriction](sandrestriction.md) -Struktur, die die Eigenschaften-und Bitmasken Einschränkungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="05618-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="05618-117">Sortieren Sie die Inhaltstabelle nach Bedarf, indem Sie die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode der Tabelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05618-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="05618-118">Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um alle Zeilen aus der Tabelle Contents zur Verarbeitung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="05618-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

