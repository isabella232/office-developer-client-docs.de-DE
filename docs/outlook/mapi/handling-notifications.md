---
title: Behandeln von Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299387"
---
# <a name="handling-notifications"></a><span data-ttu-id="79d67-103">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="79d67-103">Handling notifications</span></span>

<span data-ttu-id="79d67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79d67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79d67-105">Benachrichtigungen aktivieren Sie ein Objekt, um ein anderes Objekt zu informieren, dass eine Änderung durchlaufen wurde.</span><span class="sxs-lookup"><span data-stu-id="79d67-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="79d67-106">Der Typ der Änderung wird als Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="79d67-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="79d67-107">MAPI definiert mehrere Ereignisse, für die Benachrichtigungen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="79d67-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="79d67-108">Clients registrieren sich in der Regel für ein oder mehrere Ereignisse mit einem oder mehreren Objekten.</span><span class="sxs-lookup"><span data-stu-id="79d67-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="79d67-109">Diese Objekte werden als Advise sources bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="79d67-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="79d67-110">Zu den Objekten, die als Advise-Quellen fungieren können, gehört das Session-Objekt unter MAPIs Steuerelement oder ein von einem Dienstanbieter erstelltes Objekt wie eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="79d67-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="79d67-111">Das informierte Objekt, das als Advise-Senke bezeichnet wird, enthält entweder eine Implementierung der [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle oder die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und befindet sich innerhalb einer Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="79d67-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="79d67-112">Advise-Quellobjekte implementieren Sie eine **Advise** -Methode, die von Clients zum Registrieren von Benachrichtigungen aufgerufen wird, und eine Unadvise-Methode, die zum Abbrechen einer Registrierung aufgerufen wird. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="79d67-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="79d67-113">Einer der zu **Advise** -Parameter ist ein Zeiger auf eine Implementierung von **IMAPIAdviseSink** oder \* \* IMAPIViewAdviseSink \* \*.</span><span class="sxs-lookup"><span data-stu-id="79d67-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="79d67-114">Die Advise-Quelle speichert diesen Zeiger zwischen, sodass er [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** beim Auftreten einer Änderung aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="79d67-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="79d67-115">Da das Empfangen von Benachrichtigungen es Benutzern ermöglicht, die aktuellsten Informationen anzuzeigen, empfiehlt es sich, dass alle Clients Benachrichtigungen registrieren und behandeln.</span><span class="sxs-lookup"><span data-stu-id="79d67-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="79d67-116">Sie ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="79d67-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="79d67-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="79d67-117">In this section</span></span>

- <span data-ttu-id="79d67-118">[Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie Sie einen Client für Benachrichtigungen im Rahmen des Initialisierungsprozesses registrieren.</span><span class="sxs-lookup"><span data-stu-id="79d67-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="79d67-119">[Abbrechen einer Benachrichtigung](canceling-a-notification.md): Beschreibt, wie ein Abonnement für eine Benachrichtigung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="79d67-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="79d67-120">[Behandeln von Nachrichtenspeicher](handling-message-store-notification.md)Benachrichtigungen: Beschreibt, wie Sie sich für Nachrichtenspeicher Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="79d67-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="79d67-121">[Adressbuch Benachrichtigung](handing-address-book-notification.md): Beschreibt, wie Sie sich für Adressbuch Benachrichtigungen registrieren und behandeln.</span><span class="sxs-lookup"><span data-stu-id="79d67-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="79d67-122">[Behandlung von Tabellen Benachrichtigungen](handling-table-notification.md): Beschreibt, wie Sie sich in der Hierarchietabelle für Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="79d67-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="79d67-123">[Implementieren eines Advise](implementing-an-advise-sink-object.md)-Senke-Objekts: Beschreibt, wie ein Advise-Senke-Objekt implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="79d67-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="79d67-124">[Timing a Notification](timing-a-notification.md): Beschreibt den Zeitpunkt der Client Benachrichtigung durch Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="79d67-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="79d67-125">Sicherstellen [einer threadsicheren Benachrichtigung](ensuring-a-thread-safe-notification.md): Beschreibt, wie threadsichere Benachrichtigungen mit MAPI sichergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="79d67-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="79d67-126">[Erzwingen einer Benachrichtigung](forcing-a-notification.md): Beschreibt, wie eine Benachrichtigung in MAPI erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="79d67-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

