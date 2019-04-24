---
title: Aufrufen von MAPI über Windows-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318105"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="b050f-103">Aufrufen von MAPI über Windows-Dienste</span><span class="sxs-lookup"><span data-stu-id="b050f-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="b050f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b050f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b050f-105">Um MAPI-Clientanwendungen zu aktivieren, die als Windows-Dienste für den Betrieb mit MAPI-kompatiblen Dienstanbietern geschrieben wurden, stellt MAPI mehrere Einschränkungen und Anforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="b050f-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="b050f-106">MAPI-Clients weisen die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="b050f-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="b050f-107">Eine Benutzeroberfläche kann nicht zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="b050f-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="b050f-108">Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transportanbieter senden.</span><span class="sxs-lookup"><span data-stu-id="b050f-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="b050f-109">Darüber hinaus können MAPI-Clients Nachrichten nur mithilfe des Microsoft Exchange-Servers oder eines anderen Server basierten Transportanbieters senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="b050f-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="b050f-110">Aufgrund von Identitäts-und Sicherheitsproblemen zwischen Clientanwendungen und dem MAPI-Spooler werden die meisten Transportanbieter in einem Dienst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b050f-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="b050f-111">Alle MAPI-Clientanwendungen, unabhängig davon, ob Sie als Windows-Dienste implementiert werden, müssen die [MAPIInitialize](mapiinitialize.md) -Funktion aufrufen, um die MAPI-Bibliotheken zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b050f-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="b050f-112">Ein Aufruf der [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) -Funktion ist auch erforderlich, um die OLE-Bibliotheken zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b050f-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="b050f-113">Sowohl [MAPIInitialize](mapiinitialize.md) als auch [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) führen Aufrufe der [](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) Funktion zum INITIALISIEREN der Component Object Model (com)-Bibliotheken aus.</span><span class="sxs-lookup"><span data-stu-id="b050f-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="b050f-114">Clients, die Dienste sind, müssen ein spezielles Flag, MAPI_NT_SERVICE, im **ulFlags** -Element der [MAPIINIT_0](mapiinit_0.md) -Struktur festlegen, das an [MAPIInitialize](mapiinitialize.md) und im _ulFlags_ -Parameter übergeben wird, der an die [MAPILogonEx](mapilogonex.md) übergeben wird. Funktion, um MAPI über Ihre spezielle Implementierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b050f-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="b050f-115">MAPI-Clients, die als Windows-Dienste geschrieben und mit der MAPI-Clientschnittstelle geschrieben wurden, haben eine zusätzliche Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b050f-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="b050f-116">Sie müssen das MAPI_NO_MAIL-Flag im Aufruf von [MAPILogonEx](mapilogonex.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="b050f-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="b050f-117">Andere Clienttypen müssen kein Flag für die Anmeldung festlegen, da es automatisch von MAPI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b050f-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="b050f-118">Um Nachrichten in einem Initialisierungsthread zu behandeln, führt ein MAPI-Client, der als Dienst implementiert wird, folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="b050f-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="b050f-119">Ruft die [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) -Funktion auf, wenn der Hauptthread blockiert.</span><span class="sxs-lookup"><span data-stu-id="b050f-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="b050f-120">Ruft die [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)-, [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)-und [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) -Sequenz von Windows-Funktionen auf, um die Nachricht zu behandeln, wenn [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) die Summe des Werts des _nCount_ -Parameters und des der Wert von **WAIT_OBJECT_0**, der angibt, dass sich eine Nachricht in der Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="b050f-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b050f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b050f-121">See also</span></span>



[<span data-ttu-id="b050f-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="b050f-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="b050f-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="b050f-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="b050f-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b050f-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="b050f-125">Probleme bei der Betriebsumgebung</span><span class="sxs-lookup"><span data-stu-id="b050f-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

