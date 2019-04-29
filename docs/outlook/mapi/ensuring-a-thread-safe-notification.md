---
title: Sicherstellen einer Thread sicheren Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424847"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="9f929-103">Sicherstellen einer Thread sicheren Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="9f929-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="9f929-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f929-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f929-105">Wenn Ihr Client auf einer Multithread-Plattform ausgeführt wird, müssen Sie möglicherweise sicherstellen, dass Aufrufe an Ihre [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methoden in einem bestimmten Thread stattfinden.</span><span class="sxs-lookup"><span data-stu-id="9f929-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="9f929-106">Da Aufrufe von **OnNotify** in der Regel in einem beliebigen Thread auftreten können, ist es möglich, Benachrichtigungen zu unerwarteten und unerwünschten Threads zu erhalten, was zu Fehlern führt, die schwierig zu Debuggen sind.</span><span class="sxs-lookup"><span data-stu-id="9f929-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="9f929-107">Um sicherzustellen, dass Aufrufe von onNotify für eine bestimmte Benachrichtigung für den gleichen Thread ausgeführt werden, der für den **Advise** -Aufruf verwendet wurde, rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, bevor **Sie** **Advise**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9f929-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="9f929-108">\* \* \* \* HrThisThreadAdviseSink \* \* \* \* erstellt ein neues Advise-Senke-Objekt aus dem Advise-Senke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f929-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="9f929-109">Führen Sie dieses neue Objekt im Aufruf von **Advise**aus.</span><span class="sxs-lookup"><span data-stu-id="9f929-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="9f929-110">Alle Clients mit Advise-Senke-Objekten, die möglicherweise nicht außerhalb des Kontexts eines bestimmten Threads funktionieren, sollten immer Advise-Senke-Objekte registrieren, die mit **HrThisThreadAdviseSink**erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f929-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

