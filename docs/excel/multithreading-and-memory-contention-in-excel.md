---
title: Multithreading und Memory Contention in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in Excel, Arbeitsspeicher-Streit in Excel,Funktionen [Excel 2007], threadsichere, threadsichere Funktionen [Excel 2007],thread-lokaler Speicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301638"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="34908-104">Multithreading und Memory Contention in Excel</span><span class="sxs-lookup"><span data-stu-id="34908-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="34908-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="34908-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="34908-106">Versionen von Microsoft Excel vor Excel 2007 verwenden einen einzelnen Thread für alle Arbeitsblattberechnungen.</span><span class="sxs-lookup"><span data-stu-id="34908-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="34908-107">Ab Excel 2007 kann Excel für die Verwendung von 1 bis 1024 gleichzeitigen Threads für die Arbeitsblattberechnung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="34908-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="34908-108">Auf einem Computer mit mehreren Prozessoren oder mehreren Kernen entspricht die Standardanzahl von Threads der Anzahl der Prozessoren oder Kerne.</span><span class="sxs-lookup"><span data-stu-id="34908-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="34908-109">Daher können threadsichere Zellen oder Zellen, die nur threadsichere Funktionen enthalten, gleichzeitigen Threads zugewiesen werden, vorbehaltlich der üblichen Neuberechnungslogik, die nach ihren Vorgängern berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="34908-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="34908-110">Thread-Safe-Funktionen</span><span class="sxs-lookup"><span data-stu-id="34908-110">Thread-Safe Functions</span></span>

<span data-ttu-id="34908-111">Die meisten integrierten Arbeitsblattfunktionen ab Excel 2007 sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="34908-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="34908-112">Sie können auch XLL-Funktionen als threadsicher schreiben und registrieren.</span><span class="sxs-lookup"><span data-stu-id="34908-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="34908-113">Excel verwendet einen Thread (seinen Hauptthread), um alle Befehle, threadunsicheren Funktionen, **xlAuto-Funktionen** (außer [xlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12)** und COM- und Visual Basic for Applications (VBA)-Funktionen auf aufruft.</span><span class="sxs-lookup"><span data-stu-id="34908-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="34908-114">Wenn eine XLL-Funktion einen **XLOPER-** oder **XLOPER12-Wert** mit **xlbitDLLFree-Satz** zurückgibt, verwendet Excel denselben Thread, für den der Funktionsaufruf zum Aufrufen von **xlAutoFree** oder **xlAutoFree12** ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="34908-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="34908-115">Der Aufruf von **xlAutoFree** oder **xlAutoFree12** erfolgt vor dem nächsten Funktionsaufruf in diesem Thread.</span><span class="sxs-lookup"><span data-stu-id="34908-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="34908-116">Für XLL-Entwickler gibt es Vorteile für das Erstellen threadsicherer Funktionen:</span><span class="sxs-lookup"><span data-stu-id="34908-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="34908-117">Sie ermöglichen Excel, das Beste aus einem Multiprozessor- oder Multi-Core-Computer zu machen.</span><span class="sxs-lookup"><span data-stu-id="34908-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="34908-118">Sie eröffnen die Möglichkeit, Remoteserver viel effizienter zu verwenden, als dies mit einem einzigen Thread möglich ist.</span><span class="sxs-lookup"><span data-stu-id="34908-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="34908-119">Angenommen, Sie verfügen über einen Computer mit einem Prozessor, der für die Verwendung, z. B.  *N-Threads, konfiguriert*  wurde.</span><span class="sxs-lookup"><span data-stu-id="34908-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="34908-120">Angenommen, es wird eine Kalkulationstabelle ausgeführt, die eine große Anzahl von Aufrufen an eine XLL-Funktion sendet, die wiederum eine Anforderung für Daten oder eine Berechnung an einen Remoteserver oder Cluster von Servern sendet.</span><span class="sxs-lookup"><span data-stu-id="34908-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="34908-121">Abhängig von der Topologie der Abhängigkeitsstruktur Excel die Funktion fast zeitgleich aufrufen.</span><span class="sxs-lookup"><span data-stu-id="34908-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="34908-122">Vorausgesetzt, der Server oder die Server sind ausreichend schnell oder parallel, kann die Neuberechnungszeit der Tabelle um den Faktor 1/N reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="34908-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="34908-123">Das wichtigste Problem beim Schreiben von threadsicheren Funktionen ist die korrekte Behandlung von Ressourceninhalten.</span><span class="sxs-lookup"><span data-stu-id="34908-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="34908-124">Dies bedeutet in der Regel Speicher-Streit, und er kann in zwei Probleme aufgeschlüsselt werden:</span><span class="sxs-lookup"><span data-stu-id="34908-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="34908-125">So erstellen Sie Speicher, von dem Sie wissen, dass er nur von diesem Thread verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34908-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="34908-126">So stellen Sie sicher, dass auf freigegebenen Arbeitsspeicher von mehreren Threads sicher zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="34908-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="34908-127">Zunächst ist zu beachten, auf welchen Speicher in einer XLL alle Threads und nur der aktuell ausgeführte Thread zugriffen kann.</span><span class="sxs-lookup"><span data-stu-id="34908-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="34908-128">**Zugriff durch alle Threads**</span><span class="sxs-lookup"><span data-stu-id="34908-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="34908-129">Variablen, Strukturen und Klasseninstanzen, die außerhalb des Textkörpers einer Funktion deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="34908-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="34908-130">Statische Variablen, die innerhalb des Textkörpers einer Funktion deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="34908-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="34908-131">In diesen beiden Fällen wird der Arbeitsspeicher im Speicherblock der DLL, der für diese Instanz der DLL erstellt wurde, beiseite gelegt.</span><span class="sxs-lookup"><span data-stu-id="34908-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="34908-132">Wenn eine andere Anwendungsinstanz die DLL lädt, ruft sie eine eigene Kopie dieses Speichers ab, sodass es keinen Streit über diese Ressourcen außerhalb dieser Instanz der DLL gibt.</span><span class="sxs-lookup"><span data-stu-id="34908-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="34908-133">**Zugriff nur durch den aktuellen Thread**</span><span class="sxs-lookup"><span data-stu-id="34908-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="34908-134">Automatische Variablen im Funktionscode (einschließlich Funktionsargumenten).</span><span class="sxs-lookup"><span data-stu-id="34908-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="34908-135">In diesem Fall wird der Arbeitsspeicher auf dem Stapel für jede Instanz des Funktionsaufrufs beiseite gelegt.</span><span class="sxs-lookup"><span data-stu-id="34908-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="34908-136">Der Bereich des dynamisch zugewiesenen Arbeitsspeichers hängt vom Bereich des Zeigers ab, der darauf zeigt: Wenn auf den Zeiger von allen Threads zugegriffen werden kann, ist auch der Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34908-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="34908-137">Wenn es sich bei dem Zeiger um eine automatische Variable in einer Funktion handelt, ist der zugewiesene Arbeitsspeicher für diesen Thread praktisch privat.</span><span class="sxs-lookup"><span data-stu-id="34908-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="34908-138">Arbeitsspeicher, auf den nur ein Thread zugegriffen werden kann: Thread-Local Speicher</span><span class="sxs-lookup"><span data-stu-id="34908-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="34908-139">Da auf statische Variablen im Textkörper einer Funktion von allen Threads zugegriffen werden kann, sind Funktionen, die sie verwenden, eindeutig nicht threadsicher.</span><span class="sxs-lookup"><span data-stu-id="34908-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="34908-140">Eine Instanz der Funktion in einem Thread kann den Wert ändern, während eine andere Instanz in einem anderen Thread davon aus geht, dass es sich um etwas völlig anderes handelt.</span><span class="sxs-lookup"><span data-stu-id="34908-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="34908-141">Es gibt zwei Gründe für das Deklarieren statischer Variablen innerhalb einer Funktion:</span><span class="sxs-lookup"><span data-stu-id="34908-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="34908-142">Statische Daten werden von einem Aufruf zum nächsten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="34908-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="34908-143">Ein Zeiger auf statische Daten kann von der Funktion sicher zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34908-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="34908-144">Im ersten Fall möchten Sie möglicherweise Daten haben, die beibehalten werden und für alle Aufrufe der Funktion bedeutungslos sind: vielleicht ein einfacher Indikator, der jedes Mal erhöht wird, wenn die Funktion für einen Thread aufgerufen wird, oder eine Struktur, die Nutzungs- und Leistungsdaten für jeden Aufruf sammelt.</span><span class="sxs-lookup"><span data-stu-id="34908-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="34908-145">Die Frage ist, wie die freigegebenen Daten oder die Datenstruktur geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="34908-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="34908-146">Dies wird am besten mithilfe des kritischen Abschnitts durchgeführt, wie im nächsten Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="34908-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="34908-147">Wenn die Daten nur für die Verwendung durch diesen Thread vorgesehen sind, was aus Grund 1 der Fall sein kann und immer aus Grund 2 der Fall ist, stellt sich die Frage, wie Speicher erstellt wird, der beibehalten wird, aber nur über diesen Thread zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="34908-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="34908-148">Eine Lösung besteht in der Verwendung der Thread-Local Storage (TLS)-API.</span><span class="sxs-lookup"><span data-stu-id="34908-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="34908-149">Betrachten Sie beispielsweise eine Funktion, die einen Zeiger auf einen **XLOPER -Wert zurückgibt.**</span><span class="sxs-lookup"><span data-stu-id="34908-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="34908-150">Diese Funktion ist nicht threadsicher, da ein Thread die statische **XLOPER12** zurückgeben kann, während ein anderer sie überschreiben kann.</span><span class="sxs-lookup"><span data-stu-id="34908-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="34908-151">Die Wahrscheinlichkeit, dass dies geschieht, ist noch größer, wenn **xlOPER12** an **xlAutoFree12 übergeben werden muss.**</span><span class="sxs-lookup"><span data-stu-id="34908-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="34908-152">Eine Lösung besteht in der Zuweisung einer **XLOPER12,** der Rückgabe eines Zeigers und der Implementierung von **xlAutoFree12,** sodass der **XLOPER12-Speicher** selbst frei wird.</span><span class="sxs-lookup"><span data-stu-id="34908-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="34908-153">Dieser Ansatz wird in vielen beispielfunktionen in [Memory Management in Excel verwendet.](memory-management-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="34908-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="34908-154">Dieser Ansatz ist einfacher zu implementieren als der im nächsten Abschnitt beschriebene Ansatz, der auf der TLS-API basiert, hat jedoch einige Nachteile.</span><span class="sxs-lookup"><span data-stu-id="34908-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="34908-155">Zunächst muss Excel **xlAutoFree** xlAutoFree12 aufrufen, unabhängig vom Typ der /   zurückgegebenen **XLOPER** /  **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="34908-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="34908-156">Zweitens gibt es beim Zurückgeben von **XLOPER** XLOPER12 s ein Problem, das den Rückgabewert eines Aufrufs einer /  C-API-Rückruffunktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="34908-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12** s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="34908-157">**XlOPER** XLOPER12 kann auf Arbeitsspeicher verweisen, der von Excel frei werden muss, der /   **XLOPER** /  **XLOPER12** selbst muss jedoch auf die gleiche Weise frei werden, wie er zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="34908-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="34908-158">Wenn ein solcher **XLOPER** XLOPER12 als Rückgabewert einer XLL-Arbeitsblattfunktion verwendet werden soll, gibt es keine einfache Möglichkeit, /   **xlAutoFree** /  **xlAutoFree12** darüber zu informieren, dass beide Zeiger auf die entsprechende Weise frei gemacht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="34908-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="34908-159">(Das Festlegen von **xlbitXLFree** und **xlbitDLLFree** löst das Problem nicht, da die Behandlung von **XLOPER/XLOPER12s** in Excel mit beiden Satz nicht definiert ist und möglicherweise von Version zu Version geändert wird.) Um dieses Problem zu beheben, kann die XLL tiefe Kopien aller Excel **zugewiesenen XLOPER/XLOPER12s** erstellen, die an das Arbeitsblatt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34908-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="34908-160">Eine Lösung, die diese Einschränkungen vermeidet, besteht im Auffüllen und Zurückgeben eines thread lokalen **XLOPER/XLOPER12-Ansatzes,** der erfordert, dass **xlAutoFree/xlAutoFree12** den **XLOPER/XLOPER12-Zeiger** selbst nicht frei gibt.</span><span class="sxs-lookup"><span data-stu-id="34908-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="34908-161">Die nächste Frage ist, wie Sie den thread-lokalen Speicher einrichten und  abrufen, d. h. wie sie die Funktion get_thread_local_xloper12 im vorherigen Beispiel implementieren.</span><span class="sxs-lookup"><span data-stu-id="34908-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="34908-162">Dies erfolgt mithilfe der Thread Local Storage (TLS)-API.</span><span class="sxs-lookup"><span data-stu-id="34908-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="34908-163">Der erste Schritt besteht im Abrufen eines TLS-Index mithilfe von **TlsAlloc**, der letztendlich mit **TlsFree freigegeben werden muss.**</span><span class="sxs-lookup"><span data-stu-id="34908-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="34908-164">Beides wird am besten über **DllMain erreicht.**</span><span class="sxs-lookup"><span data-stu-id="34908-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="34908-165">Nachdem Sie den Index erhalten haben, besteht der nächste Schritt in der Zuweisung eines Speicherblocks für jeden Thread.</span><span class="sxs-lookup"><span data-stu-id="34908-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="34908-166">In [Windows Entwicklungsdokumentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) wird empfohlen, dies jedes Mal zu tun, wenn die **DllMain-Rückruffunktion** mit einem **DLL_THREAD_ATTACH-Ereignis** aufgerufen wird, und den Arbeitsspeicher für alle **DLL_THREAD_DETACH.**</span><span class="sxs-lookup"><span data-stu-id="34908-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="34908-167">Wenn Sie jedoch diesen Ratschlag erhalten, würde ihre DLL unnötige Arbeit für Threads tun, die nicht für die Neuberechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34908-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="34908-168">Stattdessen ist es besser, eine Strategie zum Zuordnen bei erster Verwendung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="34908-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="34908-169">Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="34908-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="34908-170">Für die vorherigen Beispiele, die **XLOPERs** oder **XLOPER12s** zurückgeben, reicht das Folgende aus, Aber Sie können eine beliebige Struktur erstellen, die Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="34908-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="34908-171">Die folgende Funktion ruft einen Zeiger auf die thread-lokale Instanz ab oder weist einen zu, wenn dies der erste Aufruf ist.</span><span class="sxs-lookup"><span data-stu-id="34908-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="34908-172">Jetzt können Sie sehen, wie der thread-lokale **XLOPER/XLOPER12-Speicher** erhalten wird: Zuerst erhalten Sie einen Zeiger auf die Threadinstanz von **TLS_data**, und dann geben Sie einen Zeiger auf den darin enthaltenen **XLOPER/XLOPER12** zurück, wie folgt.</span><span class="sxs-lookup"><span data-stu-id="34908-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="34908-173">Die **mtr_safe_example_1** und **mtr_safe_example_2** können als threadsichere Arbeitsblattfunktionen registriert werden, wenn Sie Excel.</span><span class="sxs-lookup"><span data-stu-id="34908-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="34908-174">Sie können die beiden Ansätze jedoch nicht in einer XLL kombinieren.</span><span class="sxs-lookup"><span data-stu-id="34908-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="34908-175">Ihre XLL kann nur eine Implementierung von **xlAutoFree** und **xlAutoFree12** exportieren, und jede Speicherstrategie erfordert einen anderen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="34908-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="34908-176">Bei **mtr_safe_example_1** der an **xlAutoFree/xlAutoFree12** übergebene Zeiger zusammen mit allen Daten, auf die er verweist, frei.</span><span class="sxs-lookup"><span data-stu-id="34908-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="34908-177">Bei **mtr_safe_example_2** nur die Daten mit Spitzstrichen frei.</span><span class="sxs-lookup"><span data-stu-id="34908-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="34908-178">Windows bietet auch eine Funktion **GetCurrentThreadId**, die die eindeutige systemweite ID des aktuellen Threads zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="34908-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="34908-179">Dies bietet dem Entwickler eine andere Möglichkeit, code thread sicher zu machen oder seinen Verhaltensthread spezifisch zu machen.</span><span class="sxs-lookup"><span data-stu-id="34908-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="34908-180">Nur von mehreren Threads auf Arbeitsspeicher barrierefrei: Kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="34908-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="34908-181">Sie sollten den Lese-/Schreibspeicher schützen, auf den mehrere Threads in kritischen Abschnitten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="34908-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="34908-182">Sie benötigen einen benannten kritischen Abschnitt für jeden Speicherblock, den Sie schützen möchten.</span><span class="sxs-lookup"><span data-stu-id="34908-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="34908-183">Sie können diese während des Aufrufs der **xlAutoOpen-Funktion** initialisieren und lossenken und während des Aufrufs der **xlAutoClose-Funktion** auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="34908-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="34908-184">Anschließend müssen Sie jeden Zugriff auf den geschützten Block innerhalb eines Aufrufpaars von **EnterCriticalSection** und **LeaveCriticalSection enthalten.**</span><span class="sxs-lookup"><span data-stu-id="34908-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="34908-185">Es ist immer nur ein Thread in den kritischen Abschnitt zulässig.</span><span class="sxs-lookup"><span data-stu-id="34908-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="34908-186">Im Folgenden finden Sie ein Beispiel für die Initialisierung, Uninitialisierung und Verwendung eines Abschnitts namens **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="34908-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="34908-187">Eine andere, vielleicht sicherere Möglichkeit zum Schutz eines Speicherblocks besteht in der Erstellung einer Klasse, die eigene **CRITICAL_SECTION** enthält und deren Konstruktor-, Destruktor- und Accessormethoden sich um ihre Verwendung kümmern.</span><span class="sxs-lookup"><span data-stu-id="34908-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="34908-188">Dieser Ansatz hat den zusätzlichen Vorteil, dass Objekte geschützt werden, die vor der Ausführung von **xlAutoOpen** initialisiert werden oder nach dem Aufgerufen von **xlAutoClose** erhalten bleiben. Sie sollten jedoch vorsichtig sein, wenn Sie zu viele kritische Abschnitte und den dadurch zu erstellenden Betriebssystemaufwand erstellen.</span><span class="sxs-lookup"><span data-stu-id="34908-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="34908-189">Wenn Sie über Code verfügen, der gleichzeitig Zugriff auf mehr als einen Geschützten Speicherblock benötigt, müssen Sie die Reihenfolge, in der die kritischen Abschnitte eingegeben und beendet werden, sehr sorgfältig berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="34908-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="34908-190">Die folgenden beiden Funktionen könnten beispielsweise einen Deadlock erzeugen.</span><span class="sxs-lookup"><span data-stu-id="34908-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="34908-191">Wenn die erste Funktion in  einem Thread g_csSharedTableA, während die zweite in einem anderen Thread **g_csSharedTableB,** hängen beide Threads.</span><span class="sxs-lookup"><span data-stu-id="34908-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="34908-192">Der richtige Ansatz besteht in einer konsistenten Reihenfolge und beenden Sie wie folgt in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="34908-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="34908-193">Nach Möglichkeit ist es aus Der Sicht der Threadkooperation besser, den Zugriff auf unterschiedliche Blöcke zu isolieren, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="34908-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="34908-194">Wenn es für eine freigegebene Ressource viele Streit gibt, z. B. häufige Zugriffsanforderungen für kurze Zeit, sollten Sie die Möglichkeit des kritischen Abschnitts zum Drehen in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="34908-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="34908-195">Dies ist eine Technik, die das Warten auf die Ressource weniger prozessorintensiv macht.</span><span class="sxs-lookup"><span data-stu-id="34908-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="34908-196">Dazu können Sie entweder **InitializeCriticalSectionAndSpinCount** beim Initialisieren des Abschnitts oder **SetCriticalSectionSpinCount** nach der Initialisierung verwenden, um die Anzahl der Threadschleifen vor dem Warten auf die Verfügbarheit von Ressourcen zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="34908-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="34908-197">Der Wartevorgang ist aufwändig, daher wird dies durch Das Drehen vermieden, wenn die Ressource in der Zwischenzeit frei wird.</span><span class="sxs-lookup"><span data-stu-id="34908-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="34908-198">Bei einem Einzelnen Prozessorsystem wird die Anzahl der Drehungen effektiv ignoriert, Sie können sie jedoch trotzdem angeben, ohne schaden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="34908-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="34908-199">Der Speicherheap-Manager verwendet eine Drehanzahl von 4000.</span><span class="sxs-lookup"><span data-stu-id="34908-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="34908-200">Weitere Informationen zur Verwendung kritischer Abschnitte finden Sie in der Dokumentation Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="34908-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34908-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34908-201">See also</span></span>



[<span data-ttu-id="34908-202">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="34908-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="34908-203">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="34908-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="34908-204">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="34908-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

