---
title: Suchen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571836"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="e9595-103">Suchen eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="e9595-103">Searching a message store</span></span>

<span data-ttu-id="e9595-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9595-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9595-105">Clientanwendungen können Suchen über einen oder mehrere Ordner suchen Sie nach Nachrichten, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e9595-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="e9595-106">Die einfachste Suchverfahren umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und platzieren die Ergebnisse in einem Ordner-Ergebnisse für diese Suche oder bei einer vorherigen Suche explizit erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9595-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="e9595-107">Nicht alle Nachrichtenspeicher unterstützt diese Technik.</span><span class="sxs-lookup"><span data-stu-id="e9595-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="e9595-108">Bestimmen unterstützt, unabhängig davon, ob die Nachrichtenspeicher Sie verwenden die Verwendung von Suchergebnissen Ordner, rufen Sie seine [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der **PR\_STORE_SUPPORT_MASK** -Eigenschaft ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9595-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="e9595-109">Wenn das Flag STORE_SEARCH_OK festgelegt ist, wird die Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9595-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="e9595-110">Wenn es nicht festgelegt ist, benötigen Sie eine alternative Methode wie manuelle Überprüfung der Zielordner.</span><span class="sxs-lookup"><span data-stu-id="e9595-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="e9595-111">Suchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="e9595-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="e9595-112">Wenn Sie einen Ordner Suchergebnisse aus einem früheren Suchvorgang haben, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="e9595-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="e9595-113">Andernfalls, erstellen Sie einen Ordner-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="e9595-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="e9595-114">Rufen Sie die Eintrags-ID für den Stammordner-Ergebnisse der Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufrufen und Anfordern einer **PR_FINDER_ENTRYID** ([PidTagFinderEntryId ab](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9595-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="e9595-115">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen des Ordners durch PR_FINDER_ENTRYID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e9595-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="e9595-116">Rufen Sie den Ordner [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) -Methode zum Erstellen eines Suchergebnisse-Ordners mit der FOLDER_SEARCH-Flag.</span><span class="sxs-lookup"><span data-stu-id="e9595-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="e9595-117">Erstellen Sie eine Einschränkung, um Ihre Suchkriterien zu halten.</span><span class="sxs-lookup"><span data-stu-id="e9595-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="e9595-118">Erstellen Sie ein Array von Eintragsbezeichner, die den Ordner für die Suche darstellen.</span><span class="sxs-lookup"><span data-stu-id="e9595-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="e9595-119">Dieser Schritt ist nicht erforderlich, wenn der Suchergebnisse Ordner vor verwendet wurde und Sie die gleichen Ordner suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="e9595-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="e9595-120">Rufen Sie den Suchergebnisse Ordner [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode, die Eintrags-ID-Array und _LpRestriction_ die Beschränkung auf _LpContainerList_ .</span><span class="sxs-lookup"><span data-stu-id="e9595-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="e9595-121">Wenn Sie für die Suche abgeschlossen Benachrichtigungen mit dem Nachrichtenspeicher registriert haben, warten Sie auf die Benachrichtigung eingeht.</span><span class="sxs-lookup"><span data-stu-id="e9595-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="e9595-122">Zeigen Sie die Ergebnisse der Suche durch Aufrufen der Suchergebnisse des Ordners [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode zum Zugriff auf die Inhaltstabelle an.</span><span class="sxs-lookup"><span data-stu-id="e9595-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="e9595-123">Rufen Sie den Inhalt [der Tabelle QueryRows Abrufen die Nachrichten, die die Suchkriterien erfüllen](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="e9595-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

