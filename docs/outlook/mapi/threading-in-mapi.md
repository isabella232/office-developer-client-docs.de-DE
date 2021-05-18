---
title: Threading in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405541"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="0636d-103">Threading in MAPI</span><span class="sxs-lookup"><span data-stu-id="0636d-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="0636d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0636d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0636d-105">Ein Thread ist die grundlegende Entität, der ein Betriebssystem CPU-Zeit zurteilung.</span><span class="sxs-lookup"><span data-stu-id="0636d-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="0636d-106">Ein Thread verfügt über eigene Register, Stapel, Priorität und Speicher, teilt sich jedoch einen Adressraum und Prozessressourcen wie Zugriffstoken.</span><span class="sxs-lookup"><span data-stu-id="0636d-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="0636d-107">Threads teilen auch Arbeitsspeicher, und ein Thread liest, was ein anderer Thread geschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="0636d-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="0636d-108">MAPI-Clients verwenden die folgenden generischen Threadingmodelle.</span><span class="sxs-lookup"><span data-stu-id="0636d-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="0636d-109">**Threadmodell**</span><span class="sxs-lookup"><span data-stu-id="0636d-109">**Threading model**</span></span>|<span data-ttu-id="0636d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0636d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0636d-111">Einzelnes Threadmodell</span><span class="sxs-lookup"><span data-stu-id="0636d-111">Single threading model</span></span>  <br/> |<span data-ttu-id="0636d-112">Alle Objekte werden im einzelnen Thread verwendet.</span><span class="sxs-lookup"><span data-stu-id="0636d-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="0636d-113">Apartmentthreadingmodell</span><span class="sxs-lookup"><span data-stu-id="0636d-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="0636d-114">Ein Objekt kann nur für den Thread verwendet werden, von dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0636d-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="0636d-115">Kostenloses Threading oder Threadpartmodell</span><span class="sxs-lookup"><span data-stu-id="0636d-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="0636d-116">Ein Objekt kann für jeden Thread verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0636d-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="0636d-117">MAPI verwendet das kostenlose Threadingmodell, das threadsichere Objekte unterstützt, die jederzeit in jedem Thread verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0636d-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="0636d-118">OLE verwendet das Apartmentthreadmodell.</span><span class="sxs-lookup"><span data-stu-id="0636d-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="0636d-119">Das Apartmentthreadmodell unterstützt Objekte, die explizit übertragen werden müssen, wenn ein anderer Thread als der, der das Objekt erstellt hat, dieses Objekt verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="0636d-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="0636d-120">Der Mechanismus, den OLE zum Übertragen von Objekten von einem Thread in einen anderen verwendet, wird als Marshalling bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0636d-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="0636d-121">Das Marshalling umfasst ein Stubobjekt und ein Proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="0636d-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="0636d-122">Diese speziellen Objekte verpacken die Parameter der Schnittstelle im Zu marshallenden Objekt, übertragen diese Parameter an den anderen Thread und packen sie bei der Ankunft aus.</span><span class="sxs-lookup"><span data-stu-id="0636d-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="0636d-123">Konflikt zwischen den beiden Multithreadmodellen tritt auf, wenn ein freithreading-MAPI-Objekt mithilfe von OLE "lightweight" Remote Procedure Call oder EINEMFN an einen anderen Prozess gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0636d-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="0636d-124">DURCH DIE ARBEIT WIRD die Semantik des Objekts vom freien Threading zum Apartmentthreading geändert, indem Stub- und Proxyschnittstellen mit dem Verhalten des Apartmentthreads zwischen dem Objekt und dem Aufrufer interposiert werden.</span><span class="sxs-lookup"><span data-stu-id="0636d-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="0636d-125">Das Bewusstsein für die Situationen in MAPI, die zu diesem Konflikt führen, kann Clients und Dienstanbietern helfen, Probleme zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0636d-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="0636d-126">Auf ein MAPI-Objekt kann zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="0636d-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="0636d-127">Durch direkte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem Dienstanbieter oder mapI zurückgegeben wird, der mit dem Clientprozess verknüpft ist, z. B. das sitzungsobjekt, das von [MAPILogonEx](mapilogonex.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0636d-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="0636d-128">Durch indirekte Aufrufe seiner Methoden mithilfe eines von einem beliebigen Dienstanbieter zurückgegebenen Schnittstellenzeigers, z. B. des ordnerobjekts, das aus einem anderen Ordner in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0636d-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="0636d-129">Über eine Rückruffunktion, z. B. die [ANAPIAdviseSink::OnNotify-Methode,](imapiadvisesink-onnotify.md) die an einen Dienstanbieter oder mapI in einem **Advise-Aufruf** übergeben wird, oder die Methoden, die den Fortschritt eines langwierigen Vorgangs anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="0636d-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

