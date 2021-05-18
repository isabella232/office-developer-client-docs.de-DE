---
title: Informationen Notification-Based Store-Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409174"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="226a1-103">Informationen Notification-Based Store-Indizierung</span><span class="sxs-lookup"><span data-stu-id="226a1-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="226a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="226a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="226a1-105">Ein MAPI-Speicheranbieter kann angeben, ob der MAPI-Protokollhandler Nachrichten im Speicher durchforstet und indiziert oder ob der Speicher Benachrichtigungen an den Indexer sendet, wenn Nachrichten indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="226a1-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="226a1-106">Letzteres wird als benachrichtigungsbasierte Indizierung bezeichnet, und ein Speicher, der die benachrichtigungsbasierte Indizierung unterstützt, wird als Pushspeicher bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="226a1-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="226a1-107">Ein Speicheranbieter, der die benachrichtigungsbasierte Indizierung unterstützt, legt **das** STORE_PUSHER_OK in **[der](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK fest.</span><span class="sxs-lookup"><span data-stu-id="226a1-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="226a1-108">Der MAPI-Protokollhandler oder ein Client kann die **PR_STORE_SUPPORT_MASK,um** die Merkmale des Speichers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="226a1-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="226a1-109">Wenn eine Anlage, ein Ordner oder eine Nachricht indiziert werden soll, generiert der Speicheranbieter einen MAPI Uniform Resource Locator (URL), der das zu indizierte Objekt identifiziert und an den Indexer sendet.</span><span class="sxs-lookup"><span data-stu-id="226a1-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="226a1-110">Diese MAPI-URL ist in Unicode codiert und muss das Objekt für den MAPI-Protokollhandler eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="226a1-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="226a1-111">Weitere Informationen zu MAPI-URLs finden Sie unter [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="226a1-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="226a1-112">Da ein Indexer nicht immer alles indizieren kann, bevor ein Herunterfahren in einem Pushspeicher stattfindet, muss der Pushspeicher beibehalten, was pusht werden muss.</span><span class="sxs-lookup"><span data-stu-id="226a1-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="226a1-113">Wenn ein Speicheranbieter eine Benachrichtigung über ein Objekt sendet, das indiziert werden muss, gibt er den Benachrichtigungstyp **fnevIndexing** im **ulEventType-Element** der **[NOTIFICATION-Struktur](notification.md)** an.</span><span class="sxs-lookup"><span data-stu-id="226a1-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="226a1-114">Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="226a1-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="226a1-115">Der Speicheranbieter identifiziert den **[](pidtagsearchownerid-canonical-property.md)** Prozess in der PR_SEARCH_OWNER_ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="226a1-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="226a1-116">Außerdem wird der Prozess in der INDEX_SEARCH_PUSHER_PROCESS [identifiziert](index_search_pusher_process.md) und diese Informationen als Teil des **pbEventParameters-Mitglieds** der EXTENDED_NOTIFICATION **werden.**</span><span class="sxs-lookup"><span data-stu-id="226a1-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="226a1-117">Wenn der Prozess heruntergefahren oder abstürzt, kann der MAPI-Protokollhandler dies sofort erkennen und die Indizierung des Pushspeichers beenden.</span><span class="sxs-lookup"><span data-stu-id="226a1-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="226a1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="226a1-118">See also</span></span>



[<span data-ttu-id="226a1-119">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="226a1-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="226a1-120">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="226a1-120">MAPI Constants</span></span>](mapi-constants.md)

