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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360396"
---
# <a name="timing-a-notification"></a><span data-ttu-id="ee6ca-103">Timing einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="ee6ca-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="ee6ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee6ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee6ca-105">Da es sich bei der Ereignisbenachrichtigung um einen asynchronen Prozess handelt, können Sie jederzeit benachrichtigt werden, nicht unbedingt unmittelbar nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="ee6ca-106">Der Zeitpunkt der Aufrufe Ihrer [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode variiert je nach dem Dienstanbieter, der die Advise-Quelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="ee6ca-107">Dienstanbieter können Ihren Client entweder Benachrichtigen:</span><span class="sxs-lookup"><span data-stu-id="ee6ca-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="ee6ca-108">Gleichzeitig mit dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="ee6ca-109">Direkt nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-109">Directly after the event.</span></span>
    
- <span data-ttu-id="ee6ca-110">Zu einem späteren Zeitpunkt nach dem Ereignis, möglicherweise \*\*\*\* nach einem Unadvise-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="ee6ca-111">Die meisten Dienstanbieter \*\*\*\* rufen OnNotify auf, nachdem die für das Ereignis zuständige MAPI-Methode an den Aufrufer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="ee6ca-112">Benachrichtigungen an Nachrichten werden beispielsweise gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) oder nach der Veröffentlichung der Nachricht nach dem Aufruf von **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="ee6ca-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="ee6ca-113">Bis zum Senden der Benachrichtigung sind keine Änderungen im Nachrichtenspeicher sichtbar.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="ee6ca-114">Sie können Benachrichtigungen von einer Advise-Quelle erhalten, nachdem Sie **Unadvise** aufgerufen haben, um eine Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="ee6ca-115">Stellen Sie sicher, dass Sie Ihre Advise-Senke erst freigeben, nachdem der Verweiszähler auf Null gesunken ist \*\*\*\* , nicht nach einem erfolgreichen Unadvise-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="ee6ca-116">Gehen Sie nicht davon aus, dass die \*\*\*\* Advise-Senke nicht mehr erforderlich ist, weil Sie Unadvise aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="ee6ca-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

