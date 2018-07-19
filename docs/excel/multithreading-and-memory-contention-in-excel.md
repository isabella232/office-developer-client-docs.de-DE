---
title: Multithreading und Arbeitsspeicher Konflikte in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in excel, Arbeitsspeicher Konflikte in Excel, Funktionen [Excel 2007], threadsicheren, threadsicheren Funktionen [Excel 2007], lokalen Speicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790563"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="7184a-104">Multithreading und Arbeitsspeicher Konflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="7184a-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="7184a-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7184a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7184a-106">Microsoft Excel-Versionen verwenden als Excel 2007 einen einzelnen Thread für alle Arbeitsblatt Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="7184a-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="7184a-107">Jedoch kann ab Excel 2007, Excel konfiguriert werden von 1 1024 parallelen Threads für die Berechnung des Arbeitsblatts.</span><span class="sxs-lookup"><span data-stu-id="7184a-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="7184a-108">Auf einem Computer mit mehreren Prozessoren oder mehreren Prozessorkernen ist die Standardanzahl von Threads gleich der Anzahl der Prozessoren oder Kerne.</span><span class="sxs-lookup"><span data-stu-id="7184a-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="7184a-109">Aus diesem Grund können threadsicheren Zellen oder Zellen, die nur Funktionen enthalten, die Thread-Sicherheit, sind gleichzeitigen Threads, unterliegen der üblichen neuberechnung Logik, die nach ihrer Vorgängerzellen berechnet werden müssen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="7184a-110">Threadsicheren Funktionen</span><span class="sxs-lookup"><span data-stu-id="7184a-110">Thread-Safe Functions</span></span>

<span data-ttu-id="7184a-111">Die meisten integrierten Arbeitsblattfunktionen in Excel 2007 beginnende sind threadsicheren.</span><span class="sxs-lookup"><span data-stu-id="7184a-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="7184a-112">Sie können auch Schreiben und Registrieren von XLL-Funktionen als threadsicheren wird.</span><span class="sxs-lookup"><span data-stu-id="7184a-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="7184a-113">Excel verwendet einen Thread (den Hauptthread), um alle Befehle, Thread unsichere Funktionen, **XlAuto** -Funktionen (außer [XlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12**) und COM- und Visual Basic für Applikationen (VBA) Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7184a-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="7184a-114">In denen eine XLL-Funktion ein **XLOPER** oder **XLOPER12** mit **XlbitDLLFree** zurückgibt, verwendet Excel im gleichen Threads, auf dem der Funktionsaufruf erfolgte **XlAutoFree** oder **xlAutoFree12**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7184a-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="7184a-115">Die **XlAutoFree** oder **xlAutoFree12** wird vor der nächsten Funktionsaufruf auf diesem Thread aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7184a-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="7184a-116">Für Entwickler, XLL stehen Vorteile für das Erstellen von threadsicheren Funktionen:</span><span class="sxs-lookup"><span data-stu-id="7184a-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="7184a-117">Sie ermöglichen Excel auf einem Computer mit mehreren Prozessoren oder mehreren Prozessorkernen optimal.</span><span class="sxs-lookup"><span data-stu-id="7184a-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="7184a-118">Öffnen sie die Möglichkeit der Verwendung von Remoteservern wesentlich effizienter als erledigt werden können einen einzelnen Thread verwenden.</span><span class="sxs-lookup"><span data-stu-id="7184a-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="7184a-119">Angenommen Sie, Sie haben einen Computer mit einem Prozessor, der Verwendung, sagen, *N* Threads konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="7184a-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="7184a-120">Nehmen Sie an, dass eine Kalkulationstabelle ausgeführt wird, sendet der macht eine große Anzahl von Anrufen an eine XLL-Funktion, das wiederum eine Anforderung für Daten oder für eine Berechnung auf einem Remoteserver oder Cluster-Servern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="7184a-121">Unterliegen der Topologie Abhängigkeits-Gesamtstruktur konnte Excel die Funktion N Zeiten fast gleichzeitig anrufen.</span><span class="sxs-lookup"><span data-stu-id="7184a-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="7184a-122">Den oder die Server ausreichend fast oder parallel sind, die Neuberechnungszeit der Kalkulationstabelle konnte gesenkt werden soweit wie Faktor 1/N.</span><span class="sxs-lookup"><span data-stu-id="7184a-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="7184a-123">Das wichtige Problem beim Schreiben von threadsicheren Funktionen wird Konflikte bei Ressourcen ordnungsgemäß behandelt.</span><span class="sxs-lookup"><span data-stu-id="7184a-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="7184a-124">Bedeutet dies normalerweise Arbeitsspeicher Konflikte, und es kann in zwei Probleme unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="7184a-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="7184a-125">Wie Sie Speicher zu erstellen, die Sie kennen wird nur von diesem Thread verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="7184a-126">Wie Sie sicherstellen, dass gemeinsam genutzten Speicher sicher von mehreren Threads zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7184a-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="7184a-127">Als erstes kennen sollten, ist welchen Speicher in einer XLL von allen Threads zugegriffen werden kann und was nur vom derzeit ausgeführten Thread zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7184a-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="7184a-128">**Alle Threads zugreifen können**</span><span class="sxs-lookup"><span data-stu-id="7184a-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="7184a-129">Deklariert Variablen, Strukturen und Klasseninstanzen außerhalb des Textes, einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="7184a-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="7184a-130">Statische Variablen, die in den Textkörper einer Funktion deklariert.</span><span class="sxs-lookup"><span data-stu-id="7184a-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="7184a-131">In diesen beiden Fällen wird Arbeitsspeicher reserviert in der DLL Speicherblock erstellt für diese Instanz der DLL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7184a-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="7184a-132">Wenn eine andere Anwendungsinstanz geladen wird aus die DLL, ruft eine eigenen Kopie dieses Speichers, so, dass keine Konflikte bei dieser Ressourcen von außerhalb dieser Instanz der DLL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7184a-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="7184a-133">**Nur vom aktuellen Thread zugegriffen werden.**</span><span class="sxs-lookup"><span data-stu-id="7184a-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="7184a-134">Automatische Variablen Funktion-Codes (einschließlich Funktionsargumente).</span><span class="sxs-lookup"><span data-stu-id="7184a-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="7184a-135">In diesem Fall wird Arbeitsspeicher auf dem Stapel für jede Instanz des Funktionsaufrufs reserviert.</span><span class="sxs-lookup"><span data-stu-id="7184a-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7184a-136">Die dynamisch reservierter Speicher hängen von des Bereichs des Zeigers, das darauf zeigt: Wenn der Mauszeiger von allen Threads zugegriffen werden kann, ist auch der Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7184a-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="7184a-137">Wenn der Zeiger einer automatischen Variablen in einer Funktion ist, ist reservierte Speicher effektiv zu diesem Thread privat.</span><span class="sxs-lookup"><span data-stu-id="7184a-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="7184a-138">Arbeitsspeicher, die nur von einem Thread zugegriffen werden: Thread-Local-Speicher</span><span class="sxs-lookup"><span data-stu-id="7184a-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="7184a-139">Wenn die statische Variablen in den Textkörper einer Funktion von allen Threads zugegriffen werden kann, sind Funktionen, die sie verwenden deutlich nicht threadsicheren.</span><span class="sxs-lookup"><span data-stu-id="7184a-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="7184a-140">Eine Instanz der Funktion in einem Thread könnten den Wert ändern, während eine andere Instanz auf einem anderen Thread vorausgesetzt wird, dass sie eine vollständig andere ist.</span><span class="sxs-lookup"><span data-stu-id="7184a-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="7184a-141">Es gibt zwei Gründe für das Deklarieren statischer Variables in einer Funktion:</span><span class="sxs-lookup"><span data-stu-id="7184a-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="7184a-142">Statische Daten aus einen Anruf an das nächste beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="7184a-143">Ein Zeiger auf statische Daten kann problemlos von der Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7184a-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="7184a-144">Im Fall von erste Grund sollten Daten enthalten, die beibehalten und ist für alle Anrufe an die Funktion Bedeutung: vielleicht einen einfachen Indikator, der jedes Mal, wenn die Funktion für jeden Thread aufgerufen wird, oder eine Struktur, die Verwendung und Leistungsdaten Eve erfasst Ry Anruf.</span><span class="sxs-lookup"><span data-stu-id="7184a-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="7184a-145">Die Frage wird der freigegebene Daten oder die Datenstruktur schützen.</span><span class="sxs-lookup"><span data-stu-id="7184a-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="7184a-146">Dies geschieht am besten mithilfe von kritischen Abschnitt wie im nächste Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="7184a-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="7184a-147">Wenn die Daten nur für die Verwendung von diesem Thread die könnte die Groß-/Kleinschreibung Grund 1 und ist immer der Fall Grund 2 vorgesehen ist, ist die Frage wie Speicher zu erstellen, die weiterhin auftritt, aber kann nur von diesem Thread zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="7184a-148">Eine Lösung besteht darin, den lokalen Speicher (TLS) API verwenden.</span><span class="sxs-lookup"><span data-stu-id="7184a-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="7184a-149">Beispiel: haben Sie eine Funktion, die einen Zeiger auf eine **XLOPER**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7184a-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="7184a-150">Diese Funktion ist nicht threadsicheren, da ein Thread die statische **XLOPER12** zurückgeben kann, während sie einen anderen überschreibt.</span><span class="sxs-lookup"><span data-stu-id="7184a-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="7184a-151">Die Wahrscheinlichkeit hierfür ist noch größer, wenn die **XLOPER12** an **xlAutoFree12**übergeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="7184a-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="7184a-152">Eine Lösung besteht darin, eine **XLOPER12**zuweisen, einen Zeiger zu ihm zurückkehren und **xlAutoFree12** implementieren, sodass der **XLOPER12** Speicher selbst freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7184a-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="7184a-153">Dieser Ansatz ist in viele Funktionen Beispiel gezeigt in [Speicherverwaltung in Excel](memory-management-in-excel.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="7184a-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

<span data-ttu-id="7184a-154">Dieser Ansatz ist einfacher zu implementieren als die Vorgehensweise im nächsten Abschnitt werden die TLS-API verwendet, aber es einige Nachteile hat.</span><span class="sxs-lookup"><span data-stu-id="7184a-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="7184a-155">Excel müssen Sie zunächst **XlAutoFree**Aufrufen/ **xlAutoFree12** aufbauen, den Typ des der zurückgegebenen **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="7184a-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="7184a-156">Zweitens besteht ein Problem bei der Rückgabe **XLOPER**/ **XLOPER12**s, die den Rückgabewert eines Anrufs an eine C-API-Callback-Funktion sind.</span><span class="sxs-lookup"><span data-stu-id="7184a-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="7184a-157">Die **XLOPER**/ **XLOPER12** möglicherweise zeigen Sie auf Speicher, die durch Excel, aber die **XLOPER**freigegeben werden muss/ **XLOPER12** selbst freigegeben werden muss, auf die gleiche Weise er zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="7184a-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="7184a-158">Wenn eine solche ein **XLOPER**/ **XLOPER12** ist als den Rückgabewert eine XLL-Arbeitsblattfunktion verwendet werden soll, es ist keine einfache Möglichkeit, **XlAutoFree**informieren/ **xlAutoFree12** müssen beide Zeiger in geeigneter Weise frei.</span><span class="sxs-lookup"><span data-stu-id="7184a-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="7184a-159">(Festlegen von **XlbitXLFree** und **XlbitDLLFree** das Problem löst nicht die Behandlung von **XLOPER/XLOPER12s** in Excel mit festgelegt ist nicht definiert und möglicherweise ändern von Version zu Version.) Um dieses Problem zu umgehen, kann XLL tiefe Kopien alle Excel zugewiesenen **XLOPER/XLOPER12s** erstellen, die sie an das Arbeitsblatt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7184a-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="7184a-160">Eine Lösung, die diese Einschränkungen vermieden werden zu füllen und einer lokalen **XLOPER/XLOPER12**zurückzugeben, ein Ansatz, der diese **XlAutoFree/xlAutoFree12** erfordert gibt den **XLOPER/XLOPER12** Zeiger selbst nicht frei.</span><span class="sxs-lookup"><span data-stu-id="7184a-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

<span data-ttu-id="7184a-161">Die nächste Frage ist das Einrichten und Abrufen des Thread-Local-Speichers mit anderen Worten, wie im vorherigen Beispiel die Funktion **get_thread_local_xloper12** implementieren.</span><span class="sxs-lookup"><span data-stu-id="7184a-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="7184a-162">Dies erfolgt mithilfe der Thread lokalen Speicher (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="7184a-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="7184a-163">Der erste Schritt besteht darin erhalten einen Index TLS mithilfe von **TlsAlloc**, der letztlich mit **TlsFree**freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="7184a-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="7184a-164">Beide werden am besten aus **DllMain**durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7184a-164">Both are best accomplished from **DllMain**.</span></span>
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

<span data-ttu-id="7184a-165">Nachdem Sie den Index abgerufen haben, besteht der nächste Schritt für jeden Thread einen Block von Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="7184a-166">In der [Dokumentation zur Entwicklung von Windows](http://msdn.microsoft.com/de-de/library/ms682583%28VS.85%29.aspx) empfiehlt auf diese Weise jedes Mal, wenn die **DllMain** Callback-Funktion mit einem **DLL_THREAD_ATTACH** -Ereignis aufgerufen wird, und den Speicher bei jedem **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="7184a-166">The [Windows Development Documentation](http://msdn.microsoft.com/de-de/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="7184a-167">Jedoch würde diese Empfehlung folgen die DLL für nicht für die neuberechnung verwendeten Threads unnötige Arbeit leisten.</span><span class="sxs-lookup"><span data-stu-id="7184a-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="7184a-168">In diesem Fall ist es besser mithilfe eine Strategie für das zuordnen auf erste verwenden.</span><span class="sxs-lookup"><span data-stu-id="7184a-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="7184a-169">Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="7184a-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="7184a-170">Für den vorherigen Beispielen, die **XLOPERs** oder **XLOPER12s**zurückgeben, die folgenden reicht, aber Sie können eine beliebige Struktur, die Ihren Anforderungen erfüllt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7184a-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="7184a-171">Die folgende Funktion ruft einen Zeiger auf die Thread-Local-Instanz oder weist einen solchen ist dies der erste Aufruf.</span><span class="sxs-lookup"><span data-stu-id="7184a-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

<span data-ttu-id="7184a-172">Nun können Sie sehen, wie der Thread-Local **XLOPER/XLOPER12** Arbeitsspeicher abgerufen wird: zunächst rufen Sie einen Zeiger auf die Instanz des Threads von **TLS_data**, und klicken Sie dann geben Sie einen Zeiger auf die darin enthaltenen, wie folgt **XLOPER/XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="7184a-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

<span data-ttu-id="7184a-173">Die Funktionen **mtr_safe_example_1** und **mtr_safe_example_2** können als threadsicheren Arbeitsblattfunktionen registriert werden beim Ausführen von Excel.</span><span class="sxs-lookup"><span data-stu-id="7184a-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="7184a-174">Sie können nicht jedoch die beiden Methoden in einer XLL verwenden.</span><span class="sxs-lookup"><span data-stu-id="7184a-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="7184a-175">Ihre XLL kann nur eine Implementierung der **XlAutoFree** und **xlAutoFree12**exportieren, und jeder Strategie Arbeitsspeicher erfordert einen anderen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="7184a-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="7184a-176">Mit **mtr_safe_example_1**muss der Zeiger übergeben **XlAutoFree/xlAutoFree12** zusammen mit den Daten, die sie auf zeigt freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="7184a-177">Mit **mtr_safe_example_2**sollten nur die verweist auf Daten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="7184a-178">Windows bietet eine Funktion **GetCurrentThreadId**, die eindeutige systemweite-ID des aktuellen Threads zurückgibt</span><span class="sxs-lookup"><span data-stu-id="7184a-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="7184a-179">Dadurch wird den Entwickler mit einer anderen Methode, Code Thread sicher zu machen, oder einen Thread Verhalten bestimmter vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7184a-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="7184a-180">Arbeitsspeicher, die nur von mehreren Threads zugegriffen werden: kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="7184a-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="7184a-181">Sie sollten Lese-Schreib-Speicher schützen, die von mehreren Threads mithilfe von kritischen Abschnitten zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7184a-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="7184a-182">Für die einzelnen Einstellungen zum Blockieren des Speichers, den Sie schützen möchten, benötigen Sie einen benannten kritischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="7184a-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="7184a-183">Initialisieren diese während des Anrufs an die Funktion **XlAutoOpen** und freigegeben werden, und legen Sie diese während des Anrufs an die Funktion **XlAutoClose** auf einen Nullwert fest.</span><span class="sxs-lookup"><span data-stu-id="7184a-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="7184a-184">Sie müssen jedem Zugriff auf den geschützten Block innerhalb eines Paars von Anrufen an **EnterCriticalSection** und **LeaveCriticalSection**enthalten.</span><span class="sxs-lookup"><span data-stu-id="7184a-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="7184a-185">Nur ein Thread kann jederzeit in den kritischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="7184a-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="7184a-186">Es folgt ein Beispiel der Initialisierung, zur Aufhebung und Verwenden eines Abschnitts **G_csSharedTable**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7184a-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

<span data-ttu-id="7184a-187">Ein anderes, vielleicht sichererer Ansatz zum Schützen eines Blocks von Arbeitsspeicher ist eine Klasse erstellen, die eine eigene **CRITICAL_SECTION** und dessen Konstruktor, Destruktor enthält und Accessormethoden übernehmen, deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="7184a-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="7184a-188">Dieser Ansatz bietet den Vorteil, zum Schutz von Objekten, die initialisiert werden können, bevor **XlAutoOpen** ausgeführt wird oder nach dem **XlAutoClose** aufgerufen wird, aber Sie vorsichtig zum Erstellen von zu viele wichtige Abschnitte und das Betriebssystem Gemeinkosten, die dies erstellen würden.</span><span class="sxs-lookup"><span data-stu-id="7184a-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="7184a-189">Wenn Sie Code, die Zugriff auf mehr als ein Block mit geschütztem Speicher zur selben Zeit benötigt haben, müssen Sie die Reihenfolge sorgfältig zu prüfen, in der kritische Abschnitte eingegeben und beendet werden.</span><span class="sxs-lookup"><span data-stu-id="7184a-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="7184a-190">Beispielsweise könnte die folgenden beiden Funktionen einen Deadlock erstellen.</span><span class="sxs-lookup"><span data-stu-id="7184a-190">For example, the following two functions could create a deadlock.</span></span>
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="7184a-191">Wenn die erste Funktion in einem Thread **G_csSharedTableA** eingibt, während die zweite in einem anderen Thread **G_csSharedTableB**eingibt, hängen beide Threads.</span><span class="sxs-lookup"><span data-stu-id="7184a-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="7184a-192">Der richtige Ansatz ist in einer konsistenten Reihenfolge eingeben und wie folgt in umgekehrter Reihenfolge, beenden.</span><span class="sxs-lookup"><span data-stu-id="7184a-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="7184a-193">Sofern möglich, ist es besser aus einem Thread Zusammenarbeit Sicht zum Zugriff auf verschiedene Blöcke zu isolieren, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7184a-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="7184a-194">Besteht die Konkurrenz für eine freigegebene Ressource, wie häufige zugriffsanforderungen kurze, sollten Sie mit den kritischen Abschnitt Möglichkeit dreht.</span><span class="sxs-lookup"><span data-stu-id="7184a-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="7184a-195">Dies ist eine Technik gestaltet sich die Ressource weniger prozessorintensive warten.</span><span class="sxs-lookup"><span data-stu-id="7184a-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="7184a-196">Zu diesem Zweck können Sie entweder **InitializeCriticalSectionAndSpinCount** verwenden, bei der Initialisierung der Bereich oder das **SetCriticalSectionSpinCount** einmal zum Festlegen der Anzahl an, wie oft der Thread gewartet werden Ressourcen in einer Schleife initialisiert verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7184a-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="7184a-197">Der Wait-Vorgang ist teuer, sodass sich drehenden dies vermieden werden, wenn die Ressource in der Zwischenzeit freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7184a-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="7184a-198">Auf einem System Einzelprozessor die Anzahl der Drehfeld effektiv ignoriert, jedoch können Sie diese weiterhin ohne Schaden angeben.</span><span class="sxs-lookup"><span data-stu-id="7184a-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="7184a-199">Der Speicher Heap-Manager wird ein Drehfeld Count 4000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="7184a-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="7184a-200">Weitere Informationen zur Verwendung der wichtigen Abschnitte finden Sie unter Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7184a-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7184a-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7184a-201">See also</span></span>



[<span data-ttu-id="7184a-202">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="7184a-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="7184a-203">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="7184a-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="7184a-204">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7184a-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

