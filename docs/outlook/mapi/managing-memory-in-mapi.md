---
title: Verwalten von Arbeitsspeicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5859d94f85ca3fe7a0c738ed596d3c1a11fb2e8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792916"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="d7049-103">Verwalten von Arbeitsspeicher in MAPI</span><span class="sxs-lookup"><span data-stu-id="d7049-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="d7049-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7049-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7049-105">Wissen, wie und wann zum Zuordnen und Freigeben von Arbeitsspeicher ist ein wichtiger Teil der Programmierung mit MAPI.</span><span class="sxs-lookup"><span data-stu-id="d7049-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="d7049-106">MAPI bietet sowohl Funktionen und Makros, mit denen der Client oder Dienstanbieter kann Speicher einheitlich zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d7049-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="d7049-107">Die drei Funktionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7049-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="d7049-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d7049-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d7049-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d7049-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d7049-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d7049-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="d7049-111">Wenn Clients und -Dienstanbieter verwenden Sie diese Funktionen, das Problem der "Eigentümer" – weiß, d. h., das Freigeben von – ein bestimmter Block des Speichers wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="d7049-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="d7049-112">Ein Client Aufrufen einer Service Provider-Methode muss einen Puffer groß genug für ein Rückgabewert beliebiger Größe nicht übergeben.</span><span class="sxs-lookup"><span data-stu-id="d7049-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="d7049-113">Der Dienstanbieter kann einfach die erforderliche Menge an Arbeitsspeicher mit **MAPIAllocateBuffer** zuweisen und, bei Bedarf **MAPIAllocateMore**und dem Client können später freigegeben werden soll Belieben **MAPIFreeBuffer**, unabhängig von dem Dienst verwenden Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d7049-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="d7049-114">Die Arbeitsspeicher-Makros werden verwendet, um die Strukturen oder Arrays von Strukturen mit einer bestimmten Größe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d7049-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="d7049-115">Clients und -Dienstanbieter sollten diese Makros verwenden, anstatt Speicher manuell.</span><span class="sxs-lookup"><span data-stu-id="d7049-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="d7049-116">Beispielsweise wenn ein Client namensauflösung Verarbeitung für eine Empfängerliste mit drei Einträge verarbeiten muss, kann das Makro **SizedADRLIST** verwendet werden so erstellen Sie eine **ADRLIST** -Struktur, mit der richtigen Anzahl an **IAddrBook::ResolveName** übergeben **ADRENTRY** Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="d7049-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="d7049-117">Alle Makros Speicher sind in der MAPIDEFS definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="d7049-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="d7049-118">Diese Makros sind:</span><span class="sxs-lookup"><span data-stu-id="d7049-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="d7049-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="d7049-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="d7049-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="d7049-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="d7049-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="d7049-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="d7049-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="d7049-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="d7049-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="d7049-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="d7049-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d7049-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="d7049-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="d7049-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="d7049-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d7049-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="d7049-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="d7049-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="d7049-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="d7049-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="d7049-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="d7049-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="d7049-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="d7049-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="d7049-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="d7049-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="d7049-132">MAPI unterstützt die Verwendung der COM-Schnittstelle [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) auch für die Speicherverwaltung.</span><span class="sxs-lookup"><span data-stu-id="d7049-132">MAPI also supports the use of the COM interface [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="d7049-133">-Dienstanbieter erhalten einen **IMalloc** -Schnittstelle auf MAPI bei der Initialisierung und können auch über die Funktion [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="d7049-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="d7049-134">Der wichtigste Vorteil für die Verwendung der **IMalloc** -Methoden zum Verwalten von Arbeitsspeicher über die MAPI-Funktionen besteht darin, dass mit den Methoden COM möglich, einen vorhandenen Puffer neu zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d7049-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="d7049-135">Neubelegung unterstützt die Funktionen des MAPI-Speicher nicht.</span><span class="sxs-lookup"><span data-stu-id="d7049-135">The MAPI memory functions do not support reallocation.</span></span> 
  

