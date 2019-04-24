---
title: Informationen zu Benachrichtigungs basierter Speicher Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322134"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="39fa0-103">Informationen zu Benachrichtigungs basierter Speicher Indizierung</span><span class="sxs-lookup"><span data-stu-id="39fa0-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="39fa0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39fa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39fa0-105">Ein MAPI-Speicheranbieter kann angeben, ob der MAPI-Protokoll Handler Nachrichten im Speicher durchforstet und indiziert, oder ob der Informationsspeicher Benachrichtigungen an den Indexer sendet, wenn Nachrichten indiziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39fa0-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="39fa0-106">Letztere wird als Benachrichtigungs basierte Indizierung bezeichnet, und ein Speicher, der die Benachrichtigungs basierte Indizierung unterstützt, wird als Pusher-Speicher bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39fa0-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="39fa0-107">Ein Informationsspeicher Anbieter, der die Benachrichtigungs basierte Indizierung unterstützt, legt das **STORE_PUSHER_OK** -Flag in der **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="39fa0-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="39fa0-108">Der MAPI-Protokoll Handler oder ein Client kann die **PR_STORE_SUPPORT_MASK** -Eigenschaft abrufen, um die Eigenschaften des Speichers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="39fa0-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="39fa0-109">Wenn eine Anlage, ein Ordner oder eine Nachricht indiziert werden soll, generiert der Speicheranbieter einen MAPI-URL (Uniform Resource Locator), der das zu indizierende Objekt identifiziert und es an den Indexer sendet.</span><span class="sxs-lookup"><span data-stu-id="39fa0-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="39fa0-110">Diese MAPI-URL ist in Unicode codiert und muss das Objekt eindeutig dem MAPI-Protokoll Handler zuordnen.</span><span class="sxs-lookup"><span data-stu-id="39fa0-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="39fa0-111">Weitere Informationen zu MAPI-URLs finden Sie unter [Informationen zu MAPI-URLs für die Benachrichtigungs basierte Indizierung](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="39fa0-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="39fa0-112">Da ein Indexer nicht immer alles indizieren kann, bevor ein Herunterfahren in einem Pusher-Speicher erfolgt, muss der Pusher-Speicher beibehalten, was verschoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="39fa0-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="39fa0-113">Wenn ein Informationsspeicher Anbieter eine Benachrichtigung über ein Objekt sendet, das indiziert werden muss, gibt es den Benachrichtigungstyp **fnevIndexing** im **ulEventType** -Element der **[Benachrichtigungs](notification.md)** Struktur an.</span><span class="sxs-lookup"><span data-stu-id="39fa0-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="39fa0-114">Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="39fa0-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="39fa0-115">Der Informationsspeicher Anbieter identifiziert den Prozess in der **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="39fa0-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="39fa0-116">Außerdem wird der Prozess in der [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) -Struktur identifiziert, und diese Informationen werden als Teil des **pbEventParameters** -Elements der **EXTENDED_NOTIFICATION** -Struktur übergeben.</span><span class="sxs-lookup"><span data-stu-id="39fa0-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="39fa0-117">Wenn der Prozess heruntergefahren oder abstürzt, kann der MAPI-Protokoll Handler sofort feststellen, dass die Indizierung des Pusher-Speichers beendet wird.</span><span class="sxs-lookup"><span data-stu-id="39fa0-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39fa0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39fa0-118">See also</span></span>



[<span data-ttu-id="39fa0-119">Informationen zur Speicher-API</span><span class="sxs-lookup"><span data-stu-id="39fa0-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="39fa0-120">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="39fa0-120">MAPI Constants</span></span>](mapi-constants.md)

