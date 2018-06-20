---
title: Über den API-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791254"
---
# <a name="about-the-store-api"></a><span data-ttu-id="1519c-103">Über den API-Speicher</span><span class="sxs-lookup"><span data-stu-id="1519c-103">About the Store API</span></span>

  
  
<span data-ttu-id="1519c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1519c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1519c-105">Die speichern-API bietet verschiedene Speicherfunktionalität zum Speichern von Anbietern.</span><span class="sxs-lookup"><span data-stu-id="1519c-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="1519c-106">Es bietet die folgenden Definitionen Datentypen, Eigenschaften und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1519c-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="1519c-107">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="1519c-107">Definitions:</span></span>
  
- [<span data-ttu-id="1519c-108">Konstanten für den API-Speicher</span><span class="sxs-lookup"><span data-stu-id="1519c-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="1519c-109">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="1519c-109">Data types:</span></span>
  
- <span data-ttu-id="1519c-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="1519c-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="1519c-112">Benannte Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1519c-112">Named Properties:</span></span>
  
- <span data-ttu-id="1519c-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1519c-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1519c-115">**[Ordnergröße Server anzeigen](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="1519c-116">**[Ausblenden der Besprechung Update-Option](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="1519c-117">**[Stellen Sie Store Typ Private](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="1519c-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="1519c-119">Anbieter, die nicht über die Funktionalität dieser benannten Eigenschaften erfordern können einfach ignoriert werden sollen und nicht Support in der **IMAPIProp** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="1519c-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="1519c-120">Da diese Eigenschaften in Microsoft Outlook 2003 Service Pack 1 beginnende verfügbar sind, hat einen Speicher in einer früheren Version von Microsoft Outlook hinzugefügt keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="1519c-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="1519c-121">Wenn sie nicht vorhanden sind oder deren Wert **false**ist, werden sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1519c-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="1519c-122">Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1519c-122">Properties:</span></span>
  
- <span data-ttu-id="1519c-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1519c-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1519c-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1519c-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="1519c-127">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="1519c-127">Interfaces:</span></span>
  
- <span data-ttu-id="1519c-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="1519c-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="1519c-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="1519c-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="1519c-131">Registrieren Speicher für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="1519c-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="1519c-132">Der MAPI-Protokollhandler überprüft die Windows-Registrierung für Geschäfte, die indiziert werden soll für die Suche.</span><span class="sxs-lookup"><span data-stu-id="1519c-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="1519c-133">Speicheranbieter, die indiziert werden soll, müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="1519c-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="1519c-134">Weitere Informationen zum Registrieren von Anbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter [Informationen zum Registrieren-Speicher für die Indizierung](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="1519c-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="1519c-135">Speichert die Indizierung</span><span class="sxs-lookup"><span data-stu-id="1519c-135">Indexing Stores</span></span>

<span data-ttu-id="1519c-136">MAPI-Anbieter können wahlweise den MAPI-Protokollhandler zum Durchforsten und Indizieren von Nachrichten im Speicher zulassen oder Senden von Benachrichtigungen an die Indizierung, nur, wenn Nachrichten indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1519c-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="1519c-137">Weitere Informationen zu Benachrichtigungen-basierte Indizierung finden Sie unter [About Notification-Based Store indizieren](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="1519c-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

