---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427728"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="7bbd4-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7bbd4-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="7bbd4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bbd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bbd4-105">Erstellt eine Ratensenke, die eine vorhandene Ratensenke zur Threadsicherheit umschließt.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bbd4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7bbd4-106">Header file:</span></span>  <br/> |<span data-ttu-id="7bbd4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7bbd4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7bbd4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7bbd4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7bbd4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7bbd4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7bbd4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7bbd4-110">Called by:</span></span>  <br/> |<span data-ttu-id="7bbd4-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="7bbd4-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="7bbd4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bbd4-112">Parameters</span></span>

 <span data-ttu-id="7bbd4-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7bbd4-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7bbd4-114">[in] Zeiger auf die umbrochene Ratensenke.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="7bbd4-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7bbd4-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="7bbd4-116">[out] Zeiger auf einen Zeiger auf eine neue Hinweissenke, die die durch den  _lpAdviseSink-Parameter angezeigte_ Ratensenke umschließt.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7bbd4-117">Return value</span><span class="sxs-lookup"><span data-stu-id="7bbd4-117">Return value</span></span>

<span data-ttu-id="7bbd4-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7bbd4-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7bbd4-119">Remarks</span></span>

<span data-ttu-id="7bbd4-120">Der Zweck des Wrappers besteht im Sicherstellen, dass die Benachrichtigung für denselben Thread aufgerufen wird, der die **HrThisThreadAdviseSink-Funktion** aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="7bbd4-121">Diese Funktion wird verwendet, um Benachrichtigungsrückrufe zu schützen, die in einem bestimmten Thread ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="7bbd4-122">Clientanwendungen sollten **HrThisThreadAdviseSink** verwenden, um einzuschränken, wann Benachrichtigungen generiert werden, d. h. wenn Aufrufe an die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) des vom Client in einem vorherigen Advise-Aufruf übergebenen **Advise-Objekts** ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="7bbd4-123">Wenn Benachrichtigungen willkürlich generiert werden dürfen, kann eine Benachrichtigungsimplementierung einen Client zu einem Multithreadvorgang zwingen, wenn dies nicht angemessen wäre.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="7bbd4-124">Ein Client kann z. B. eine Bibliothek verwenden, z. B. eine der Microsoft Foundation-Klassenbibliotheken, die keine Multithreadaufrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="7bbd4-125">Eine Benachrichtigung in einem anderen Thread würde einen solchen Client schwer testen und fehleranfällig machen.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="7bbd4-126">**HrThisThreadAdviseSink** stellt sicher, dass **OnNotify-Aufrufe** nur zu den folgenden geeigneten Zeiten auftreten:</span><span class="sxs-lookup"><span data-stu-id="7bbd4-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="7bbd4-127">Während der Verarbeitung eines Aufrufs einer beliebigen MAPI-Methode.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="7bbd4-128">Während der Verarbeitung Windows Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="7bbd4-129">Wenn **HrThisThreadAdviseSink** implementiert ist, werden alle Aufrufe der **OnNotify-Methode** der neuen Ratensenke für jeden Thread dazu führen, dass die ursprüngliche Benachrichtigungsmethode für den Thread ausgeführt wird, in dem **HrThisThreadAdviseSink** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bbd4-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="7bbd4-130">Weitere Informationen zu Benachrichtigungs- und Hinweissenken finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Implementieren eines Advise Sink-Objekts](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="7bbd4-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

