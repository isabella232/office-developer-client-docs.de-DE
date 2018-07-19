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
ms.openlocfilehash: fdd66e4a27209e6b80757bcf52408eb0cea43794
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791806"
---
# <a name="handling-notifications"></a><span data-ttu-id="63fb3-103">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="63fb3-103">Handling notifications</span></span>

<span data-ttu-id="63fb3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63fb3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63fb3-105">Benachrichtigungen aktivieren, ein Objekt zu einem anderen zu informieren, dass es eine Änderung unterzogen wurde-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63fb3-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="63fb3-106">Die Art der Änderung wird als ein Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="63fb3-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="63fb3-107">MAPI definiert mehrere Ereignisse, die für die Benachrichtigung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="63fb3-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="63fb3-108">Clients registrieren Sie sich in der Regel für eine oder mehrere Ereignisse mit einem oder mehreren Objekten.</span><span class="sxs-lookup"><span data-stu-id="63fb3-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="63fb3-109">Diese Objekte werden als bezeichnet advise-Quellen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="63fb3-110">Objekte, die act can as advise-Quellen sind das Session-Objekt unter des MAPI-Steuerelement oder ein Objekt von einem Dienstanbieter, wie eine Nachricht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="63fb3-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="63fb3-111">Das informierte-Objekt genannt der Advise-Empfänger enthält, entweder eine Implementierung von der [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle oder die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und ist innerhalb von einer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="63fb3-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="63fb3-112">Advise-Source-Objekten Implementieren einer **Advise** -Methode, die von Clients für Benachrichtigungen registriert aufgerufen wird, und eine **Unadvise** -Methode, die aufgerufen wird, um eine Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="63fb3-113">Einer der Parameter zu **Advise** ist ein Zeiger auf eine Implementierung der **IMAPIAdviseSink** oder ** IMAPIViewAdviseSink **.</span><span class="sxs-lookup"><span data-stu-id="63fb3-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or ** IMAPIViewAdviseSink **.</span></span> <span data-ttu-id="63fb3-114">Die Quelle der Advise speichert diese Zeiger, damit sie aufrufen kann [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** bei einer Änderung wird.</span><span class="sxs-lookup"><span data-stu-id="63fb3-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="63fb3-115">Da Benutzern das Anzeigen der aktuellsten Informationen empfangen von Benachrichtigungen ermöglicht werden, wird empfohlen, dass alle Clients für registrieren und Behandeln von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="63fb3-116">Es ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="63fb3-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="63fb3-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="63fb3-117">In this section</span></span>

- <span data-ttu-id="63fb3-118">[Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie einen Client für Benachrichtigungen als Teil der Initialisierungsprozess zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="63fb3-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="63fb3-119">[Stornieren einer Benachrichtigungs](canceling-a-notification.md): Beschreibt, wie Sie ein Abonnement für eine Benachrichtigung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="63fb3-120">[Benachrichtigung bei Nachrichten speichern behandeln](handling-message-store-notification.md): Beschreibt, wie für Benachrichtigungen über Textnachrichten Store registrieren.</span><span class="sxs-lookup"><span data-stu-id="63fb3-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="63fb3-121">[Zuzuteilen Address Book Benachrichtigung](handing-address-book-notification.md): Beschreibt, wie Sie für registrieren und Address Book Benachrichtigungen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="63fb3-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="63fb3-122">[Behandeln von Tabelle Benachrichtigung](handling-table-notification.md): Beschreibt, wie für Benachrichtigungen aus der Hierarchietabelle registrieren.</span><span class="sxs-lookup"><span data-stu-id="63fb3-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="63fb3-123">[Implementieren einer Advise-Empfängerobjekt](implementing-an-advise-sink-object.md): Implementieren einer Advise-Empfängerobjekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="63fb3-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="63fb3-124">[Eine Benachrichtigung Anzeigedauer](timing-a-notification.md): den Zeitpunkt der Benachrichtigung durch den Client von Dienstanbietern beschreibt.</span><span class="sxs-lookup"><span data-stu-id="63fb3-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="63fb3-125">[Sicherstellen, dass eine Benachrichtigung threadsicheren](ensuring-a-thread-safe-notification.md): Beschreibt, wie Sie threadsicheren Benachrichtigung mit MAPI sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="63fb3-126">[Erzwingen Sie eine Benachrichtigung](forcing-a-notification.md): Beschreibt, wie Sie eine Benachrichtigung in MAPI zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="63fb3-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

