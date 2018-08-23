---
title: Aufrufen von MAPI-Anruf über Windows-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565865"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="54e24-103">Aufrufen von MAPI-Anruf über Windows-Dienste</span><span class="sxs-lookup"><span data-stu-id="54e24-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="54e24-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54e24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54e24-105">Um MAPI-Clientanwendungen zu aktivieren, die als Windows-Dienste für den Betrieb mit MAPI-kompatible Dienstanbieter geschrieben werden, erfordert MAPI verschiedene Einschränkungen und Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="54e24-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="54e24-106">MAPI-Clients bieten die folgenden Nachteile:</span><span class="sxs-lookup"><span data-stu-id="54e24-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="54e24-107">Sie können eine Benutzeroberfläche nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="54e24-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="54e24-108">Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transport Anbieter.</span><span class="sxs-lookup"><span data-stu-id="54e24-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="54e24-109">Darüber hinaus können MAPI-Clients senden und Empfangen von Nachrichten mithilfe von nur die Microsoft Exchange-Server oder einen anderen Server-basierten Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="54e24-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="54e24-110">Aufgrund des Identität und Sicherheit zwischen Clientanwendungen und die MAPI-Warteschlange sind die meisten Transportanbieter in einem Dienst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54e24-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="54e24-111">Alle MAPI-Clientanwendungen, ob sie als Windows-Dienste implementiert werden, müssen die Funktion ["MAPIInitialize"](mapiinitialize.md) zum Initialisieren der MAPI-Bibliotheken aufrufen.</span><span class="sxs-lookup"><span data-stu-id="54e24-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="54e24-112">Ein Aufruf der Funktion [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) ist auch erforderlich, die OLE-Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="54e24-112">A call to the [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="54e24-113">["MAPIInitialize"](mapiinitialize.md) und [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) tätigen von Anrufen an die Funktion [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) die Bibliotheken Component Object Model (COM) nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="54e24-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="54e24-114">Clients, die Dienste sind müssen ein spezielles Flag, MAPI_NT_SERVICE, legen Sie im **UlFlags** -Member der [MAPIINIT_0](mapiinit_0.md) -Struktur, die ["MAPIInitialize"](mapiinitialize.md) übergeben wird, und die _UlFlags_ -Parameter, der an die [MAPILogonEx](mapilogonex.md) übergeben wird Funktion, um die spezielle Implementierung MAPI zu informieren.</span><span class="sxs-lookup"><span data-stu-id="54e24-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="54e24-115">MAPI-Clients, die als Windows-Dienste und mit der MAPI-Client-Schnittstelle geschrieben werden müssen, eine zusätzliche Anforderung.</span><span class="sxs-lookup"><span data-stu-id="54e24-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="54e24-116">Sie müssen das Flag MAPI_NO_MAIL im Aufruf [MAPILogonEx](mapilogonex.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54e24-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="54e24-117">Andere Typen von Clients müssen kein Flag für die Anmeldung festgelegt werden, da er automatisch vom MAPI festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="54e24-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="54e24-118">Zur Verarbeitung von Nachrichten in einem Initialisierungsthread, führt ein MAPI-Client, der als Dienst implementiert wird Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="54e24-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="54e24-119">Ruft die [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) Funktion bei der Hauptthread blockiert.</span><span class="sxs-lookup"><span data-stu-id="54e24-119">Calls the [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="54e24-120">Ruft die [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)und [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) Abfolge der Windows-Funktionen in der Nachricht behandelt [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) die Summe der Wert des Parameters _nCount_ zurückgibt und die der Wert der **WAIT_OBJECT_0**, die angibt, dass eine Meldung in der Warteschlange ist.</span><span class="sxs-lookup"><span data-stu-id="54e24-120">Calls the [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54e24-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54e24-121">See also</span></span>



[<span data-ttu-id="54e24-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="54e24-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="54e24-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="54e24-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="54e24-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="54e24-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="54e24-125">Probleme in der Betriebssystemumgebung</span><span class="sxs-lookup"><span data-stu-id="54e24-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

