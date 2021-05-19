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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426037"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="d4eaa-103">Durchsuchen eines Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="d4eaa-103">Searching a message store</span></span>

<span data-ttu-id="d4eaa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4eaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4eaa-105">Clientanwendungen können einen oder mehrere Ordner durchsuchen, die nach Nachrichten suchen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="d4eaa-106">Die unkomplizierteste Suchmethode umfasst das Anwenden einer Einschränkung zum Definieren von Kriterien und das Platzieren der Ergebnisse in einem Suchergebnisordner, der explizit für diese Suche oder für eine vorherige Suche erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="d4eaa-107">Nicht alle Nachrichtenspeicher unterstützen diese Technik.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="d4eaa-108">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) auf, um zu bestimmen, ob der von Ihnen verwendete Nachrichtenspeicher die Verwendung von Suchergebnissen unterstützt, um die **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="d4eaa-109">Wenn das STORE_SEARCH_OK festgelegt ist, wird die Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="d4eaa-110">Wenn sie nicht festgelegt ist, benötigen Sie einen alternativen Ansatz, z. B. die manuelle Überprüfung der Zielordner.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="d4eaa-111">So durchsuchen Sie einen oder mehrere Ordner in einem Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="d4eaa-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="d4eaa-112">Wenn Sie über einen Suchergebnisordner aus einer vorherigen Suche verfügen, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="d4eaa-113">Andernfalls, um einen Suchergebnisordner zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d4eaa-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="d4eaa-114">Rufen Sie die Eintrags-ID für den Stammordner der Suchergebnisse ab, indem Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers aufrufen und PR_FINDER_ENTRYID **(** [PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) anfordern.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="d4eaa-115">Rufen [Sie IMsgStore::OpenEntry auf,](imsgstore-openentry.md) um den durch die Datei dargestellten Ordner PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="d4eaa-116">Rufen Sie die [IMAPIFolder::CreateFolder-Methode](imapifolder-createfolder.md) des Ordners auf, um einen Suchergebnisordner mit dem FOLDER_SEARCH zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="d4eaa-117">Erstellen Sie eine Einschränkung, um Ihre Suchkriterien zu halten.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="d4eaa-118">Erstellen Sie ein Array von Eintragsbezeichnern, die die zu durchsuchenden Ordner darstellen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="d4eaa-119">Dieser Schritt ist nicht erforderlich, wenn der Suchergebnisordner bereits verwendet wurde und Sie dieselben Ordner durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="d4eaa-120">Rufen Sie die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Suchergebnisordners auf, und zeigen Sie  _lpContainerList_ auf das Eintragsbezeichnerarray und  _lpRestriction_ auf die Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="d4eaa-121">Wenn Sie sich für die Suche mit vollständigen Benachrichtigungen beim Nachrichtenspeicher registriert haben, warten Sie, bis die Benachrichtigung eintrifft.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="d4eaa-122">Zeigen Sie die Ergebnisse der Suche an, indem Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Suchergebnisordners aufrufen, um auf die Inhaltstabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="d4eaa-123">Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Inhaltstabelle auf, um die Nachrichten abzurufen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d4eaa-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

