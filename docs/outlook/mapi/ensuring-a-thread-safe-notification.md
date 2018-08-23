---
title: Sicherstellen einer threadsicheren Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585304"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="b7e2f-103">Sicherstellen einer threadsicheren Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b7e2f-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="b7e2f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7e2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7e2f-105">Wenn der Client auf eine Multithread-Plattform ausgeführt wird, benötigen Sie möglicherweise die Assurance, dass Anrufe an Ihre [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Methoden für einen bestimmten Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="b7e2f-106">Da Anrufe an **OnNotify** in der Regel auf einem beliebigen Thread auftreten können, ist es möglich, Benachrichtigung bei unerwarteten und unerwünschte Threads, führt zu Fehlern, die schwierig zu debuggen sind.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="b7e2f-107">Sicherstellen, dass Anrufe an **OnNotify** für eine bestimmte Benachrichtigung rufen Sie auf dem gleichen Thread, der für die **Advise** verwendet wurde, rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) vor **Advise**vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="b7e2f-108">\*\* \*\* HrThisThreadAdviseSink \*\*\* erstellt ein neues Advise-Empfänger-Objekt aus der Advise-Empfängerobjekt.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="b7e2f-109">Übergeben Sie den Anruf an **Advise**dieses neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="b7e2f-110">Alle Clients mit Advise-Empfänger,-Objekten, die möglicherweise nicht außerhalb des Kontexts von einem bestimmten Thread verwendet werden sollte immer registrieren, advise-Empfängerobjekten mit **HrThisThreadAdviseSink**erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7e2f-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

