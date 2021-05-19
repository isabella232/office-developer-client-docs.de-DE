---
title: Speicherverwaltung in Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Arbeitsspeicher xloper12 [excel 2007], Verwalten von Speicher in Excel, Excel-Stapel, Zeichenfolgen [Excel 2007], Speicherverwaltung, Speicherverwaltung in Excel, XLOPER-Speicher [Excel 2007], Speicher [Excel 2007], Richtlinien für die Verwaltung
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419541"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="134f4-104">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="134f4-104">Memory Management in Excel</span></span>

 <span data-ttu-id="134f4-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="134f4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="134f4-p101">Beim Erstellen von effizienten und stabilen XLL-Dateien ist die Speicherverwaltung von zentraler Bedeutung. Wenn Speicher nicht korrekt verwaltet wird, kann dies zu einer Reihe von Problemen in Microsoft Excel führen – von kleineren Problemen, wie z. B. eine ineffiziente Speicherzuteilung und -initialisierung und kleinere Speicherverluste, bis hin zu größeren Problemen, wie z. B. eine Destabilisierung von Excel.</span><span class="sxs-lookup"><span data-stu-id="134f4-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="134f4-p102">Eine fehlerhafte Verwaltung von Speicher ist die häufigste Ursache von schwerwiegenden Fehlern im Zusammenhang mit Add-Ins. Sie sollten daher Ihr Projekt mit einer konsistenten und gut durchdachten Strategie für Speicherverwaltung erstellen. </span><span class="sxs-lookup"><span data-stu-id="134f4-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="134f4-110">Die Speicherverwaltung in Microsoft Office Excel 2007 wurde mit der Einführung der Multithreaded-Arbeitsmappenneuberechnung zunehmend komplexer.</span><span class="sxs-lookup"><span data-stu-id="134f4-110">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation.</span></span> <span data-ttu-id="134f4-111">Wenn Sie threadsichere Arbeitsblattfunktionen erstellen und exportieren möchten, müssen Sie die Konflikte verwalten, die auftreten können, wenn mehrere Threads um Zugriff konkurrieren.</span><span class="sxs-lookup"><span data-stu-id="134f4-111">If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="134f4-112">Für die folgenden drei Datenstrukturtypen gibt es Überlegungen im Hinblick auf den Speicher:</span><span class="sxs-lookup"><span data-stu-id="134f4-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="134f4-113">**XLOPER** s und **XLOPER12** s</span><span class="sxs-lookup"><span data-stu-id="134f4-113">**XLOPER** s and **XLOPER12** s</span></span>
    
- <span data-ttu-id="134f4-114">Zeichenfolgen, die nicht in **XLOPER** oder **XLOPER12** enthalten sind</span><span class="sxs-lookup"><span data-stu-id="134f4-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="134f4-115">**FP**- und **FP12**-Arrays</span><span class="sxs-lookup"><span data-stu-id="134f4-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="134f4-116">XLOPER/XLOPER12-Speicher</span><span class="sxs-lookup"><span data-stu-id="134f4-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="134f4-117">Die **XLOPER**/ **XLOPER12**-Datenstruktur weist einige Untertypen auf, die Zeiger auf Speicherblöcke enthalten, und zwar Zeichenfolgen (**xltypeStr**), Arrays (**xltypeMulti**) und externe Verweise (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="134f4-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="134f4-118">Beachten Sie auch, dass **xltypeMulti**-Arrays die Zeichenfolgen **XLOPER**/ **XLOPER12s** enthalten können, die wiederum auf andere Speicherblöcke zeigen.</span><span class="sxs-lookup"><span data-stu-id="134f4-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="134f4-119">Ein **XLOPER**/ **XLOPER12** kann auf verschiedene Arten erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="134f4-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="134f4-120">Von Excel bei der Vorbereitung von Argumenten, die an eine XLL-Funktion übergeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="134f4-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="134f4-121">Von Excel beim Zurückgeben von **XLOPER** oder **XLOPER12** in einem C-API-Aufruf</span><span class="sxs-lookup"><span data-stu-id="134f4-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="134f4-122">Von der DLL beim Erstellen von Argumenten, die an einen C-API-Aufruf übergeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="134f4-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="134f4-123">Von der DLL beim Erstellen eines Rückgabewerts einer XLL-Funktion</span><span class="sxs-lookup"><span data-stu-id="134f4-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="134f4-124">Ein Speicherblock innerhalb eines der auf den Speicher zeigenden Typen kann auf verschiedene Weise zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="134f4-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="134f4-125">Als statischer Block innerhalb Ihrer DLL außerhalb des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="134f4-126">Als statischer Block innerhalb Ihrer DLL innerhalb eines Teils des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="134f4-127">Der Block kann dynamisch von der DLL auf verschiedene Weise zugeteilt und freigegeben werden: **malloc** und **free**, **new** und **delete** und so weiter.</span><span class="sxs-lookup"><span data-stu-id="134f4-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="134f4-128">Er kann dynamisch von Excel zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="134f4-129">Angesichts der Anzahl möglicher Ursprünge für **XLOPER**/ **XLOPER12**-Speicher und der Anzahl von Situationen, in denen der Speicher möglicherweise von **XLOPER**/ **XLOPER12** zugewiesen wurde, ist es nicht verwunderlich, dass dieses Thema sehr schwierig erscheinen mag.</span><span class="sxs-lookup"><span data-stu-id="134f4-129">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult.</span></span> <span data-ttu-id="134f4-130">Die Komplexität kann jedoch erheblich verringert werden, wenn Sie mehrere Regeln und Richtlinien beachten.</span><span class="sxs-lookup"><span data-stu-id="134f4-130">However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="134f4-131">Regeln für das Arbeiten mit XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="134f4-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="134f4-132">Versuchen Sie nicht, Speicher freizugeben oder **XLOPERs**/ **XLOPER12** s zu überschreiben, die als Argumente an Ihre XLL-Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-132">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12** s that are passed as arguments to your XLL function.</span></span> <span data-ttu-id="134f4-133">Sie sollten diese Argumente als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="134f4-133">You should treat such arguments as read-only.</span></span> <span data-ttu-id="134f4-134">Weitere Informationen finden Sie unter „Zurückgeben von **XLOPER** oder **XLOPER12** durch Ändern von vorhandenen Argumenten“ unter [Bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="134f4-134">For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="134f4-135">Wenn Excel Speicher für ein **XLOPER**/ **XLOPER12** zugeteilt hat, das von Ihrer DLL in einem Aufruf der C-API zurückgegeben wurde:</span><span class="sxs-lookup"><span data-stu-id="134f4-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="134f4-136">Sie müssen den Speicher durch einen Aufruf von [xlFree](xlfree.md) freigeben, wenn Sie **XLOPER**/ **XLOPER12** nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="134f4-136">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md).</span></span> <span data-ttu-id="134f4-137">Verwenden Sie keine andere Methode, z. B. „free“ oder „delete“, um den Speicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-137">Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="134f4-138">Wenn der zurückgegebene Typ **xltypeMulti** ist, überschreiben Sie keine **XLOPER**/ **XLOPER12** s innerhalb des Arrays, insbesondere, wenn sie Zeichenfolgen enthalten, und vor allem nicht, wenn Sie das Überschreiben mit einer Zeichenfolge versuchen.</span><span class="sxs-lookup"><span data-stu-id="134f4-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12** s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="134f4-139">Wenn Sie **XLOPER**/ **XLOPER12** in Excel als Rückgabewert für die DLL-Funktion zurückgeben möchten, müssen Sie Excel anweisen, nach Abschluss des Vorgangs Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="134f4-140">Sie müssen **xlFree** nur in einem **XLOPER**/ **XLOPER12** aufrufen, das als Rückgabewert für einen C-API-Aufruf erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="134f4-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="134f4-141">Wenn die DLL Speicher für ein **XLOPER**/ **XLOPER12** zugeteilt hat, das Sie in Excel als Rückgabewert für die DLL-Funktion zurückgeben möchten, müssen Sie Excel mitteilen, dass die DLL Speicherplatz freigeben muss. </span><span class="sxs-lookup"><span data-stu-id="134f4-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="134f4-142">Richtlinien für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="134f4-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="134f4-p108">Achten Sie darauf, dass die DLL in der Methode, die Sie zum Zuteilen und Freigeben des Speichers verwenden, konsistent ist. Vermischen Sie keine Methoden. Ein guter Ansatz besteht darin, die verwendete Methode in einer Speicherklasse oder -struktur zu umschließen, in der Sie die verwendete Methode ändern können, ohne den Code an vielen Stellen zu verändern.</span><span class="sxs-lookup"><span data-stu-id="134f4-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="134f4-p109">Bleiben Sie bei der Erstellung von **xltypeMulti**-Arrays innerhalb der DLL beim Zuteilen von Speicher für Zeichenfolgen konsistent: Teilen Sie den Speicher immer dynamisch zu, oder verwenden Sie immer statischen Speicher. Wenn Sie dies tun, wissen Sie beim Freigeben des Speichers, dass Sie die Zeichenfolgen immer oder nie freigeben müssen.</span><span class="sxs-lookup"><span data-stu-id="134f4-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="134f4-148">Erstellen Sie tiefe Kopien des Speichers, der Excel zugeteilt ist, wenn Sie ein in Excel erstelltes **XLOPER**/ **XLOPER12** kopieren.</span><span class="sxs-lookup"><span data-stu-id="134f4-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="134f4-149">Setzen Sie die Excel zugeordnete Zeichenfolgen **XLOPER**/ **XLOPER12** s nicht in **XltypeMulti**-Arrays ein.</span><span class="sxs-lookup"><span data-stu-id="134f4-149">Do not put Excel-allocated string **XLOPER**/ **XLOPER12** s within **xltypeMulti** arrays.</span></span> <span data-ttu-id="134f4-150">Erstellen Sie tiefe Kopien der Zeichenfolgen, und speichern Sie Zeiger auf die Kopien im Array.</span><span class="sxs-lookup"><span data-stu-id="134f4-150">Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="134f4-151">Freigeben von Excel zugewiesenem XLOPER/XLOPER12-Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="134f4-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="134f4-152">Sehen Sie sich den folgenden XLL-Befehl an, der **xlGetName** zum Abrufen einer Zeichenfolge mit dem Pfad und Dateinamen der DLL verwendet und diese mit **xlcAlert** in einem Warnungsdialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="134f4-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="134f4-153">Wenn die Funktion den Arbeitsspeicher, auf den von **xDllName** gezeigt wird, nicht mehr benötigt, kann dieser durch einen Aufruf der [xlFree-Funktion](xlfree.md), eine der C-API-Funktionen (nur DLL), freigegeben werden. </span><span class="sxs-lookup"><span data-stu-id="134f4-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="134f4-154">Die **xlFree**-Funktion ist im Funktionsreferenzabschnitt ausführlich dokumentiert (siehe [C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), beachten Sie aber Folgendes:</span><span class="sxs-lookup"><span data-stu-id="134f4-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="134f4-155">Sie können Zeiger an mehrere **XLOPER**/ **XLOPER12** s in einem einzigen Aufruf von **xlFree** übergeben. Dies wird nur durch die Anzahl der Funktionsargumente beschränkt, die in der ausgeführten Version von Excel unterstützt werden (30 in Excel 2003, 255 ab Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="134f4-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12** s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="134f4-156">**xlFree** legt den enthaltenen Zeiger auf **NULL** fest, um sicherzustellen, dass der Versuch, ein **XLOPER**/ **XLOPER12**, das bereits freigegeben wurde, freizugeben, sicher ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-156">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe.</span></span> <span data-ttu-id="134f4-157">**XlFree** ist die einzige C-API-Funktion, die die zugehörigen Argumente ändert.</span><span class="sxs-lookup"><span data-stu-id="134f4-157">**xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="134f4-158">Sie können problemlos **xlFree** in allen **XLOPER**/ **XLOPER12** aufrufen, die für den Rückgabewert eines Aufrufs der C-API verwendet werden, unabhängig davon, ob ein Zeiger auf Speicher darin enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="134f4-159">Zurückgeben von XLOPER/XLOPER12s, die von Excel freigegeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="134f4-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="134f4-160">Angenommen, Sie möchten den Beispielbefehl im vorherigen Abschnitt bearbeiten und in eine Arbeitsblattfunktion ändern, die den DLL-Pfad und den Dateinamen zurückgibt, wenn ein **Boolean** **true**-Argument übergeben wird, andernfalls **#N/A**.</span><span class="sxs-lookup"><span data-stu-id="134f4-160">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise.</span></span> <span data-ttu-id="134f4-161">Sie können natürlich **xlFree** nicht aufrufen, um den Zeichenfolgenspeicher vor der Rückgabe an Excel freizugeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-161">Clearly you cannot call **xlFree** to release the string memory before returning it to Excel.</span></span> <span data-ttu-id="134f4-162">Wenn der Speicher jedoch nicht irgendwann freigegeben wird, geht bei dem Add-In bei jedem Aufruf der Funktion Speicher verloren.</span><span class="sxs-lookup"><span data-stu-id="134f4-162">However, if it is not freed at some point, the add-in will leak memory every time the function is called.</span></span> <span data-ttu-id="134f4-163">Um dieses Problem zu umgehen, können Sie ein Bit im **xltype**-Feld von **XLOPER**/ **XLOPER12**, definiert als **xlbitXLFree** in „xlcall.h“ festlegen.</span><span class="sxs-lookup"><span data-stu-id="134f4-163">To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h.</span></span> <span data-ttu-id="134f4-164">Wenn dies festgelegt wird, wird Excel angewiesen, den zurückgegebenen Speicher freizugeben, wenn das Kopieren des Werts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-164">Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="134f4-165">Beispiel</span><span class="sxs-lookup"><span data-stu-id="134f4-165">Example</span></span>

<span data-ttu-id="134f4-166">Im folgenden Codebeispiel ist der XLL-Befehl im vorherigen Abschnitt konvertiert in eine XLL-Arbeitsblattfunktion dargestellt.</span><span class="sxs-lookup"><span data-stu-id="134f4-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="134f4-167">XLL-Funktionen, die **XLOPER**/ **XLOPER12** s verwenden, müssen als Zeiger auf **XLOPER**/ **XLOPER12** s deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-167">XLL functions that use **XLOPER**/ **XLOPER12** s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12** s.</span></span> <span data-ttu-id="134f4-168">Die Verwendung in diesem Beispiel eines statischen **XLOPER12** innerhalb der Funktion ist nicht threadsicher.</span><span class="sxs-lookup"><span data-stu-id="134f4-168">The use in this example of a static **XLOPER12** within the function is not thread safe.</span></span> <span data-ttu-id="134f4-169">Sie könnten diese Funktion fälschlicherweise als threadsicher registrieren, würden jedoch riskieren, dass **xRtnValue** von einem Thread überschrieben wird, bevor ein anderer Thread damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-169">You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="134f4-170">Sie müssen **xlbitXLFree** nach dem Aufruf des Excel-Rückrufs festlegen, der dies zuweist.</span><span class="sxs-lookup"><span data-stu-id="134f4-170">You must set **xlbitXLFree** after the call to the Excel callback that allocates it.</span></span> <span data-ttu-id="134f4-171">Wenn Sie dies davor festlegen, wird es überschrieben und hat nicht den gewünschten Effekt.</span><span class="sxs-lookup"><span data-stu-id="134f4-171">If you set it before this, it is overwritten and does not have the effect that you want.</span></span> <span data-ttu-id="134f4-172">Wenn Sie beabsichtigen, den Wert vor der Rückgabe an das Arbeitsblatt als Argument in einem Aufruf einer anderen C-API-Funktion zu verwenden, sollten Sie dieses Bit nach einem derartigen Aufruf festlegen.</span><span class="sxs-lookup"><span data-stu-id="134f4-172">If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call.</span></span> <span data-ttu-id="134f4-173">Andernfalls könnten Sie Funktionen verwechseln, die dieses Bit nicht maskieren, bevor der **XLOPER**/ **XLLOPER12**-Typ überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="134f4-173">Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="134f4-174">Zurückgeben von XLOPER/XLOPER12s, die von der DLL freigegeben werden sollen</span><span class="sxs-lookup"><span data-stu-id="134f4-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="134f4-175">Ein ähnliches Problem tritt auf, wenn Ihre XLL Speicher für ein **XLOPER**/ **XLOPER12** zugewiesen hat und diesen an Excel zurückgeben möchte.</span><span class="sxs-lookup"><span data-stu-id="134f4-175">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel.</span></span> <span data-ttu-id="134f4-176">Excel erkennt ein anderes Bit, das im **xltype**-Feld von **XLOPER**/ **XLOPER12**, definiert als **xlbitDLLFree** in xlcall.h, festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="134f4-176">Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="134f4-177">Wenn Excel **XLOPER**/ **XLOPER12** erhält, wobei dieses Bit festgelegt ist, versucht es, eine Funktion aufzurufen, die von der XLL mit dem Namen [xlAutoFree](xlautofree-xlautofree12.md) (für **XLOPER** s) oder **xlAutoFree12** (für **XLOPER12** s) exportiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="134f4-177">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER** s) or **xlAutoFree12** (for **XLOPER12** s).</span></span> <span data-ttu-id="134f4-178">Diese Funktion wird in der Funktionsreferenz ausführlicher beschrieben (siehe [-Add-In-Manager und XLL-Schnittstellenfunktionen](add-in-manager-and-xll-interface-functions.md)). Hier finden Sie aber eine beispielhafte minimale Implementierung.</span><span class="sxs-lookup"><span data-stu-id="134f4-178">This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here.</span></span> <span data-ttu-id="134f4-179">Ihr Zweck besteht darin, den **XLOPER**/ **XLOPER12**-Speicher auf eine Weise freizugeben, die mit der ursprünglichen Zuweisung konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-179">Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="134f4-180">Beispiele</span><span class="sxs-lookup"><span data-stu-id="134f4-180">Examples</span></span>

<span data-ttu-id="134f4-181">Die folgende Beispielfunktion hat den gleichen Zweck wie die vorherige Funktion, mit der Ausnahme, dass sie den Text „Der vollständige Pfadname für diese DLL ist“ vor dem DLL-Namen umfasst.</span><span class="sxs-lookup"><span data-stu-id="134f4-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="134f4-182">Eine minimal hinreichende Implementierung von **xlAutoFree12** in der XLL, die die vorherige Funktion exportiert hat, wäre wie folgt.</span><span class="sxs-lookup"><span data-stu-id="134f4-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="134f4-p117">Diese Implementierung ist nur ausreichend, wenn die XLL nur **XLOPER12**-Zeichenfolgen zurückgibt und diese Zeichenfolgen nur mithilfe von **malloc** zugewiesen werden. Beachten Sie, dass bei dem Test </span><span class="sxs-lookup"><span data-stu-id="134f4-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="134f4-185">in diesem Fall ein Fehler auftreten würde, da **xlbitDLLFree** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="134f4-186">Im Allgemeinen sollten **xlAutoFree** und **xlAutoFree12** so implementiert werden, dass Speicherplatz freigegeben wird, der von XLL erstellten **xltypeMulti**-Arrays und externen **xltypeRef**-Referenzen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="134f4-187">Vielleicht entschließen Sie sich, Ihre XLL-Funktionen so zu implementieren, dass sie ALLE dynamisch zugewiesenen **XLOPER** s und **XLOPER12** s zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-187">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER** s and **XLOPER12** s.</span></span> <span data-ttu-id="134f4-188">In diesem Fall müssen Sie **xlbitDLLFree** für alle **XLOPER** s und **XLOPER12** s unabhängig von den Untertypen festlegen.</span><span class="sxs-lookup"><span data-stu-id="134f4-188">In this case, you would need to set **xlbitDLLFree** on all such **XLOPER** s and **XLOPER12** s regardless of the sub-type.</span></span> <span data-ttu-id="134f4-189">Außerdem müssten Sie **xlAutoFree** und **xlAutoFree12** implementieren, damit dieser Speicher und auch der gesamte Speicher, auf den innerhalb der **XLOPER**/ **XLOPER12** gezeigt wird, freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="134f4-189">You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="134f4-190">Dieser Ansatz ist eine Möglichkeit, um den Rückgabewert threadsicher zu machen.</span><span class="sxs-lookup"><span data-stu-id="134f4-190">This approach is one way to make the return value thread safe.</span></span> <span data-ttu-id="134f4-191">Die vorherige Funktion könnte z. B. wie folgt umgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-191">For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="134f4-192">Weitere Informationen zu **xlAutoFree** und **xlAutoFree12** finden Sie unter [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="134f4-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="134f4-193">Zurückgeben von Modify-in-Place-Argumenten</span><span class="sxs-lookup"><span data-stu-id="134f4-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="134f4-p119">Excel ermöglicht einer XLL-Funktion, einen Wert durch Ändern eines vorhandenen Arguments zurückzugeben. Dies ist nur mit einem Argument möglich, das als Zeiger übergeben wird. Die Funktion muss hierfür so registriert werden, dass Excel weiß, welches Argument geändert wird. </span><span class="sxs-lookup"><span data-stu-id="134f4-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="134f4-197">Diese Methode des Zurückgebens eines Werts wird für allen Datentypen unterstützt, die von einem Zeiger übergeben werden können, ist jedoch für die folgenden Typen besonders hilfreich:</span><span class="sxs-lookup"><span data-stu-id="134f4-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="134f4-198">ASCII-Bytezeichenfolgen mit Längenzählung, die auf NULL enden</span><span class="sxs-lookup"><span data-stu-id="134f4-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="134f4-199">Unicode-Zeichenfolgen für Breitzeichen mit Längenzählung, die auf NULL enden (beginnend bei Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="134f4-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="134f4-200">**FP**-Gleitkommaarrays</span><span class="sxs-lookup"><span data-stu-id="134f4-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="134f4-201">**FP12**-Gleitkommaarrays (beginnend bei Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="134f4-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="134f4-202">Sie sollten nicht versuchen, **XLOPER** s oder **XLOPER12** s auf diese Weise zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-202">You should not try to return **XLOPER** s or **XLOPER12** s in this manner.</span></span> <span data-ttu-id="134f4-203">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="134f4-203">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="134f4-p121">Der Vorteil der Verwendung dieser Methode besteht darin, dass Excel den Speicher für Rückgabewerte zuweist, anstatt nur die return-Anweisung zu verwenden. Nachdem Excel das Lesen der zurückgegebenen Daten abgeschlossen hat, wird der Speicher freigegeben. Dadurch werden die Speicherverwaltungsaufgaben von der XLL-Funktion gelöst. Diese Technik ist threadsicher: Wenn Funktionen gleichzeitig von Excel in unterschiedlichen Threads aufgerufen werden, verfügt jeder Funktionsaufruf in jedem Thread über seinen eigenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="134f4-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="134f4-208">Dies ist besonders für die zuvor aufgeführten Datentypen hilfreich, da der Mechanismus für den Rückruf der DLL zum Freigeben von Speicher nach der Rückgabe, der für **XLOPER**/ **XLOPER12** s besteht, für einfache Zeichenfolgen und **FP**/ **FP12**-Arrays nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-208">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12** s does not exist for simple strings and **FP**/ **FP12** arrays.</span></span> <span data-ttu-id="134f4-209">Daher stehen Ihnen beim Zurückgeben einer von DLL erstellten Zeichenfolge oder eines Gleitkommaarrays die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="134f4-209">Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="134f4-p123">Legen Sie einen persistenten Zeiger auf einen dynamisch zugewiesenen Puffer fest, und geben Sie den Zeiger zurück. Führen Sie beim nächsten Aufruf der Funktion Folgendes aus: (1) Überprüfen Sie, dass der Zeiger nicht NULL ist. (2) Geben Sie die im vorherigen Aufruf zugewiesenen Ressourcen frei, und setzen Sie den Zeiger auf NULL zurück. (3) Verwenden Sie den Zeiger für einen neu zugewiesenen Speicherblock wieder.</span><span class="sxs-lookup"><span data-stu-id="134f4-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="134f4-212">Erstellen Sie Ihre Zeichenfolgen und Arrays in einem statischen Puffer, der nicht freigegeben werden muss, und geben Sie einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="134f4-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="134f4-213">Ändern Sie ein vorhandenes Argument, und schreiben Ihre Zeichenfolge oder Ihr Array direkt in den von Excel reservierten Platz.</span><span class="sxs-lookup"><span data-stu-id="134f4-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="134f4-214">Andernfalls müssen Sie ein **XLOPER**/ **XLOPER12** erstellen und **xlbitDLLFree** und **xlAutoFree**/ **xlAutoFree12** verwenden, um die Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="134f4-215">Die letzte Option ist die einfachste Lösung, wenn ein Argument mit demselben Typ wie der Rückgabewert an Sie übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="134f4-215">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value.</span></span> <span data-ttu-id="134f4-216">Wichtig ist hierbei, dass Sie beachten, dass die Puffergrößen beschränkt sind und Sie sehr vorsichtig sein müssen, um diese nicht zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="134f4-216">The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them.</span></span> <span data-ttu-id="134f4-217">Wenn dies passiert, kann Excel abstürzen.</span><span class="sxs-lookup"><span data-stu-id="134f4-217">Getting this wrong could crash Excel.</span></span> <span data-ttu-id="134f4-218">Als Nächstes werden Puffergrößen für Zeichenfolgen und **FP**/ **FP12**-Arrays erläutert.</span><span class="sxs-lookup"><span data-stu-id="134f4-218">Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="134f4-219">Strings</span><span class="sxs-lookup"><span data-stu-id="134f4-219">Strings</span></span>

<span data-ttu-id="134f4-220">Probleme mit der Verwaltung von Zeichenfolgenspeicher sind wohl die häufigste Ursache für Instabilität bei Anwendungen und Add-Ins. Dies ist angesichts der Vielzahl von Möglichkeiten zur Behandlung von Zeichenfolgen leicht nachvollziehbar: Zeichenfolgen mit NULL-Terminierung oder Längenzählung (oder beides), statische oder dynamische Puffer, Zeichenfolgen mit fester Länge oder fast unbegrenzter Länge, vom Betriebssystem verwalteter Speicher (z. B. OLE BSTR) oder nicht verwaltete Zeichenfolgen usw.</span><span class="sxs-lookup"><span data-stu-id="134f4-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="134f4-p125">C/C++-Programmierer kennen sich am besten mit Zeichenfolgen aus, die auf NULL enden. Die standardmäßige C-Bibliothek wurde für derartige Zeichenfolgen entwickelt. Statische Zeichenfolgenliterale im Code werden Zeichenfolgen kompiliert, die auf NULL enden. Alternativ können in Excel Zeichenfolgen verwendet werden, die im Allgemeinen nicht auf NULL enden. Die Kombination dieser Fakten erfordert einen klaren und konsistenten Ansatz innerhalb Ihrer DLL/XLL im Hinblick auf die Behandlung von Zeichenfolgen und Zeichenfolgenspeicher.</span><span class="sxs-lookup"><span data-stu-id="134f4-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="134f4-226">Die häufigsten Probleme sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="134f4-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="134f4-227">Die Übergabe eines NULL-Zeigers oder eines ungültigen Zeigers an eine Funktion, die einen gültigen Zeiger erwartet und die die Gültigkeit des Zeigers nicht selbst überprüft bzw. überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="134f4-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="134f4-228">Das Überschreiten der Grenzen eines Zeichenfolgenpuffers durch eine Funktion, die die Länge des Puffers nicht gegen die Länge der geschriebenen Zeichenfolge überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="134f4-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="134f4-229">Der Versuch, Zeichenfolgenpufferspeicher freizugeben, der statisch ist oder bereits freigegeben wurde oder der auf eine Weise zugewiesen wurde, die nicht mit der Art und Weise konsistent ist, in der er freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="134f4-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="134f4-230">Speicherverluste, die daraus resultieren, dass Zeichenfolgen zugewiesen und dann nicht freigegeben werden, in der Regel in einer häufig aufgerufenen Funktion.</span><span class="sxs-lookup"><span data-stu-id="134f4-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="134f4-231">Regeln für Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="134f4-231">Rules for Strings</span></span>

<span data-ttu-id="134f4-232">Wie bei **XLOPER**/ **XLOPER** s gibt es Regeln und Richtlinien, die Sie beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="134f4-232">As with **XLOPER**/ **XLOPER** s, there are rules and guidelines you should follow.</span></span> <span data-ttu-id="134f4-233">Die Richtlinien sind identisch mit denen im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="134f4-233">The guidelines are the same as given in the previous section.</span></span> <span data-ttu-id="134f4-234">Die folgenden Regeln sind eine Erweiterung der Regeln, die speziell für Zeichenfolgen gelten.</span><span class="sxs-lookup"><span data-stu-id="134f4-234">The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="134f4-235">**Regeln:**</span><span class="sxs-lookup"><span data-stu-id="134f4-235">**Rules:**</span></span>
  
- <span data-ttu-id="134f4-236">Versuchen Sie nicht, Speicher freizugeben oder Zeichenfolgen-**XLOPER**/ **XLOPER12** s bzw. einfache Zeichenfolgen mit Längenzählung oder NULL-Terminierung zu überschreiben, die als Argumente an Ihre XLL-Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-236">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12** s or simple length-counted or null-terminated strings passed as arguments to your XLL function.</span></span> <span data-ttu-id="134f4-237">Sie sollten diese Argumente als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="134f4-237">You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="134f4-238">Wenn Excel Speicher für ein Zeichenfolgen-**XLOPER**/ **XLOPER12** für den Rückgabewert einer C-API-Rückruffunktion zuweist, verwenden Sie **xlFree**, um diesen freizugeben, oder legen Sie **xlbitXLFree** fest, wenn Sie ihn aus einer XLL-Funktion an Excel zurückgeben möchten.</span><span class="sxs-lookup"><span data-stu-id="134f4-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="134f4-239">Wenn die DLL einen Zeichenfolgenpuffer dynamisch für ein **XLOPER**/ **XLOPER12** zuweist, geben Sie diesen auf eine Art und Weise frei, die damit konsistent ist, wie er nach Abschluss zugewiesen wurde, oder legen Sie **xlbitDLLFree** fest, wenn Sie ihn aus einer XLL-Funktion an Excel zurückgeben möchten, und geben Sie ihn dann in **xlAutoFree**/ **xlAutoFree12** frei.</span><span class="sxs-lookup"><span data-stu-id="134f4-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="134f4-240">Wenn Excel Speicher für ein **xltypeMulti**-Array zugewiesen hat, der in einem Aufruf der C-API an Ihre DLL zurückgegeben wird, überschreiben Sie keine Zeichenfolgen-**XLOPER**/ **XLOPER12** s innerhalb des Arrays.</span><span class="sxs-lookup"><span data-stu-id="134f4-240">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12** s within the array.</span></span> <span data-ttu-id="134f4-241">Solche Arrays dürfen nur mithilfe von **xlFree** freigegeben werden, oder durch Festlegen von **xlbitXLFree**, wenn sie von einer XLL-Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-241">Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="134f4-242">Unterstützte Zeichenfolgentypen</span><span class="sxs-lookup"><span data-stu-id="134f4-242">String Types Supported</span></span>

<span data-ttu-id="134f4-243">**xltypeStr XLOPER/XLOPER12s von C-API**</span><span class="sxs-lookup"><span data-stu-id="134f4-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="134f4-244">\*\*Bytezeichenfolgen: \*\*XLOPER\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="134f4-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="134f4-245">\*\*Zeichenfolgen für Breitzeichen: \*\* XLOPER12\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="134f4-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="134f4-246">Alle Versionen von Excel</span><span class="sxs-lookup"><span data-stu-id="134f4-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="134f4-247">Ab Excel 2007</span><span class="sxs-lookup"><span data-stu-id="134f4-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="134f4-248">Maximale Länge: 255 erweiterte ASCII-Bytes</span><span class="sxs-lookup"><span data-stu-id="134f4-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="134f4-249">Maximale Länge 32.767 Unicode-Zeichen</span><span class="sxs-lookup"><span data-stu-id="134f4-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="134f4-250">Erstes Byte (nicht signiert) = Länge</span><span class="sxs-lookup"><span data-stu-id="134f4-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="134f4-251">Erstes Unicode-Zeichen = Länge</span><span class="sxs-lookup"><span data-stu-id="134f4-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="134f4-252">Gehen Sie nicht davon aus, dass **XLOPER**- oder **XLOPER12**-Zeichenfolgen auf NULL enden.</span><span class="sxs-lookup"><span data-stu-id="134f4-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="134f4-253">**C/C++-Zeichenfolgen**</span><span class="sxs-lookup"><span data-stu-id="134f4-253">**C/C++ strings**</span></span>

|<span data-ttu-id="134f4-254">**Bytezeichenfolgen**</span><span class="sxs-lookup"><span data-stu-id="134f4-254">**Byte strings**</span></span>|<span data-ttu-id="134f4-255">**Zeichenfolgen für Breitzeichen**</span><span class="sxs-lookup"><span data-stu-id="134f4-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="134f4-256">Null-Terminierung (**Zeichen** \*) "C" Maximale Länge: 255 erweiterte ASCII-Bytes</span><span class="sxs-lookup"><span data-stu-id="134f4-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="134f4-257">Null-Terminierung (**wchar_t** \*) "C%" Maximale Länge 32.767 Unicode-Zeichen</span><span class="sxs-lookup"><span data-stu-id="134f4-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="134f4-258">Längenzählung (**nicht signiertes Zeichen** \*) "D"</span><span class="sxs-lookup"><span data-stu-id="134f4-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="134f4-259">Längenzählung (**wchar_t** \*) "D%"</span><span class="sxs-lookup"><span data-stu-id="134f4-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="134f4-260">Zeichenfolgen in xltypeMulti XLOPER/XLOPER12-Arrays</span><span class="sxs-lookup"><span data-stu-id="134f4-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="134f4-261">In vielen Fällen erstellt Excel ein **xltypeMulti**-Array zur Verwendung in Ihrer DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="134f4-261">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL.</span></span> <span data-ttu-id="134f4-262">Einige der XLM-Informationsfunktionen geben solche Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="134f4-262">Several of the XLM information functions return such arrays.</span></span> <span data-ttu-id="134f4-263">Die C-API-Funktion **xlfGetWorkspace** gibt beispielsweise ein Array mit Zeichenfolgen zurück, die alle die derzeit registrierten DLL-Prozeduren beschreiben, wenn das Argument *44* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="134f4-263">For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures.</span></span> <span data-ttu-id="134f4-264">Die C-API-Funktion **xlfDialogBox** gibt eine geänderte Kopie ihres Arrayarguments zurück, das tiefe Kopien der Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="134f4-264">The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings.</span></span> <span data-ttu-id="134f4-265">Am häufigsten trifft eine XLL auf ein **xltypeMulti**-Array, wo ein Argument an eine XLL-Funktion übergeben wurde, oder dieser Typ wurde ihr von einem Bereichsbezug aufgezwungen.</span><span class="sxs-lookup"><span data-stu-id="134f4-265">Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference.</span></span> <span data-ttu-id="134f4-266">In diesen Fällen erstellt Excel tiefe Kopien der Zeichenfolgen in den Quellzellen und zeigt innerhalb des Arrays auf diese.</span><span class="sxs-lookup"><span data-stu-id="134f4-266">In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="134f4-267">Wenn Sie diese Zeichenfolgen in Ihrer DLL ändern möchten, sollten Sie Ihre eigenen tiefen Kopien erstellen.</span><span class="sxs-lookup"><span data-stu-id="134f4-267">Where you want to modify these strings in your DLL, you should make your own deep copies.</span></span> <span data-ttu-id="134f4-268">Wenn Sie eigene **xltypeMulti**-Arrays erstellen, platzieren Sie keine von Excel zugewiesenen Zeichenfolgen-**XLOPER**/ **XLOPER12** s darin.</span><span class="sxs-lookup"><span data-stu-id="134f4-268">When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12** s within them.</span></span> <span data-ttu-id="134f4-269">Auf diese Weise besteht das Risiko, dass Sie sie später nicht korrekt oder gar nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-269">This risks you not freeing them correctly later, or not freeing them at all.</span></span> <span data-ttu-id="134f4-270">Sie sollten erneut tiefe Kopien der Zeichenfolgen erstellen und Zeiger auf die Kopien im Array speichern.</span><span class="sxs-lookup"><span data-stu-id="134f4-270">Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="134f4-271">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="134f4-271">**Examples**</span></span>
  
<span data-ttu-id="134f4-272">Die folgende Beispielfunktion erstellt eine dynamisch zugewiesene Kopie einer Unicode-Länge mit Längenbeschränkung.</span><span class="sxs-lookup"><span data-stu-id="134f4-272">The following example function creates a dynamically allocated copy of a length-counted Unicode string.</span></span> <span data-ttu-id="134f4-273">Beachten Sie, dass der Aufrufer letztendlich den in diesem Beispiel zugewiesenen Speicher mithilfe von **delete**[] freigeben muss und dass für die Quellzeichenfolge keine Null-Terminierung angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="134f4-273">Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated.</span></span> <span data-ttu-id="134f4-274">Die kopierte Zeichenfolge wird aus Sicherheitsgründen abgeschnitten und endet nicht auf NULL.</span><span class="sxs-lookup"><span data-stu-id="134f4-274">The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="134f4-275">Diese Funktion kann dann sicher zum Kopieren einer **XLOPER12** verwendet werden, wie in der folgenden exportierbaren XLL-Funktion dargestellt, die eine Kopie ihrer Argumente zurückgibt, wenn es sich um eine Zeichenfolge handelt.</span><span class="sxs-lookup"><span data-stu-id="134f4-275">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string.</span></span> <span data-ttu-id="134f4-276">Alle anderen Typen werden als eine Zeichenfolge der Länge Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="134f4-276">All other types are returned as a zero-length string.</span></span> <span data-ttu-id="134f4-277">Beachten Sie, dass Bereiche nicht verarbeitet werden, die Funktion gibt **#VALUE!** zurück.</span><span class="sxs-lookup"><span data-stu-id="134f4-277">Note that ranges are not handled—the function returns **#VALUE!**.</span></span> <span data-ttu-id="134f4-278">Die Funktion muss so registriert werden, dass sie ein Argument vom Typ U verwendet, damit Verweise als Werte übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-278">The function must be registered as taking a type U argument so that references are passed in as values.</span></span> <span data-ttu-id="134f4-279">Dies entspricht der integrierten Arbeitsblattfunktion **T()**, mit der Ausnahme, dass **AsText** auch Fehler in leere Zeichenfolgen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="134f4-279">This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings.</span></span> <span data-ttu-id="134f4-280">In diesem Codebeispiel wird vorausgesetzt, dass **xlAutoFree12** den übergebenen Zeiger und auch dessen Inhalt mithilfe von **delete** freigibt.</span><span class="sxs-lookup"><span data-stu-id="134f4-280">This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="134f4-281">Zurückgeben von Modify-in-Place-Zeichenfolgenargumenten</span><span class="sxs-lookup"><span data-stu-id="134f4-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="134f4-282">Argumente, die als die Typen **F**, **G**, **F%** und **G%** registriert sind, können direkt bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-282">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place.</span></span> <span data-ttu-id="134f4-283">Wenn Excel Zeichenfolgenargumente für diese Typen vorbereitet, wird ein Puffer mit maximaler Länge erstellt.</span><span class="sxs-lookup"><span data-stu-id="134f4-283">When Excel is preparing string arguments for these types, it creates a maximum length buffer.</span></span> <span data-ttu-id="134f4-284">Dann wir die Argumentzeichenfolge in den Puffer kopiert, auch wenn diese Zeichenfolge viel kürzer ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-284">Then it copies the argument string into that, even if this string is very much shorter.</span></span> <span data-ttu-id="134f4-285">Auf diese Weise kann die XLL- ihren Rückgabewert direkt in den gleichen Speicher schreiben.</span><span class="sxs-lookup"><span data-stu-id="134f4-285">This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="134f4-286">Die Puffergößen für diese Typen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="134f4-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="134f4-287">**Bytezeichenfolgen:** 256 Bytes, einschließlich der Längenzählung (Typ G) oder Null-Terminierung (Typ F).</span><span class="sxs-lookup"><span data-stu-id="134f4-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="134f4-288">**Unicode-Zeichenfolgen:** 32.768 Breitzeichen (65.536 Bytes), einschließlich der Längenzählung (Typ G%) oder Null-Terminierung (Typ F%).</span><span class="sxs-lookup"><span data-stu-id="134f4-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="134f4-p134">Sie können eine solche Funktion nicht direkt aus VBA (Visual Basic für Applikationen) aufrufen, da Sie nicht sicherstellen können, dass ein ausreichend großer Puffer zugewiesen wurde. Sie können eine solche Funktion nur aus einer anderen DLL sicher aufrufen, wenn Sie explizit einen ausreichend großen Puffer übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="134f4-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="134f4-291">Nachfolgend sehen Sie ein Beispiel für eine XLL-Funktion, die ein übergebenes, auf NULL endendes Breitzeichen mithilfe der standardmäßigen Bibliotheksfunktion **wcsrev** reserviert.</span><span class="sxs-lookup"><span data-stu-id="134f4-291">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**.</span></span> <span data-ttu-id="134f4-292">Das Argument würde in diesem Fall als Typ **F%** registriert.</span><span class="sxs-lookup"><span data-stu-id="134f4-292">The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="134f4-293">Beständiger Speicher (binäre Namen)</span><span class="sxs-lookup"><span data-stu-id="134f4-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="134f4-294">Binäre Namen werden mit Blöcken von Binärdaten definiert und zugeordnet, d. h., unstrukturierte Daten, die zusammen mit der Arbeitsmappe gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="134f4-295">Sie werden mit der Funktion [xlDefineBinaryName](xldefinebinaryname.md) erstellt, und die Daten werden mit der Funktion [xlGetBinaryName](xlgetbinaryname.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="134f4-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="134f4-296">Beide Funktionen werden in der Funktionsreferenz ausführlicher beschrieben (siehe [C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), und beide verwenden **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="134f4-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="134f4-297">Weitere Informationen zu bekannten Problemen, durch die die praktischen Anwendungen von binären Namen eingeschränkt werden, finden Sie unter [Bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="134f4-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="134f4-298">Excel-Stapel</span><span class="sxs-lookup"><span data-stu-id="134f4-298">Excel Stack</span></span>

<span data-ttu-id="134f4-p137">Excel gibt seinen Stapelspeicher für alle geladenen DLLs frei. Der Stapelspeicher ist in der Regel für die einfache Verwendung mehr als ausreichend, und Sie müssen sich keine Gedanken darüber machen, solange Sie ein paar Richtlinien befolgen: </span><span class="sxs-lookup"><span data-stu-id="134f4-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="134f4-p138">Übergeben Sie nicht sehr große Strukturen als Argumente an Funktionen nach dem Wert in dem Stapel. Übergeben Sie stattdessen Zeiger oder Verweise.</span><span class="sxs-lookup"><span data-stu-id="134f4-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="134f4-p139">Geben Sie keine große Strukturen an den Stapel zurück. Geben Sie Zeiger an statisch oder dynamisch zugewiesenen Speicher zurück, oder verwenden Sie Argumente, die als Verweis übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="134f4-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="134f4-p140">Deklarieren Sie keine sehr großen automatischen Variablenstrukturen im Funktionscode. Deklarieren Sie sie ggf. als statisch.</span><span class="sxs-lookup"><span data-stu-id="134f4-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="134f4-p141">Rufen Sie Funktionen nicht rekursiv auf, es sei denn, Sie sind sicher, dass die Rekursionstiefe immer flach ist. Versuchen Sie es stattdessen mit einer Schleife.</span><span class="sxs-lookup"><span data-stu-id="134f4-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="134f4-309">Wenn eine DLL-Datei einen Rückruf in Excel mithilfe der C-API unternimmt, überprüft Excel zuerst, ob genügend Speicherplatz auf dem Stapel für den Aufruf mit der größten Nutzung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="134f4-309">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made.</span></span> <span data-ttu-id="134f4-310">Wenn Excel denkt, dass möglicherweise nicht genügend Platz vorhanden ist tritt ein Fehler bei dem Aufruf auf, auch wenn möglicherweise ausreichend Speicherplatz für diesen bestimmten Anruf vorhanden gewesen wäre.</span><span class="sxs-lookup"><span data-stu-id="134f4-310">If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call.</span></span> <span data-ttu-id="134f4-311">In diesem Fall gibt der Rückruf den Code **xlretFailed** zurück.</span><span class="sxs-lookup"><span data-stu-id="134f4-311">In this case, the callbacks return the code **xlretFailed**.</span></span> <span data-ttu-id="134f4-312">Für eine normale Verwendung der C-API und des Stapels ist dies eine unwahrscheinliche Ursache für den Fehler eines C-API-Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="134f4-312">For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="134f4-313">Wenn Sie sich Sorgen über den Stapelspeicher machen oder einfach nur neugierig sind oder vielleicht den mangelnden Stapelspeicher als Ursache für einen unerklärlichen Fehler beheben möchten, können Sie herausfinden, wie viel Stapelspeicher vorhanden ist, indem Sie die Funktion [xlStack](xlstack.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="134f4-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="134f4-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="134f4-314">See also</span></span>



[<span data-ttu-id="134f4-315">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="134f4-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="134f4-316">Multithreading und Speicherkonflikte in Excel</span><span class="sxs-lookup"><span data-stu-id="134f4-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="134f4-317">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="134f4-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

