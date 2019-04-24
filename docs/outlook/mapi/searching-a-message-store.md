---
title: Durchsuchen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338801"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="0546b-103">Durchsuchen eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="0546b-103">Searching a message store</span></span>

<span data-ttu-id="0546b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0546b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0546b-105">Client Anwendungen können einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0546b-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="0546b-106">Die einfachste Suchmethode umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und das Platzieren der Ergebnisse in einem Suchergebnisordner, der explizit für diese Suche oder für eine vorherige Suche erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0546b-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="0546b-107">Diese Technik wird nicht von allen Nachrichten speichern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0546b-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="0546b-108">Um zu bestimmen, ob der von Ihnen verwendete Nachrichtenspeicher mithilfe von Suchergebnis Ordnern unterstützt, rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode auf, um die **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0546b-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="0546b-109">Wenn das STORE_SEARCH_OK-Flag festgelegt ist, wird die Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0546b-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="0546b-110">Wenn Sie nicht festgelegt ist, benötigen Sie einen alternativen Ansatz wie die manuelle Überprüfung der Zielordner.</span><span class="sxs-lookup"><span data-stu-id="0546b-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="0546b-111">So durchsuchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="0546b-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="0546b-112">Wenn Sie einen Suchergebnisordner aus einer früheren Suche haben, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="0546b-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="0546b-113">Andernfalls können Sie einen Suchergebnisordner erstellen:</span><span class="sxs-lookup"><span data-stu-id="0546b-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="0546b-114">Rufen Sie die Eintrags-ID für den Suchergebnis-Stammordner ab, indem Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers aufrufen und **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md)) anfordern.</span><span class="sxs-lookup"><span data-stu-id="0546b-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="0546b-115">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um den durch PR_FINDER_ENTRYID dargestellten Ordner zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0546b-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="0546b-116">Rufen Sie die [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) -Methode des Ordners auf, um einen Ordner mit Suchergebnissen mit dem FOLDER_SEARCH-Kennzeichen Satz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0546b-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="0546b-117">Erstellen Sie eine Einschränkung für Ihre Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="0546b-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="0546b-118">Erstellen Sie ein Array von Eintrags Bezeichnern, die die zu durchsuchenden Ordner darstellen.</span><span class="sxs-lookup"><span data-stu-id="0546b-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="0546b-119">Dieser Schritt ist nicht erforderlich, wenn der Ordner Suchergebnisse zuvor verwendet wurde und Sie die gleichen Ordner durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="0546b-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="0546b-120">Rufen Sie die [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode des Suchergebnis Ordners auf, und zeigen Sie _lpContainerList_ auf das Array Eintrags-ID und _lpRestriction_ auf die Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="0546b-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="0546b-121">Wenn Sie sich mit dem Nachrichtenspeicher für vollständige Benachrichtigungen bei der Suche registriert haben, warten Sie, bis die Benachrichtigung eingeht.</span><span class="sxs-lookup"><span data-stu-id="0546b-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="0546b-122">Zeigen Sie die Ergebnisse der Suche an, indem Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Search-results-Ordners aufrufen, um auf die Inhaltstabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0546b-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="0546b-123">Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Inhaltstabelle auf, um die Nachrichten abzurufen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0546b-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

