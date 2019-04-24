---
title: Multithreading und Speicher Konflikte in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in Excel, Arbeitsspeicher Konflikte in Excel, Funktionen [Excel 2007], Thread-sichere, threadsichere Funktionen [Excel 2007], Thread-lokaler Arbeitsspeicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301638"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="d1819-104">Multithreading und Speicher Konflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="d1819-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="d1819-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d1819-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d1819-106">Versionen von Microsoft Excel vor Excel 2007 verwenden einen einzelnen Thread für alle Arbeitsblattberechnungen.</span><span class="sxs-lookup"><span data-stu-id="d1819-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="d1819-107">Excel kann jedoch ab Excel 2007 für die Verwendung von 1 bis 1024 gleichzeitigen Threads für die Arbeitsblatt Berechnung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="d1819-108">Bei einem Multi-Processor-oder Multi-Core-Computer entspricht die Standardanzahl von Threads der Anzahl von Prozessoren oder Kernen.</span><span class="sxs-lookup"><span data-stu-id="d1819-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="d1819-109">Daher können threadsichere Zellen oder Zellen, die nur Funktionen enthalten, die threadsicher sind, gleichzeitigen Threads zugewiesen werden, vorbehaltlich der üblichen neuberechnungs Logik, die nach ihren Vorgänger Berechnungen berechnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d1819-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="d1819-110">Thread sichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1819-110">Thread-Safe Functions</span></span>

<span data-ttu-id="d1819-111">Die meisten der integrierten Arbeitsblattfunktionen, die in Excel 2007 beginnen, sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="d1819-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="d1819-112">Sie können XLL-Funktionen auch als threadsicher schreiben und registrieren.</span><span class="sxs-lookup"><span data-stu-id="d1819-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="d1819-113">Excel verwendet einen Thread (seinen Hauptthread), um alle Befehle, Thread unsichere Funktionen, **xlAuto** -Funktionen (außer [xlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12**) sowie com-und Visual Basic für Applikationen (VBA)-Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1819-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="d1819-114">Wenn eine XLL-Funktion eine **XLOPER** oder **XLOPER12** mit **xlbitDLLFree** -Satz zurückgibt, verwendet Excel den gleichen Thread, auf dem der Funktionsaufruf ausgeführt wurde, um **xlAutoFree** oder **xlAutoFree12**aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1819-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="d1819-115">Der Aufruf von **xlAutoFree** oder **xlAutoFree12** erfolgt vor dem nächsten Funktionsaufruf für diesen Thread.</span><span class="sxs-lookup"><span data-stu-id="d1819-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="d1819-116">Für XLL-Entwickler gibt es Vorteile beim Erstellen von threadsicheren Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d1819-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="d1819-117">Sie ermöglichen Excel das Beste aus einem Computer mit mehreren Prozessoren oder Mehrprozessor Kernen.</span><span class="sxs-lookup"><span data-stu-id="d1819-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="d1819-118">Sie eröffnen die Möglichkeit, Remoteserver wesentlich effizienter zu verwenden als mit einem einzigen Thread.</span><span class="sxs-lookup"><span data-stu-id="d1819-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="d1819-119">Angenommen, Sie verfügen über einen Computer mit einem Prozessor, der für die Verwendung von, sagen wir, *N* -Threads konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1819-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="d1819-120">Angenommen, eine Arbeitsmappe wird ausgeführt, die eine hohe Anzahl von Aufrufen einer XLL-Funktion ausgibt, die wiederum eine Datenanforderung sendet oder eine Berechnung für einen Remoteserver oder-Cluster von Servern durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1819-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="d1819-121">Abhängig von der Topologie der Abhängigkeitsstruktur kann Excel die Funktion N-mal fast gleichzeitig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d1819-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="d1819-122">Unter der Voraussetzung, dass der Server oder die Server ausreichend schnell oder parallel sind, kann die Neuberechnungszeit des Arbeitsblatts um den Faktor 1/N reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="d1819-123">Das Hauptproblem beim Schreiben von threadsicheren Funktionen ist das korrekte verarbeiten von Ressourcenkonflikten.</span><span class="sxs-lookup"><span data-stu-id="d1819-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="d1819-124">Dies ist in der Regelspeicher Konflikte und kann in zwei Probleme unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="d1819-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="d1819-125">Das Erstellen von Arbeitsspeicher, den Sie kennen, wird nur von diesem Thread verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1819-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="d1819-126">Sicherstellen, dass auf freigegebener Arbeitsspeicher über mehrere Threads sicher zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="d1819-127">Das erste, was Sie beachten sollten, ist der Zugriff auf den Arbeitsspeicher in einer XLL für alle Threads, auf den nur über den aktuell ausgeführten Thread zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1819-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="d1819-128">**Zugänglich für alle Threads**</span><span class="sxs-lookup"><span data-stu-id="d1819-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="d1819-129">Variablen, Strukturen und Klasseninstanzen, die außerhalb des Texts einer Funktion deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1819-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="d1819-130">Statische Variablen, die innerhalb des Texts einer Funktion deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="d1819-131">In diesen beiden Fällen wird der Speicherplatz im Speicherblock der DLL reserviert, der für diese DLL-Instanz erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1819-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="d1819-132">Wenn eine andere Anwendungsinstanz die DLL lädt, erhält Sie eine eigene Kopie dieses Speichers, sodass keine Konflikte für diese Ressourcen von außerhalb dieser DLL-Instanz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d1819-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="d1819-133">**Nur vom aktuellen Thread zugänglich**</span><span class="sxs-lookup"><span data-stu-id="d1819-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="d1819-134">Automatische Variablen innerhalb des Funktionscodes (einschließlich der Funktionsargumente).</span><span class="sxs-lookup"><span data-stu-id="d1819-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="d1819-135">In diesem Fall wird der Speicher für jede Instanz des Funktionsaufrufs auf dem Stapel reserviert.</span><span class="sxs-lookup"><span data-stu-id="d1819-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d1819-136">Der Bereich des dynamisch zugewiesenen Arbeitsspeichers hängt vom Bereich des Zeigers ab, der darauf zeigt: Wenn der Mauszeiger auf alle Threads zugreifen kann, ist auch der Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d1819-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="d1819-137">Wenn der Zeiger eine automatische Variable in einer Funktion ist, ist der zugewiesene Arbeitsspeicher effektiv für diesen Thread privat.</span><span class="sxs-lookup"><span data-stu-id="d1819-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="d1819-138">Arbeitsspeicher, der von nur einem Thread zugänglich ist: Thread-lokaler Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="d1819-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="d1819-139">Da statische Variablen innerhalb des Texts einer Funktion für alle Threads zugänglich sind, sind die Funktionen, die Sie verwenden, eindeutig nicht threadsicher.</span><span class="sxs-lookup"><span data-stu-id="d1819-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="d1819-140">Eine Instanz der Funktion in einem Thread könnte den Wert ändern, während eine andere Instanz in einem anderen Thread davon ausgeht, dass es sich um etwas vollständig anderes handelt.</span><span class="sxs-lookup"><span data-stu-id="d1819-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="d1819-141">Es gibt zwei Gründe für das Deklarieren von statischen Variablen innerhalb einer Funktion:</span><span class="sxs-lookup"><span data-stu-id="d1819-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="d1819-142">Statische Daten bleiben von einem Aufruf zum nächsten erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1819-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="d1819-143">Ein Zeiger auf statische Daten kann sicher von der Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="d1819-144">Im ersten Grund möchten Sie möglicherweise Daten beibehalten, die für alle Aufrufe der Funktion von Bedeutung sind: vielleicht ein einfacher Zähler, der bei jedem Aufruf der Funktion in einem Thread erhöht wird, oder eine Struktur, die Nutzungs-und Leistungsdaten von Eve sammelt. Anruf.</span><span class="sxs-lookup"><span data-stu-id="d1819-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="d1819-145">Die Frage ist, wie die freigegebenen Daten oder die Datenstruktur geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="d1819-146">Am besten verwenden Sie den Abschnitt Critical Section, wie im nächsten Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="d1819-147">Wenn die Daten nur für die Verwendung durch diesen Thread vorgesehen sind, was der Fall für den Grund 1 sein kann und bei Grund 2 immer der Fall ist, stellt sich die Frage, wie Arbeitsspeicher erstellt werden soll, der aber nur von diesem Thread aus zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="d1819-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="d1819-148">Eine Lösung besteht darin, die TLS-API (Thread-Local Storage) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1819-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="d1819-149">Betrachten Sie beispielsweise eine Funktion, die einen Zeiger auf eine **XLOPER**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d1819-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="d1819-150">Diese Funktion ist nicht threadsicher, da ein Thread die statische **XLOPER12** zurückgeben kann, während eine andere überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="d1819-151">Die Wahrscheinlichkeit für dieses Ereignis ist noch größer, wenn die **XLOPER12** an **xlAutoFree12**übergeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d1819-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="d1819-152">Eine Lösung besteht darin, eine **XLOPER12**zu reservieren, einen Zeiger darauf zurückzugeben und **xlAutoFree12** zu implementieren, damit der **XLOPER12** -Speicher selbst freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="d1819-153">Dieser Ansatz wird in vielen der Beispiel Funktionen verwendet, die in der [Speicherverwaltung in Excel](memory-management-in-excel.md)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="d1819-154">Dieser Ansatz ist einfacher zu implementieren als der im nächsten Abschnitt beschriebene Ansatz, der auf der TLS-API basiert, aber einige Nachteile hat.</span><span class="sxs-lookup"><span data-stu-id="d1819-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="d1819-155">Zunächst muss Excel **xlAutoFree**/ **xlAutoFree12** aufrufen, unabhängig vom Typ des zurückgegebenen **XLOPER**/ -**XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="d1819-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="d1819-156">Zweitens gibt es ein Problem beim Zurückgeben von **XLOPER**/ **XLOPER12**s, die der Rückgabewert eines Aufrufs an eine C-API-Rückruffunktion sind.</span><span class="sxs-lookup"><span data-stu-id="d1819-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="d1819-157">Der **XLOPER**/ -**XLOPER12** kann auf Speicher verweisen, der von Excel freigegeben werden muss, aber die **XLOPER**/ -**XLOPER12** selbst muss auf die gleiche Weise freigegeben werden, wie Sie zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="d1819-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="d1819-158">Wenn ein solches **XLOPER**/ -**XLOPER12** als Rückgabewert einer XLL-Arbeitsblattfunktion verwendet werden soll, gibt es keine einfache Möglichkeit, **xlAutoFree**/ **xlAutoFree12** darüber zu informieren, dass beide Zeiger auf die entsprechende Weise freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d1819-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="d1819-159">(Sowohl die **xlbitXLFree** -als auch die **xlbitDLLFree** -Einstellung lösen das Problem nicht, da die Behandlung von **XLOPER/XLOPER12s** in Excel mit beiden Sätzen nicht definiert ist und möglicherweise von Version zu Version wechselt.) Um dieses Problem zu umgehen, kann die XLL Tiefe Kopien aller Excel-reservierten **XLOPER/XLOPER12s** , die es an das Arbeitsblatt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d1819-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="d1819-160">Eine Lösung, die diese Einschränkungen verhindert, ist das Auffüllen und Zurückgeben eines Thread-lokalen **XLOPER/XLOPER12**, ein Ansatz, der erfordert, dass **xlAutoFree/xlAutoFree12** den **XLOPER/XLOPER12-** Zeiger selbst nicht freilässt.</span><span class="sxs-lookup"><span data-stu-id="d1819-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="d1819-161">Die nächste Frage ist, wie Sie den threadlokalen Arbeitsspeicher einrichten und abrufen, mit anderen Worten, wie Sie die Funktion **get_thread_local_xloper12** im vorherigen Beispiel implementieren.</span><span class="sxs-lookup"><span data-stu-id="d1819-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="d1819-162">Dies erfolgt mithilfe der TLS-API (Local Storage).</span><span class="sxs-lookup"><span data-stu-id="d1819-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="d1819-163">Der erste Schritt besteht darin, einen TLS-Index mithilfe von **TlsAlloc**abzurufen, der letztendlich mithilfe von **TlsFree**veröffentlicht werden muss.</span><span class="sxs-lookup"><span data-stu-id="d1819-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="d1819-164">Beides wird am besten von **DllMain**aus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1819-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="d1819-165">Nachdem Sie den Index abgerufen haben, besteht der nächste Schritt im Zuweisen eines Speicherblocks für jeden Thread.</span><span class="sxs-lookup"><span data-stu-id="d1819-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="d1819-166">Die [Windows-Entwicklungsdokumentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) empfiehlt dies jedes Mal, wenn die **DllMain** -Rückruffunktion mit einem **DLL_THREAD_ATTACH** -Ereignis aufgerufen wird und der Arbeitsspeicher auf jeder **DLL_THREAD_DETACH**freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="d1819-167">Wenn Sie jedoch diese Ratschläge befolgen, würde Ihre DLL unnötige Arbeit für Threads ausführen, die nicht für die Neuberechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="d1819-168">Stattdessen empfiehlt es sich, eine Allocate-on-First-use-Strategie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1819-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="d1819-169">Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="d1819-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="d1819-170">Für die vorherigen Beispiele, die **XLOPERs** oder **XLOPER12s**zurückgeben, genügt Folgendes, aber Sie können eine beliebige Struktur erstellen, die Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="d1819-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="d1819-171">Die folgende Funktion Ruft einen Zeiger auf die Thread-lokale Instanz ab oder ordnet einen an, wenn es sich um den ersten Aufruf handelt.</span><span class="sxs-lookup"><span data-stu-id="d1819-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="d1819-172">Jetzt können Sie sehen, wie der Thread-lokale **XLOPER/XLOPER12** -Arbeitsspeicher abgerufen wird: zuerst rufen Sie einen Zeiger auf die Instanz von **TLS_data**des Threads ab und geben dann wie folgt einen Zeiger auf die darin enthaltene **XLOPER/XLOPER12** zurück.</span><span class="sxs-lookup"><span data-stu-id="d1819-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="d1819-173">Die **mtr_safe_example_1** -und **mtr_safe_example_2** -Funktionen können bei der Verwendung von Excel als threadsichere Arbeitsblattfunktionen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="d1819-174">Die beiden Ansätze können jedoch nicht in einer XLL kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="d1819-175">Ihre XLL kann nur eine Implementierung von **xlAutoFree** und **xlAutoFree12**exportieren, und jede Speicherstrategie erfordert eine andere Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="d1819-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="d1819-176">Bei **mtr_safe_example_1**muss der an **xlAutoFree/xlAutoFree12** übergebene Zeiger zusammen mit allen Daten freigegeben werden, auf die er verweist.</span><span class="sxs-lookup"><span data-stu-id="d1819-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="d1819-177">Bei **mtr_safe_example_2**sollten nur die gezeigten Daten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1819-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="d1819-178">Windows stellt auch eine Funktion **GetCurrentThreadId**bereit, die die eindeutige systemweite ID des aktuellen Threads zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d1819-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="d1819-179">Dadurch erhält der Entwickler eine andere Möglichkeit, Code threadsicher zu machen, oder um sein Verhalten Thread spezifisch zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="d1819-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="d1819-180">Arbeitsspeicher, der nur von mehreren Threads zugänglich ist: kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="d1819-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="d1819-181">Sie sollten Lese-/Schreibzugriff schützen, auf den über kritische Abschnitte über mehrere Threads zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1819-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="d1819-182">Sie benötigen einen benannten kritischen Abschnitt für jeden zu schützenden Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="d1819-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="d1819-183">Sie können diese während des Aufrufs der **xlAutoOpen** -Funktion initialisieren und freigeben und Sie während des Aufrufs der **xlAutoClose** -Funktion auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="d1819-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="d1819-184">Sie müssen dann jeden Zugriff auf den geschützten Block in einem Paar von Aufrufen an **EnterCriticalSection** und **LeaveCriticalSection**enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1819-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="d1819-185">Nur ein Thread ist jederzeit im kritischen Abschnitt zulässig.</span><span class="sxs-lookup"><span data-stu-id="d1819-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="d1819-186">Nachfolgend finden Sie ein Beispiel für die Initialisierung, die uninitialisierung und die Verwendung eines Abschnittsnamens **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="d1819-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="d1819-187">Eine weitere, vielleicht sicherere Möglichkeit zum Schutz eines Speicherblocks besteht darin, eine Klasse zu erstellen, die eine eigene **CRITICAL_SECTION** enthält und deren Konstruktor, Destruktor und Accessor-Methoden sich um ihre Verwendung kümmern.</span><span class="sxs-lookup"><span data-stu-id="d1819-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="d1819-188">Dieser Ansatz hat den zusätzlichen Vorteil, Objekte zu schützen, die möglicherweise initialisiert werden, bevor **xlAutoOpen** ausgeführt wird, oder zu überleben, nachdem **xlAutoClose** aufgerufen wurde, aber Sie sollten vorsichtig sein, um zu viele kritische Abschnitte und das Betriebssystem zu erstellen. Aufwand.</span><span class="sxs-lookup"><span data-stu-id="d1819-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="d1819-189">Wenn Sie über Code verfügen, der gleichzeitig auf mehr als einen geschützten Speicherblock zugreifen muss, müssen Sie die Reihenfolge, in der die kritischen Abschnitte eingegeben und beendet werden, sehr sorgfältig prüfen.</span><span class="sxs-lookup"><span data-stu-id="d1819-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="d1819-190">Die folgenden beiden Funktionen können beispielsweise einen Deadlock verursachen.</span><span class="sxs-lookup"><span data-stu-id="d1819-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="d1819-191">Wenn die erste Funktion in einem Thread **g_csSharedTableA** eintritt, während der zweite in einem anderen Thread **g_csSharedTableB**eintritt, hängen beide Threads.</span><span class="sxs-lookup"><span data-stu-id="d1819-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="d1819-192">Die richtige Vorgehensweise ist, wie folgt in eine konsistente Reihenfolge und Exit in umgekehrter Reihenfolge einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d1819-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="d1819-193">Wenn möglich, ist es besser, den Zugriff auf verschiedene Blöcke zu isolieren, wie im folgenden dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d1819-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="d1819-194">Wo es eine große Anzahl von Konflikten für eine freigegebene Ressource gibt, wie beispielsweise häufige Zugriffsanforderungen für kurze Zeit, sollten Sie erwägen, die Fähigkeit des kritischen Abschnitts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1819-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="d1819-195">Dies ist eine Technik, die das warten auf die Ressource abnimmt.</span><span class="sxs-lookup"><span data-stu-id="d1819-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="d1819-196">Zu diesem Zweck können Sie entweder **InitializeCriticalSectionAndSpinCount** beim Initialisieren des Abschnitts oder der **SetCriticalSectionSpinCount** nach der Initialisierung verwenden, um festzulegen, wie oft der Thread Schleifen soll, bevor darauf gewartet wird, dass Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1819-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="d1819-197">Der Wartevorgang ist teuer, daher wird dies durch Drehen vermieden, wenn die Ressource in der Zwischenzeit freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1819-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="d1819-198">Bei einem einzelnen Prozessorsystem wird die Anzahl der Drehungen effektiv ignoriert, aber Sie können Sie trotzdem angeben, ohne dass Sie Schaden anrichten müssen.</span><span class="sxs-lookup"><span data-stu-id="d1819-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="d1819-199">Der Speicherheap-Manager verwendet eine Drehungs Anzahl von 4000.</span><span class="sxs-lookup"><span data-stu-id="d1819-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="d1819-200">Weitere Informationen zur Verwendung kritischer Abschnitte finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="d1819-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1819-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1819-201">See also</span></span>



[<span data-ttu-id="d1819-202">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="d1819-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="d1819-203">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="d1819-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="d1819-204">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="d1819-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

