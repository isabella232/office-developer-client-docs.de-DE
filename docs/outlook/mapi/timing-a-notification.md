---
title: Timing einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411148"
---
# <a name="timing-a-notification"></a><span data-ttu-id="20125-103">Timing einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="20125-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="20125-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20125-105">Da es sich bei der Ereignisbenachrichtigung um einen asynchronen Prozess handelt, können Sie jederzeit benachrichtigt werden, nicht unbedingt unmittelbar nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="20125-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="20125-106">Der Zeitpunkt der Anrufe an Ihre [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) variiert je nach Dienstanbieter, der die Ratgeberquelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="20125-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="20125-107">Dienstanbieter können Ihren Client entweder benachrichtigen:</span><span class="sxs-lookup"><span data-stu-id="20125-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="20125-108">Gleichzeitig mit dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="20125-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="20125-109">Direkt nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="20125-109">Directly after the event.</span></span>
    
- <span data-ttu-id="20125-110">Zu einem späteren Zeitpunkt nach dem Ereignis, möglicherweise nach einem **Unadvise-Aufruf.**</span><span class="sxs-lookup"><span data-stu-id="20125-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="20125-111">Die meisten Dienstanbieter rufen **OnNotify** auf, nachdem die für das Ereignis zuständige MAPI-Methode an den Aufrufer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="20125-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="20125-112">Beispielsweise werden Benachrichtigungen zu Nachrichten gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) oder wenn die Nachricht nach dem **IUnknown::Release-Aufruf** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="20125-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="20125-113">Bis zum Senden der Benachrichtigung werden keine Änderungen im Nachrichtenspeicher angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20125-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="20125-114">Sie können Benachrichtigungen von einer Informationsquelle erhalten, nachdem Sie **Unadvise** zum Abbrechen einer Registrierung aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="20125-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="20125-115">Stellen Sie sicher, dass Sie ihre Ratensenke erst los lassen, nachdem die Referenzanzahl auf Null gefallen ist, und nicht nach einem erfolgreichen **Unadvise-Aufruf.**</span><span class="sxs-lookup"><span data-stu-id="20125-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="20125-116">Gehen Sie nicht davon aus, dass die Ratensenke nicht mehr erforderlich ist, da Sie **Unadvise** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="20125-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

