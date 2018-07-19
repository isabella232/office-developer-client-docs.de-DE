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
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791967"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="98d8d-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="98d8d-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="98d8d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98d8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98d8d-105">Erstellt eine Advise-Empfänger, der eine vorhandene Advise-Empfänger für Threadsicherheit umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="98d8d-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98d8d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="98d8d-106">Header file:</span></span>  <br/> |<span data-ttu-id="98d8d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="98d8d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98d8d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="98d8d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98d8d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98d8d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98d8d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="98d8d-110">Called by:</span></span>  <br/> |<span data-ttu-id="98d8d-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="98d8d-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="98d8d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98d8d-112">Parameters</span></span>

 <span data-ttu-id="98d8d-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="98d8d-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="98d8d-114">[in] Zeiger auf die Advise-Empfänger umgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="98d8d-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="98d8d-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="98d8d-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="98d8d-116">[out] Zeiger auf einen Zeiger auf eine neue Advise-Empfänger, der auf das durch den Parameter _LpAdviseSink_ Advise-Empfänger umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="98d8d-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98d8d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98d8d-117">Return value</span></span>

<span data-ttu-id="98d8d-118">None.</span><span class="sxs-lookup"><span data-stu-id="98d8d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98d8d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98d8d-119">Remarks</span></span>

<span data-ttu-id="98d8d-120">Der Zweck des Wrappers ist dafür sorgen, dass die Benachrichtigung auf dem gleichen Thread aufgerufen wird, die die **HrThisThreadAdviseSink** -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="98d8d-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="98d8d-121">Diese Funktion wird verwendet, um Benachrichtigung Rückrufe zu schützen, die für einen bestimmten Thread ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="98d8d-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="98d8d-122">Clientanwendungen sollten **HrThisThreadAdviseSink** verwenden, um einzuschränken, wenn Benachrichtigungen generiert werden, d. h., wenn Anrufe an die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode von der Advise-Empfängerobjekt vom Client in einem vorherigen **Advise übergeben werden **aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98d8d-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="98d8d-123">Wenn Benachrichtigungen an willkürlich generiert werden dürfen, möglicherweise eine Benachrichtigung Implementierung ein Clients in Multithread-Vorgang erzwingen, wenn, die nicht geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="98d8d-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="98d8d-124">Beispielsweise kann ein Client eine Bibliothek beispielsweise eine der Microsoft Foundation Class Libraries, verwenden, die keine Multithread-Anrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98d8d-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="98d8d-125">Benachrichtigung für einen anderen Thread würde solcher Client schwierig zu testen und fehleranfällig, stellen.</span><span class="sxs-lookup"><span data-stu-id="98d8d-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="98d8d-126">**HrThisThreadAdviseSink** stellt sicher, dass nur diese geeigneten Zeitpunkt **OnNotify** -Aufrufe erfolgen:</span><span class="sxs-lookup"><span data-stu-id="98d8d-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="98d8d-127">Während der Verarbeitung eines Anrufs an eine beliebige MAPI-Methode.</span><span class="sxs-lookup"><span data-stu-id="98d8d-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="98d8d-128">Während der Verarbeitung von Windows-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="98d8d-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="98d8d-129">Wenn **HrThisThreadAdviseSink** implementiert wird, führen dazu, dass alle Anrufe an die neue Advise-Empfänger **OnNotify** -Methode auf einem beliebigen Thread die ursprünglichen Benachrichtigungsmethode für den Thread ausgeführt werden, auf dem **HrThisThreadAdviseSink** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="98d8d-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="98d8d-130">Weitere Informationen zur Benachrichtigung und advise-Empfänger, finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md) und [Implementieren eines Objekts beraten Auffangen verwenden](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="98d8d-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

