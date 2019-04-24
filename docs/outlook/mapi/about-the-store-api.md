---
title: Informationen zur Speicher-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321749"
---
# <a name="about-the-store-api"></a><span data-ttu-id="bd88e-103">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="bd88e-103">About the Store API</span></span>

  
  
<span data-ttu-id="bd88e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd88e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd88e-105">Die Informationsspeicher-API bietet Speicheranbietern verschiedene Speicherfunktionen.</span><span class="sxs-lookup"><span data-stu-id="bd88e-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="bd88e-106">Es bietet die folgenden Definitionen, Datentypen, Eigenschaften und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="bd88e-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="bd88e-107">Definitionen:</span><span class="sxs-lookup"><span data-stu-id="bd88e-107">Definitions:</span></span>
  
- [<span data-ttu-id="bd88e-108">Konstanten für die Speicher-API</span><span class="sxs-lookup"><span data-stu-id="bd88e-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="bd88e-109">Datentypen:</span><span class="sxs-lookup"><span data-stu-id="bd88e-109">Data types:</span></span>
  
- <span data-ttu-id="bd88e-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="bd88e-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="bd88e-112">Benannte Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd88e-112">Named Properties:</span></span>
  
- <span data-ttu-id="bd88e-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="bd88e-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="bd88e-115">**[Größe des Anzeige Server Ordners](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-116">**[Option "Besprechungs Update ausblenden"](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-117">**[Speichertyp als privat festlegen](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="bd88e-119">Speicheranbieter, die keine der von diesen benannten Eigenschaften angebotenen Funktionen erfordern, können diese einfach ignorieren und keine Unterstützung in der **IMAPIProp** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="bd88e-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="bd88e-120">Da diese Eigenschaften ab Microsoft Outlook 2003 Service Pack 1 bereitgestellt werden, hat das Hinzufügen zu einem Speicher in einer früheren Version von Microsoft Outlook keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="bd88e-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="bd88e-121">Sie werden ignoriert, wenn Sie nicht vorhanden sind oder ihr Wert **false**ist.</span><span class="sxs-lookup"><span data-stu-id="bd88e-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="bd88e-122">Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd88e-122">Properties:</span></span>
  
- <span data-ttu-id="bd88e-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="bd88e-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="bd88e-127">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="bd88e-127">Interfaces:</span></span>
  
- <span data-ttu-id="bd88e-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="bd88e-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="bd88e-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="bd88e-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="bd88e-131">Registrieren von Speichern für die Indizierung</span><span class="sxs-lookup"><span data-stu-id="bd88e-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="bd88e-132">Der MAPI-Protokoll Handler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd88e-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="bd88e-133">Speicheranbieter, die indiziert werden sollen, müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="bd88e-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="bd88e-134">Weitere Informationen zum Registrieren von Speicheranbietern für die Indizierung in Outlook 2013 oder Outlook 2010 finden Sie unter Informationen [zum Registrieren](about-registering-stores-for-indexing.md)von Speicher für die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="bd88e-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="bd88e-135">Indexspeicher</span><span class="sxs-lookup"><span data-stu-id="bd88e-135">Indexing Stores</span></span>

<span data-ttu-id="bd88e-136">MAPI-Speicheranbieter können festlegen, dass der MAPI-Protokoll Handler Nachrichten im Speicher Crawlen und indizieren soll, oder Benachrichtigungen an den Indexer senden, wenn Nachrichten indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd88e-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="bd88e-137">Weitere Informationen zur Benachrichtigungen-basierten Indizierung finden Sie unter [Informationen zu Benachrichtigungs basiertEr Speicher Indizierung](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="bd88e-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

