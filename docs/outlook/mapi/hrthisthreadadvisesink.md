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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346837"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="31d34-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="31d34-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="31d34-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31d34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31d34-105">Erstellt eine Advise-Senke, die eine vorhandene Advise-Senke für die Threadsicherheit umschließt.</span><span class="sxs-lookup"><span data-stu-id="31d34-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31d34-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="31d34-106">Header file:</span></span>  <br/> |<span data-ttu-id="31d34-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="31d34-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="31d34-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="31d34-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31d34-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31d34-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31d34-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="31d34-110">Called by:</span></span>  <br/> |<span data-ttu-id="31d34-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="31d34-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="31d34-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d34-112">Parameters</span></span>

 <span data-ttu-id="31d34-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="31d34-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="31d34-114">in Zeiger auf die zu umhüllende Advise-Senke.</span><span class="sxs-lookup"><span data-stu-id="31d34-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="31d34-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="31d34-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="31d34-116">Out Zeiger auf einen Zeiger auf eine neue Advise-Senke, die die Advise-Senke umschließt, auf die durch den _lpAdviseSink_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="31d34-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31d34-117">Return value</span><span class="sxs-lookup"><span data-stu-id="31d34-117">Return value</span></span>

<span data-ttu-id="31d34-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="31d34-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31d34-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d34-119">Remarks</span></span>

<span data-ttu-id="31d34-120">Der Zweck des Wrappers besteht darin, sicherzustellen, dass die Benachrichtigung für den gleichen Thread aufgerufen wird, der die **HrThisThreadAdviseSink** -Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="31d34-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="31d34-121">Diese Funktion wird verwendet, um Benachrichtigungsrückrufe zu schützen, die für einen bestimmten Thread ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="31d34-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="31d34-122">Client Anwendungen sollten **HrThisThreadAdviseSink** verwenden, um zu beschränken, wenn Benachrichtigungen generiert werden, das heißt, wenn Aufrufe an die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode des Advise-Senke-Objekts durchgeführt werden, das vom Client in einer vorherigen Advise übergeben wurde. \*\* \*\*Anruf.</span><span class="sxs-lookup"><span data-stu-id="31d34-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="31d34-123">Wenn Benachrichtigungen zulässig sind, willkürlich zu generieren, kann eine Benachrichtigungs Implementierung einen Client in Multithread-Betrieb zwingen, wenn dies nicht angemessen wäre.</span><span class="sxs-lookup"><span data-stu-id="31d34-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="31d34-124">Beispielsweise kann ein Client eine Bibliothek verwenden, wie etwa eine der Microsoft Foundation Class-Bibliotheken, die Multithread-Aufrufe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31d34-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="31d34-125">Die Benachrichtigung in einem anderen Thread würde einen solchen Client schwer testen und fehleranfällig machen.</span><span class="sxs-lookup"><span data-stu-id="31d34-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="31d34-126">**HrThisThreadAdviseSink** stellt sicher, \*\*\*\* dass OnNotify-Aufrufe nur zu diesen geeigneten Zeiten stattfinden:</span><span class="sxs-lookup"><span data-stu-id="31d34-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="31d34-127">Während der Verarbeitung eines Aufrufs an eine beliebige MAPI-Methode.</span><span class="sxs-lookup"><span data-stu-id="31d34-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="31d34-128">Während der Verarbeitung von Windows-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="31d34-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="31d34-129">Wenn **HrThisThreadAdviseSink** implementiert wird, führen Aufrufe der OnNotify-Methode der \*\*\*\* neuen Advise-Senke in einem Thread dazu, dass die ursprüngliche Benachrichtigungsmethode für den Thread ausgeführt wird, in dem **HrThisThreadAdviseSink** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="31d34-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="31d34-130">Weitere Informationen zu Benachrichtigungs-und Advise-Senken finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Implementieren eines Advise](implementing-an-advise-sink-object.md)-Senke-Objekts.</span><span class="sxs-lookup"><span data-stu-id="31d34-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

