---
title: Zeitliches steuern einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795729"
---
# <a name="timing-a-notification"></a><span data-ttu-id="32058-103">Zeitliches steuern einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="32058-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="32058-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="32058-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="32058-105">Da ereignisbenachrichtigung einen asynchronen Prozess ist, können Sie jederzeit nicht unbedingt benachrichtigt werden, unmittelbar nachdem das Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="32058-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="32058-106">Der Zeitpunkt der Aufrufe an die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode variiert je nach der Implementierung der Advise-Quelle Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="32058-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="32058-107">Dienstanbieter können Ihren Client entweder benachrichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="32058-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="32058-108">Gleichzeitig mit dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="32058-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="32058-109">Direkt nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="32058-109">Directly after the event.</span></span>
    
- <span data-ttu-id="32058-110">An einem später Punkt nach der Ereignis möglicherweise nach einem Aufruf **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="32058-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="32058-111">Die meisten Dienstanbieter Aufrufen **OnNotify** , nachdem die MAPI-Methode für das Ereignis verantwortliche an die aufrufende zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="32058-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="32058-112">Beispielsweise werden Benachrichtigungen für Nachrichten gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder die Nachricht nach dem Aufruf von **IUnknown** freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="32058-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="32058-113">Bis die Benachrichtigung gesendet wird, sind keine Änderungen im Nachrichtenspeicher sichtbar.</span><span class="sxs-lookup"><span data-stu-id="32058-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="32058-114">Sie können aus einer Datenquelle Advise Benachrichtigungen empfangen, nachdem Sie **Unadvise** um eine Registrierung abzubrechen aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="32058-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="32058-115">Achten Sie darauf, dass Ihre Advise-Empfänger Version erst nach seiner Referenzzähler auf 0 (null), nicht nach einem erfolgreichen Aufruf der **Unadvise** gefallen hat.</span><span class="sxs-lookup"><span data-stu-id="32058-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="32058-116">Gehen Sie nicht, da Sie **Unadvise** aufgerufen haben der Advise-Empfänger nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="32058-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

