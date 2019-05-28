---
title: Verwalten von Arbeitsspeicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298096"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="71848-103">Verwalten von Arbeitsspeicher in MAPI</span><span class="sxs-lookup"><span data-stu-id="71848-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="71848-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71848-105">Es ist ein wichtiger Teil der Programmierung mit MAPI zu wissen, wie und wann der Speicher reserviert und freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="71848-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="71848-106">MAPI stellt sowohl Funktionen als auch Makros bereit, die der Client oder Dienstanbieter zur konsistenten Verwaltung des Arbeitsspeichers verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="71848-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="71848-107">Die drei Funktionen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71848-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="71848-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="71848-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="71848-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="71848-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="71848-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="71848-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="71848-111">Wenn Clients und Dienstanbieter diese Funktionen verwenden, ist das Problem des "Besitzers", d. h., dass die Veröffentlichung eines bestimmten Speicherblocks verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="71848-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="71848-112">Ein Client, der eine Dienstanbieter Methode aufruft, muss keinen Puffer übergeben, der groß genug ist, um einen Rückgabewert beliebiger Größe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="71848-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="71848-113">Der Dienstanbieter kann einfach die entsprechende Menge an Arbeitsspeicher mithilfe von **MAPIAllocateBuffer** und, falls erforderlich, **MAPIAllocateMore**, und der Client kann ihn später unter Verwendung von **mapifreebufferfreigegeben**, unabhängig vom Dienst, frei geben. Anbieter.</span><span class="sxs-lookup"><span data-stu-id="71848-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="71848-114">Die Speicher Makros werden verwendet, um Strukturen oder Arrays von Strukturen mit einer bestimmten Größe zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="71848-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="71848-115">Clients und Dienstanbieter sollten diese Makros verwenden, anstatt den Arbeitsspeicher manuell zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="71848-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="71848-116">Wenn ein Client beispielsweise die Verarbeitung von Namensauflösung für eine Empfängerliste mit drei Einträgen durchführen muss, kann das **SizedADRLIST** -Makro verwendet werden, um eine **ADRLIST** -Struktur zu erstellen, die an **IAddrBook::** ResolveName mit der richtigen Anzahl von \*\*\*\* Mitglieder der Anmietung.</span><span class="sxs-lookup"><span data-stu-id="71848-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="71848-117">Alle Speicher Makros sind im MAPIDEFS definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="71848-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="71848-118">Diese Makros lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="71848-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="71848-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="71848-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="71848-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="71848-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="71848-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="71848-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="71848-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="71848-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="71848-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="71848-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="71848-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="71848-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="71848-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="71848-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="71848-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="71848-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="71848-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="71848-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="71848-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="71848-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="71848-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="71848-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="71848-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="71848-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="71848-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="71848-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="71848-132">MAPI unterstützt auch die Verwendung der com- [](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) Schnittstelle IMalloc für die Speicherverwaltung.</span><span class="sxs-lookup"><span data-stu-id="71848-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="71848-133">Dienstanbieter erhalten einen **IMalloc** -Schnittstellenzeiger von MAPI zur Initialisierungszeit und können auch einen über die [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="71848-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="71848-134">Der Hauptvorteil bei der Verwendung \*\*\*\* der IMalloc-Methoden für die Verwaltung von Arbeitsspeicher über die MAPI-Funktionen besteht darin, dass mit den com-Methoden ein vorhandener Puffer neu reserviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="71848-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="71848-135">Die MAPI-Speicherfunktionen unterstützen keine Neuzuordnung.</span><span class="sxs-lookup"><span data-stu-id="71848-135">The MAPI memory functions do not support reallocation.</span></span> 
  

