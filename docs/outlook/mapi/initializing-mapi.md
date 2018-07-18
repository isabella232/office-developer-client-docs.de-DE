---
title: Initialisieren von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792710"
---
# <a name="initializing-mapi"></a><span data-ttu-id="c14ff-103">Initialisieren von MAPI</span><span class="sxs-lookup"><span data-stu-id="c14ff-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="c14ff-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c14ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c14ff-105">Alle Clientanwendungen, die MAPI-Bibliotheken verwenden, müssen die Funktion **"MAPIInitialize"** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="c14ff-106">Weitere Informationen finden Sie unter ["MAPIInitialize"](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="c14ff-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="c14ff-107">**"MAPIInitialize"** globale Daten für die Sitzung initialisiert und bereitet die MAPI-Bibliotheken, die Anrufe annehmen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="c14ff-108">Es gibt einige Flags, die die festzulegenden in manchen Fällen eine wichtige Rolle spielen:</span><span class="sxs-lookup"><span data-stu-id="c14ff-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="c14ff-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="c14ff-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="c14ff-110">Festlegen Sie MAPI_NT_SERVICE das Flag, ob Ihre Clients als Windows-Dienst implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c14ff-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="c14ff-111">Wenn Ihr Client ein Windows-Dienst ist und nicht dieses Flag festlegen, wird Sie von MAPI nicht als Dienst erkannt.</span><span class="sxs-lookup"><span data-stu-id="c14ff-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="c14ff-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="c14ff-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="c14ff-113">Das Flag MAPI_MULTITHREAD_NOTIFICATIONS bezieht sich auf wie MAPI Benachrichtigungen verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c14ff-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="c14ff-114">MAPI erstellt ein ausgeblendetes Fenster, das Fenster-Nachrichten empfängt beim Auftreten von Änderungen auf ein Objekt Benachrichtigungen generieren.</span><span class="sxs-lookup"><span data-stu-id="c14ff-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="c14ff-115">Die Fensternachrichten werden zu einem bestimmten Zeitpunkt, verursacht die Benachrichtigungen gesendet werden und die entsprechenden [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Methoden aufgerufen werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c14ff-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="c14ff-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="c14ff-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="c14ff-117">Das Flag MAPI_NO_COINT so festgelegt, dass **"MAPIInitialize"** nicht versucht, mit einem Aufruf von [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx)COM initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c14ff-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx).</span></span> <span data-ttu-id="c14ff-118">Wenn eine **MAPIINIT_0** -Struktur mit _UlFlags_ auf MAPI_NO_COINIT festgelegt in **"MAPIInitialize"** übergeben wird, wird MAPI wird vorausgesetzt, dass COM bereits initialisiert wurde, und den Aufruf von **CoInitialize**umgehen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="c14ff-119">Wenn MAPI_MULTITHREAD_NOTIFICATIONS Flag nicht übergeben wird, MAPI erstellt das Benachrichtigung Thread, der verwendet wurde, für den ersten Aufruf **"MAPIInitialize"** .</span><span class="sxs-lookup"><span data-stu-id="c14ff-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="c14ff-120">MAPI wird das Benachrichtigungsfenster in einem getrennten Thread erstellt, wenn MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread dedizierte zum Behandeln von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="c14ff-121">MAPI erwartet, dass den Thread, der zum Erstellen des Fensters ausgeblendete Benachrichtigung zu verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="c14ff-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="c14ff-122">Haben Sie eine Nachrichtenschleife.</span><span class="sxs-lookup"><span data-stu-id="c14ff-122">Have a message loop.</span></span>
    
- <span data-ttu-id="c14ff-123">Bleiben Sie während der Lebensdauer der Sitzung freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c14ff-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="c14ff-124">Haben Sie eine längere Lebensdauer als ein anderer Thread vom Client erstellt.</span><span class="sxs-lookup"><span data-stu-id="c14ff-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="c14ff-125">Sie können auswählen, welcher Thread verwendet wird, indem ein Flag in der erste Aufruf **"MAPIInitialize"** .</span><span class="sxs-lookup"><span data-stu-id="c14ff-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="c14ff-126">Die Gefahr zulassen eine der Threads, die Benachrichtigungen zu behandeln ist, die, wenn der Thread ausgeblendet wird, das Benachrichtigungsfenster gelöscht wird und Benachrichtigungen nicht mehr an eines Ihrer anderen Threads gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c14ff-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="c14ff-127">Spezielle Verarbeitung Bedarf auch, steuern den Versand der Benachrichtigung, die an das ausgeblendete Fenster Nachrichtenwarteschlange veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="c14ff-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="c14ff-128">Wenn Sie ein separates Fenster zum Behandeln von Benachrichtigungen verwenden, sicher, dass zum entsprechenden Zeitpunkt in einem entsprechenden Thread Benachrichtigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c14ff-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="c14ff-129">Sie benötigen keine speziellen Code zum Suchen und Verarbeiten der Windows-Nachrichten, die in der Benachrichtigungsfenster bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c14ff-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="c14ff-130">MAPI empfiehlt, dass die folgenden Arten von Clientanwendungen einen getrennten Thread verwenden, um das ausgeblendete Fenster für die Unterstützung der Benachrichtigung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="c14ff-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="c14ff-131">Alle Multithread-Clients.</span><span class="sxs-lookup"><span data-stu-id="c14ff-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="c14ff-132">Single-Threading Windows-Dienste und Win32-Konsole Applications.</span><span class="sxs-lookup"><span data-stu-id="c14ff-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="c14ff-133">Single-Thread-Clients, die nicht ihrer Hauptthread für die Benachrichtigung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="c14ff-134">Rufen Sie für die Verwendung den getrennten Thread Ansatz **"MAPIInitialize"** in jeder Thread, der das MAPI_MULTITHREAD_NOTIFICATIONS-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c14ff-135">Nur ein Client erste Aufruf von **"MAPIInitialize"** bewirkt, dass ein ausgeblendetes Fenster erstellt werden soll, um Benachrichtigungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c14ff-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="c14ff-136">Nachfolgende Aufrufe der einzige Ursache ein Referenzzähler erhöht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c14ff-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

