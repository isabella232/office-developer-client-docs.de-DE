---
title: Informationen zum benachrichtigungsbasierten Indizieren von Stores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791224"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="07603-103">Informationen zum benachrichtigungsbasierten Indizieren von Stores</span><span class="sxs-lookup"><span data-stu-id="07603-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="07603-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07603-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07603-105">Ein MAPI-Anbieter kann angeben, ob der MAPI-Protokollhandler Durchforstungen und Indizes im Speicher Nachrichten oder gibt an, ob der Speicher sendet Benachrichtigungen die Indizierung sind Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="07603-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="07603-106">Da letztere als Benachrichtigung-basierte Indizierung bezeichnet wird, und ein Speicher, der Benachrichtigung-basierte Indizierung unterstützt, ist ein bekanntes als Pusher Speicher.</span><span class="sxs-lookup"><span data-stu-id="07603-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="07603-107">Ein Store-Anbieter, der Benachrichtigung-basierte Indizierung legt das Flag **STORE_PUSHER_OK** in die **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** -Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07603-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="07603-108">Der MAPI-Protokollhandler oder einen Client kann die **PR_STORE_SUPPORT_MASK** -Eigenschaft zum Ermitteln der Merkmale des Speichers abrufen.</span><span class="sxs-lookup"><span data-stu-id="07603-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="07603-109">Wenn eine Anlage, Ordner oder eine Nachricht zu indizierenden vorhanden ist, Speicheranbieter generiert ein MAPI-Uniform Resource Locator (URL) zur Identifizierung des Objekts für die Indizierung und sendet ihn an die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="07603-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="07603-110">Der MAPI-URL ist in Unicode codiert und muss eindeutig das Objekt, das den MAPI-Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="07603-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="07603-111">Weitere Informationen zu MAPI-URLs finden Sie unter [Informationen zu MAPI-URLs für Benachrichtigung-basierte Indizierung](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="07603-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="07603-112">Da Indexer immer alles nicht indiziert werden vor dem Herunterfahren in einem Speicher Pusher, muss Pusher Speicher beibehalten was abgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="07603-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="07603-113">Wenn ein Anbieter zu einem Objekt eine Benachrichtigung, die indiziert werden soll sendet, gibt die Benachrichtigung Typ **FnevIndexing** im **UlEventType** -Member der Struktur **[Benachrichtigung](notification.md)** an.</span><span class="sxs-lookup"><span data-stu-id="07603-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="07603-114">Der **Info** -Member der Struktur **Benachrichtigung** enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="07603-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="07603-115">Speicheranbieter identifiziert den Prozess in der **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="07603-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="07603-116">Auch identifiziert den Prozess der [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) -Struktur, und übergibt diese Informationen im Rahmen der **PbEventParameters** Mitglied der **EXTENDED_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="07603-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="07603-117">Wenn der Prozess heruntergefahren wird oder stürzt ab, wird der MAPI-Protokollhandler werden sofort zu erkennen, und beenden Sie den Pusher Speicher Indizierung.</span><span class="sxs-lookup"><span data-stu-id="07603-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07603-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07603-118">See also</span></span>



[<span data-ttu-id="07603-119">Informationen zur Store-API</span><span class="sxs-lookup"><span data-stu-id="07603-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="07603-120">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="07603-120">MAPI Constants</span></span>](mapi-constants.md)

