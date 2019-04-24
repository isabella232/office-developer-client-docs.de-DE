---
title: Initialisieren von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309730"
---
# <a name="initializing-mapi"></a><span data-ttu-id="e94c2-103">Initialisieren von MAPI</span><span class="sxs-lookup"><span data-stu-id="e94c2-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="e94c2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e94c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e94c2-105">Alle Clientanwendungen, die die MAPI-Bibliotheken verwenden, müssen die **MAPIInitialize** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e94c2-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="e94c2-106">Weitere Informationen finden Sie unter [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="e94c2-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="e94c2-107">**MAPIInitialize** initialisiert globale Daten für die Sitzung und bereitet die MAPI-Bibliotheken so vor, dass Sie Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="e94c2-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="e94c2-108">Es gibt einige Flags, die in einigen Situationen festgelegt werden müssen:</span><span class="sxs-lookup"><span data-stu-id="e94c2-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="e94c2-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e94c2-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="e94c2-110">Legen Sie das MAPI_NT_SERVICE-Flag fest, wenn Ihr Client als Windows-Dienst implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e94c2-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="e94c2-111">Wenn Ihr Client ein Windows-Dienst ist und Sie dieses Flag nicht festlegen, wird es von MAPI nicht als Dienst erkannt.</span><span class="sxs-lookup"><span data-stu-id="e94c2-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="e94c2-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="e94c2-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="e94c2-113">Das MAPI_MULTITHREAD_NOTIFICATIONS-Flag bezieht sich darauf, wie MAPI-Benachrichtigungen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e94c2-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="e94c2-114">MAPI erstellt ein ausgeblendetes Fenster, das Fenster Meldungen empfängt, wenn Änderungen an Objekten erfolgen, die Benachrichtigungen generieren.</span><span class="sxs-lookup"><span data-stu-id="e94c2-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="e94c2-115">Die Fenster Meldungen werden zu einem bestimmten Zeitpunkt verarbeitet, sodass die Benachrichtigungen gesendet werden und die entsprechenden [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e94c2-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="e94c2-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="e94c2-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="e94c2-117">Legen Sie das MAPI_NO_COINT-Flag fest, sodass **MAPIInitialize** nicht versucht, com mit einem Aufruf [](https://msdn.microsoft.com/library/ms886303.aspx)von "Initialize" zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e94c2-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="e94c2-118">Wenn eine **MAPIINIT_0** -Struktur an **MAPIInitialize** übergeben wird, wobei _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, wird von MAPI davon ausgegangen, dass com bereits INITIALISIERT wurde und den Aufruf von "diinitialize" umgehen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e94c2-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="e94c2-119">Wenn das MAPI_MULTITHREAD_NOTIFICATIONS-Flag nicht übergeben wird, erstellt MAPI das Benachrichtigungsfenster für den Thread, der für Ihren ersten **MAPIInitialize** -Aufruf verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e94c2-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="e94c2-120">MAPI erstellt das Benachrichtigungsfenster in einem separaten Thread, wenn MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread, der für die Behandlung von Benachrichtigungen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="e94c2-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="e94c2-121">MAPI erwartet den Thread, der zum Erstellen des ausgeblendeten Benachrichtigungsfensters verwendet wird, für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e94c2-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="e94c2-122">Haben Sie eine Meldungsschleife.</span><span class="sxs-lookup"><span data-stu-id="e94c2-122">Have a message loop.</span></span>
    
- <span data-ttu-id="e94c2-123">Während der gesamten Lebensdauer der Sitzung nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="e94c2-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="e94c2-124">Sie haben eine längere Lebensdauer als alle anderen von Ihrem Client erstellten Threads.</span><span class="sxs-lookup"><span data-stu-id="e94c2-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="e94c2-125">Sie können auswählen, welcher Thread verwendet wird, indem Sie im ersten **MAPIInitialize** -Aufruf eine Kennzeichnung festlegen.</span><span class="sxs-lookup"><span data-stu-id="e94c2-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="e94c2-126">Die Gefahr, dass eines ihrer Threads die Benachrichtigungen verarbeitet, besteht darin, dass das Benachrichtigungsfenster zerstört wird und Benachrichtigungen nicht mehr an andere Threads gesendet werden können, wenn der Thread ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="e94c2-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="e94c2-127">Außerdem kann eine spezielle Verarbeitung erforderlich sein, um die Versendung der Benachrichtigungen zu steuern, die an die Nachrichtenwarteschlange des ausgeblendeten Fensters gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e94c2-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="e94c2-128">Wenn Sie ein separates Fenster zum Behandeln von Benachrichtigungen verwenden, müssen Sie sicherstellen, dass Benachrichtigungen zu einem geeigneten Zeitpunkt zu einem geeigneten Thread angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e94c2-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="e94c2-129">Sie benötigen keinen speziellen Code, um die im Benachrichtigungsfenster bereitgestellten Windows-Nachrichten zu überprüfen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e94c2-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="e94c2-130">MAPI empfiehlt, dass die folgenden Typen von Clientanwendungen einen separaten Thread verwenden, um das ausgeblendete Fenster für die Benachrichtigungsunterstützung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e94c2-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="e94c2-131">Alle Multithread-Clients.</span><span class="sxs-lookup"><span data-stu-id="e94c2-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="e94c2-132">Single threaded-Windows-Dienste und Win32-Konsolenanwendungen.</span><span class="sxs-lookup"><span data-stu-id="e94c2-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="e94c2-133">Single Thread-Clients, die ihren Hauptthread für die Benachrichtigung nicht verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="e94c2-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="e94c2-134">Wenn Sie den separaten Thread Ansatz verwenden möchten, rufen Sie **MAPIInitialize** für jeden Thread auf, und legen Sie das MAPI_MULTITHREAD_NOTIFICATIONS-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="e94c2-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e94c2-135">Nur der erste Aufruf des Clients an **MAPIInitialize** bewirkt, dass ein ausgeblendetes Fenster zur Unterstützung von Benachrichtigungen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e94c2-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="e94c2-136">Nachfolgende Aufrufe führen nur zu einer Erhöhung der Verweisanzahl.</span><span class="sxs-lookup"><span data-stu-id="e94c2-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

