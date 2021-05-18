---
title: Aufrufen von MAPI von Windows Diensten
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
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="836f9-103">Aufrufen von MAPI von Windows Diensten</span><span class="sxs-lookup"><span data-stu-id="836f9-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="836f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="836f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="836f9-105">Um mapi-client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span><span class="sxs-lookup"><span data-stu-id="836f9-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="836f9-106">FÜR MAPI-Clients gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="836f9-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="836f9-107">Sie können keine Benutzeroberfläche zulassen.</span><span class="sxs-lookup"><span data-stu-id="836f9-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="836f9-108">Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transportanbieter senden.</span><span class="sxs-lookup"><span data-stu-id="836f9-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="836f9-109">Darüber hinaus können MAPI-Clients Nachrichten nur mithilfe des Microsoft Exchange Server oder eines anderen serverbasierten Transportanbieters senden und empfangen.</span><span class="sxs-lookup"><span data-stu-id="836f9-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="836f9-110">Aufgrund von Identitäts- und Sicherheitsproblemen zwischen Clientanwendungen und dem MAPI-Spooler werden die meisten Transportanbieter in einem Dienst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="836f9-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="836f9-111">Alle MAPI-Clientanwendungen, unabhängig davon, ob sie als Windows implementiert werden, müssen die [MAPIInitialize-Funktion](mapiinitialize.md) aufrufen, um die MAPI-Bibliotheken zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="836f9-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="836f9-112">Ein Aufruf der [OleInitialize-Funktion](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) ist auch erforderlich, um die OLE-Bibliotheken zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="836f9-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="836f9-113">Sowohl [MAPIInitialize](mapiinitialize.md) als auch [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) rufen die [CoInitialize-Funktion](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) auf, um die COM-Bibliotheken (Component Object Model) zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="836f9-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="836f9-114">Clients, die Dienste sind, müssen ein spezielles Flag MAPI_NT_SERVICE im **ulFlags-Element** der [MAPIINIT_0-Struktur](mapiinit_0.md) festlegen, das an [MAPIInitialize](mapiinitialize.md) und den  _ulFlags-Parameter_ übergeben wird, der an die [MAPILogonEx-Funktion](mapilogonex.md) übergeben wird, um MAPI über die spezielle Implementierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="836f9-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="836f9-115">MAPI-Clients, die als Windows geschrieben und mit der MAPI-Clientschnittstelle geschrieben werden, haben eine zusätzliche Anforderung.</span><span class="sxs-lookup"><span data-stu-id="836f9-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="836f9-116">Sie müssen das MAPI_NO_MAIL im Aufruf von [MAPILogonEx festlegen.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="836f9-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="836f9-117">Andere Typen von Clients müssen kein Kennzeichen für die Anmeldung festlegen, da es automatisch von MAPI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="836f9-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="836f9-118">Um Nachrichten in einem Initialisierungsthread zu verarbeiten, führt ein als Dienst implementierter MAPI-Client die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="836f9-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="836f9-119">Ruft die [MsgWaitForMultipleObjects-Funktion auf,](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) wenn der Hauptthread blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="836f9-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="836f9-120">Ruft die [GetMessage-,](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [TranslateMessage-](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)und [DispatchMessage-Sequenz](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) von Windows-Funktionen auf, um die Nachricht zu behandeln, wenn [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) die Summe des Werts des _Parameters nCount_ und den Wert von **WAIT_OBJECT_0** zurückgibt, der angibt, dass sich eine Nachricht in der Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="836f9-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="836f9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="836f9-121">See also</span></span>



[<span data-ttu-id="836f9-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="836f9-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="836f9-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="836f9-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="836f9-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="836f9-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="836f9-125">Probleme mit der Betriebsumgebung</span><span class="sxs-lookup"><span data-stu-id="836f9-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

