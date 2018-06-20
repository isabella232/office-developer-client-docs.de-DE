---
title: Threading in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795728"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="1c8d2-103">Threading in MAPI</span><span class="sxs-lookup"><span data-stu-id="1c8d2-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="1c8d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c8d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c8d2-105">Ein Thread ist die grundlegende Entität, die ein Betriebssystem CPU-Zeit zuweist.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="1c8d2-106">Ein Thread verfügt über eine eigene Register, Stack, Priorität und Speicher, aber eine Adresse Speicherplatz und Verarbeiten von Ressourcen wie Zugriffstoken gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="1c8d2-107">Threads freigeben Arbeitsspeicher, auch mit einem Thread lesen, was ein anderer Thread geschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="1c8d2-108">MAPI-Clients verwenden Sie die folgenden generischen threading Modelle.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="1c8d2-109">**Threading-Modell**</span><span class="sxs-lookup"><span data-stu-id="1c8d2-109">**Threading model**</span></span>|<span data-ttu-id="1c8d2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c8d2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c8d2-111">Einzelne Threadingmodells</span><span class="sxs-lookup"><span data-stu-id="1c8d2-111">Single threading model</span></span>  <br/> |<span data-ttu-id="1c8d2-112">Alle Objekte werden in den einzelnen Thread verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="1c8d2-113">Des Apartmentthreading Threadingmodells</span><span class="sxs-lookup"><span data-stu-id="1c8d2-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="1c8d2-114">Ein Objekt kann nur in dem Thread verwendet werden, die sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="1c8d2-115">Free-threading, oder der Thread-Modell</span><span class="sxs-lookup"><span data-stu-id="1c8d2-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="1c8d2-116">Ein Objekt kann auf einem beliebigen Thread verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="1c8d2-117">MAPI verwendet das kostenlose Threadingmodell unterstützenden threadsicheren Objekten, die auf einem beliebigen Thread können Sie jederzeit verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="1c8d2-118">OLE verwendet die Apartmentthreading-Modells.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="1c8d2-119">Das Threadingmodell des Apartmentthreading unterstützt-Objekten, die bei ein Thread als diejenige, die das Objekt erstellt verwenden dieses Objekt muss explizit übertragen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="1c8d2-120">Der Mechanismus, den OLE verwendet, um Objekte von einem Thread in eine andere zu übertragen wird als Marshallen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="1c8d2-121">Das Marshallen beinhaltet ein Stubobjekt und ein Proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="1c8d2-122">Diese spezielle Objekte Packen Sie die Parameter der Schnittstelle im Objekt gemarshallt werden, diese Parameter an den anderen Thread übertragen und Entpacken sie nach dem eintreffen.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="1c8d2-123">Konflikt zwischen den beiden Multithread-Modellen tritt auf, wenn ein-threading MAPI-Objekt an einen anderen Prozess, die mit OLE "lightweight" Remote Procedure Call oder LRPC gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="1c8d2-124">LRPC Semantik des Objekts von free-threading zu Apartmentthreading durch interposing Stub und des Proxys Schnittstellen mit Apartmentthreading-Verhalten zwischen dem Objekt und seine Aufrufer geändert.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="1c8d2-125">Zur Förderung des Bekanntheitsgrads der Situationen in MAPI, die zu dieser Konflikt führen kann Clients und Dienstanbieter können Probleme.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="1c8d2-126">Ein MAPI-Objekt kann zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="1c8d2-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="1c8d2-127">Über direkte Aufrufe von dessen eine Schnittstelle mit Methoden verknüpft von einem Dienstanbieter oder MAPI zurückgegebene Zeiger an den Client-Prozess wie das Sitzungsobjekt von [MAPILogonEx](mapilogonex.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="1c8d2-128">Unter Verwendung eines Schnittstelle Zeigers zurückgegeben, die für alle Dienstanbieter, wie etwa das Folder-Objekt kopiert über indirekte Aufrufe der Methoden aus einem anderen Ordner im [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)haben.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="1c8d2-129">Über eine Callback-Funktion wie die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode übergebenen mit einem Dienstanbieter oder MAPI einen **Advise** -Anruf oder die Methoden, die auf einer langen Operation Fortschritt anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="1c8d2-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

