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
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344828"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="0f45f-103">Threading in MAPI</span><span class="sxs-lookup"><span data-stu-id="0f45f-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="0f45f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f45f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f45f-105">Ein Thread ist die grundlegende Entität, in die ein Betriebssystem CPU-Zeit zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0f45f-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="0f45f-106">Ein Thread verfügt über eigene Register, Stapel, Priorität und Speicher, hat jedoch einen Adressraum und verarbeitet Ressourcen wie Zugriffstoken.</span><span class="sxs-lookup"><span data-stu-id="0f45f-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="0f45f-107">Threads teilen auch Arbeitsspeicher, wobei ein Thread liest, was ein anderer Thread geschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="0f45f-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="0f45f-108">MAPI-Clients verwenden die folgenden generischen Threadingmodelle.</span><span class="sxs-lookup"><span data-stu-id="0f45f-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="0f45f-109">**Threadingmodell**</span><span class="sxs-lookup"><span data-stu-id="0f45f-109">**Threading model**</span></span>|<span data-ttu-id="0f45f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f45f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f45f-111">Single Threading-Modell</span><span class="sxs-lookup"><span data-stu-id="0f45f-111">Single threading model</span></span>  <br/> |<span data-ttu-id="0f45f-112">Alle Objekte werden im einzelnen Thread verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f45f-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="0f45f-113">Apartment-Threading-Modell</span><span class="sxs-lookup"><span data-stu-id="0f45f-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="0f45f-114">Ein Objekt kann nur für den Thread verwendet werden, der es erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="0f45f-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="0f45f-115">Freies Threading oder Thread-Party-Modell</span><span class="sxs-lookup"><span data-stu-id="0f45f-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="0f45f-116">Ein Objekt kann in einem beliebigen Thread verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f45f-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="0f45f-117">MAPI verwendet das ﻿kostenlose Threadingmodell und unterstützt threadsichere Objekte, die jederzeit in einem beliebigen Thread verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0f45f-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="0f45f-118">OLE verwendet das Apartment-Threadingmodell.</span><span class="sxs-lookup"><span data-stu-id="0f45f-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="0f45f-119">Das Apartment-Threading-Modell unterstützt Objekte, die explizit übergeben werden müssen, wenn ein anderer Thread als derjenige, der das Objekt erstellt hat, dieses Objekt verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="0f45f-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="0f45f-120">Der Mechanismus, den OLE zum Übertragen von Objekten von einem Thread zu einem anderen verwendet, wird als Marshalling bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0f45f-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="0f45f-121">Marshalling umfasst ein Stub-Objekt und ein Proxy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f45f-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="0f45f-122">Diese speziellen Objekte verpacken die Parameter der Schnittstelle im Objekt, das gemarshallt werden soll, übertragen diese Parameter in den anderen Thread und entpacken Sie bei der Ankunft.</span><span class="sxs-lookup"><span data-stu-id="0f45f-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="0f45f-123">Der Konflikt zwischen den beiden Multithread-Modellen ergibt sich, wenn ein MAPI-Objekt mit freiem Threading an einen anderen Prozess mithilfe von OLE "Lightweight"-Remote Prozeduraufruf oder LRPC gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f45f-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="0f45f-124">LRPC ändert die Semantik des Objekts vom freien Threading in den Apartmentthreading, indem Stub-und Proxy Schnittstellen mit dem Apartmentthreading-Verhalten zwischen dem Objekt und seinem Aufrufer zwischen den Objekten ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="0f45f-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="0f45f-125">Das Bewusstsein für die Situationen in MAPI, die zu diesem Konflikt führen, kann dazu beitragen, dass Clients und Dienstanbieter Probleme vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0f45f-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="0f45f-126">Auf ein MAPI-Objekt kann zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="0f45f-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="0f45f-127">Durch direkte Aufrufe seiner Methoden mithilfe eines Schnittstellenzeigers, der von einem Dienstanbieter oder einer mit dem Prozess des Clients verknüpften MAPI zurückgegeben wird, wie beispielsweise das von [MAPILogonEx](mapilogonex.md)zurückgegebene Sitzungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f45f-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="0f45f-128">Durch indirekte Aufrufe seiner Methoden mithilfe eines von einem beliebigen Dienstanbieter zurückgegebenen Schnittstellenzeigers, wie beispielsweise des Folder-Objekts, das aus einem anderen Ordner in [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md)kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0f45f-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="0f45f-129">Über eine Rückruffunktion, wie beispielsweise die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode, die an einen Dienstanbieter oder an MAPI in einem **Advise** -Aufruf übergeben wird, oder die Methoden, die den Fortschritt bei einem langwierigen Vorgang anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="0f45f-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

