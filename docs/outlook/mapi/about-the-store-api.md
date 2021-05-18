---
title: Informationen zur Speicher-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405555"
---
# <a name="about-the-store-api"></a><span data-ttu-id="dd6d1-103">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="dd6d1-103">About the Store API</span></span>

  
  
<span data-ttu-id="dd6d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd6d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd6d1-105">Die Store-API stellt verschiedene Speicherfunktionen für Speicheranbieter bereit.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="dd6d1-106">Es enthält die folgenden Defintions, Datentypen, Eigenschaften und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="dd6d1-107">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="dd6d1-107">Definitions:</span></span>
  
- [<span data-ttu-id="dd6d1-108">Konstanten für die Store-API</span><span class="sxs-lookup"><span data-stu-id="dd6d1-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="dd6d1-109">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="dd6d1-109">Data types:</span></span>
  
- <span data-ttu-id="dd6d1-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="dd6d1-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="dd6d1-112">Benannte Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dd6d1-112">Named Properties:</span></span>
  
- <span data-ttu-id="dd6d1-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="dd6d1-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="dd6d1-115">**[Größe des Anzeigeserverordners](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-116">**[Option zum Ausblenden von Besprechungsupdates](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-117">**[Make Store Type Private](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="dd6d1-119">Store, die keine der Funktionen dieser benannten Eigenschaften benötigen, können sie einfach ignorieren und keine Unterstützung in der **IMAPIProp-Schnittstelle** implementieren.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="dd6d1-120">Da diese Eigenschaften ab Microsoft Outlook 2003 Service Pack 1 bereitgestellt werden, hat das Hinzufügen zu einem Store in einer früheren Version von Microsoft Outlook keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="dd6d1-121">Sie werden ignoriert, wenn sie nicht vorhanden sind oder ihr Wert false **ist.**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="dd6d1-122">Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dd6d1-122">Properties:</span></span>
  
- <span data-ttu-id="dd6d1-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="dd6d1-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="dd6d1-127">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="dd6d1-127">Interfaces:</span></span>
  
- <span data-ttu-id="dd6d1-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="dd6d1-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="dd6d1-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6d1-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="dd6d1-131">Registrieren von Informationsspeichern für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="dd6d1-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="dd6d1-132">Der MAPI-Protokollhandler überprüft die Windows für Speicher, die zu Suchzwecken indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="dd6d1-133">Store, die indiziert werden möchten, müssen in der Registrierung Windows werden.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="dd6d1-134">Weitere Informationen zum Registrieren von Speicheranbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="dd6d1-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="dd6d1-135">Indizierungsspeicher</span><span class="sxs-lookup"><span data-stu-id="dd6d1-135">Indexing Stores</span></span>

<span data-ttu-id="dd6d1-136">MAPI-Speicheranbieter können festlegen, dass der MAPI-Protokollhandler Nachrichten im Speicher durchforstet und indiziert oder Benachrichtigungen nur dann an den Indexer sendet, wenn Nachrichten indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd6d1-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="dd6d1-137">Weitere Informationen zur Benachrichtigungsbasierten Indizierung finden Sie unter [Informationen Notification-Based Store Indizierung](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="dd6d1-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

