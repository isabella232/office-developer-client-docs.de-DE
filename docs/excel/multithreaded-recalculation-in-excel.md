---
title: Multithreaded neuberechnung in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790556"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="32097-104">Multithreaded neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="32097-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="32097-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="32097-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="32097-p101">Microsoft Office Excel 2007 war die erste Version von Excel, in der die Multithread-Neuberechnung (MTR) für Arbeitsblätter verwendet wurde. Sie können Excel für die Verwendung von bis zu 1.024 gleichzeitigen Threads bei der Neuberechnung konfigurieren, ungefähre von der Anzahl von Prozessoren oder Prozessorkernen auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="32097-p101">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets. You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32097-108">Da mit jedem Thread ein Betriebssystemmehraufwand verbunden ist, sollten Sie Excel nicht für die Verwendung von mehr Threads als erforderlich konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="32097-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="32097-109">Wenn der Computer über mehrere Prozessoren oder Prozessorkerne verfügt, übernimmt das Betriebssystem die Verantwortung für die effizienteste Zuweisung von Threads zu den Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="32097-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="32097-110">Übersicht über die Excel MTR</span><span class="sxs-lookup"><span data-stu-id="32097-110">Excel MTR overview</span></span>

<span data-ttu-id="32097-p102">Excel versucht, die Teile der Berechnungskette zu identifizieren, die in verschiedenen Threads gleichzeitig neu berechnet werden können. Die folgende sehr einfache Struktur (bei der x ? y bedeutet, dass y nur von x abhängt) zeigt ein Beispiel dafür.</span><span class="sxs-lookup"><span data-stu-id="32097-p102">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads. The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="32097-113">**Abbildung 1: Gleichzeitiges Berechnen in verschiedenen Threads**</span><span class="sxs-lookup"><span data-stu-id="32097-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="32097-114">![Berechnung der gleichzeitig auf verschiedenen threads] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Berechnung der gleichzeitig auf verschiedenen threads")</span><span class="sxs-lookup"><span data-stu-id="32097-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="32097-115">Nachdem A1 berechnet ist, können A2 und dann A3 in einem Thread berechnet werden, w�hrend B1 und dann C1 in einem anderen Thread berechnet werden, vorausgesetzt, dass alle Zellen threadsicher sind.</span><span class="sxs-lookup"><span data-stu-id="32097-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32097-p103">Der Begriff threadsichere Zelle bedeutet, dass eine Zelle nur threadsichere Funktionen enthält. Was und was nicht threadsicher ist, wird ausführlich [Was von Excel als threadsicher betrachtet wird und was nicht](#xl2007xllsdk_threadsafe) erl�utert.</span><span class="sxs-lookup"><span data-stu-id="32097-p103">The term thread-safe cell means a cell that only contains thread-safe functions. What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="32097-p104">Die meisten praktischen Arbeitsmappen enthalten viel komplexere Abhängigkeitsstrukturen als dieses Beispiel. Darüber hinaus ist die Neuberechnungszeit einer Zelle erst bekannt, wenn eine Berechnung abgeschlossen ist und kann je nach Argumenten der Funktion stark variieren. Für optimale Ergebnisse versucht Excel, die Berechnungsreihenfolge für jede Berechnung zu optimieren, bis keine weitere Optimierung möglich ist.</span><span class="sxs-lookup"><span data-stu-id="32097-p104">Most practical workbooks contain far more complex dependency trees than this example. Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments. To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="32097-121">Excel verwendet einen einzelnen Hauptthread, um Folgendes auszuführen:</span><span class="sxs-lookup"><span data-stu-id="32097-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="32097-122">Integrierte Befehle</span><span class="sxs-lookup"><span data-stu-id="32097-122">Built-in commands</span></span>
    
- <span data-ttu-id="32097-123">XLL-Befehle</span><span class="sxs-lookup"><span data-stu-id="32097-123">XLL commands</span></span>
    
- <span data-ttu-id="32097-124">XLL-Add-in-Manager-Schnittstellenfunktionen (**XlAutoOpen** Funktion usw.)</span><span class="sxs-lookup"><span data-stu-id="32097-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="32097-125">Benutzerdefinierte Befehle von Microsoft Visual Basic for Applications (VBA) (oft als Makros bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="32097-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="32097-126">Benutzerdefinierte VBA-Funktionen</span><span class="sxs-lookup"><span data-stu-id="32097-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="32097-127">Integrierte threadunsichere Arbeitsblattfunktionen (eine Liste finden Sie im nächstem Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="32097-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="32097-128">Benutzerdefinierte XLM-Makroarbeitsblattbefehle und -funktionen</span><span class="sxs-lookup"><span data-stu-id="32097-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="32097-129">COM-Add-In-Befehle und -Funktionen</span><span class="sxs-lookup"><span data-stu-id="32097-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="32097-130">Funktionen und Operatoren in Ausdrücken für bedingte Formatierung</span><span class="sxs-lookup"><span data-stu-id="32097-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="32097-131">Funktionen und Operatoren in definierten Namensdefinitionen, die in Arbeitsblattformeln verwendet werden</span><span class="sxs-lookup"><span data-stu-id="32097-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="32097-132">Die erzwungene Auswertung eines Ausdrucks im Feld für die Formelbearbeitung mithilfe der **F9** -TASTE</span><span class="sxs-lookup"><span data-stu-id="32097-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="32097-p105">Alle Arbeitsblattformeln, ungefähre davon, ob die Funktionen threadsicher sind oder nicht, werden im Hauptthread ausgewertet, es sei denn, Excel ist für die Verwendung von mehr als einem Thread konfiguriert. Wenn der Benutzer angibt, dass mehrere Threads verwendet werden sollen, werden die zusätzlichen Threads für threadsichere Zellen verwendet. Beachten Sie, dass der Hauptthread möglicherweise weiterhin für threadsichere Zellen verwendet wird, wenn dies aus Sicht des Lastenausgleichs sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="32097-p105">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread. When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells. Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="32097-136">Es lohnt sich, erneut zu erw�hnen, dass Excel nicht mehr als einen Befehl gleichzeitig ausführt, daher müssen Sie nicht dieselben Vorsichtsmaßnahmen wie beim Schreiben von threadsicheren Funktionen anwenden, z. B. die Verwendung von threadlokalem Speicher und kritischen Bereichen.</span><span class="sxs-lookup"><span data-stu-id="32097-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="32097-137">Was ist und nicht als Thread sicherer von Excel</span><span class="sxs-lookup"><span data-stu-id="32097-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="32097-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="32097-138"></span></span>

<span data-ttu-id="32097-139">Excel betrachtet nur Folgendes als threadsicher:</span><span class="sxs-lookup"><span data-stu-id="32097-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="32097-140">Alle un�ren und binären Operatoren in Excel</span><span class="sxs-lookup"><span data-stu-id="32097-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="32097-141">Nahezu alle integrierten Arbeitsblattfunktionen beginnend in Excel 2007 (siehe Ausnahmenliste)</span><span class="sxs-lookup"><span data-stu-id="32097-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="32097-142">XLL-Add-In-Funktionen, die ausdrücklich als threadsicher registriert wurden</span><span class="sxs-lookup"><span data-stu-id="32097-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="32097-143">Die folgenden integrierten Arbeitsblattfunktionen sind nicht threadsicher:</span><span class="sxs-lookup"><span data-stu-id="32097-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="32097-144">**PHONETIC**</span><span class="sxs-lookup"><span data-stu-id="32097-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="32097-145">**CELL**, wenn das Argument �format" oder �address" verwendet wird</span><span class="sxs-lookup"><span data-stu-id="32097-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="32097-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="32097-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="32097-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="32097-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="32097-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="32097-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="32097-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="32097-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="32097-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="32097-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="32097-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="32097-151">**CUBESET**</span></span>
    
- <span data-ttu-id="32097-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="32097-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="32097-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="32097-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="32097-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="32097-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="32097-155">**ADDRESS**, wenn der fünfte Parameter (sheet_name) vorgegeben ist</span><span class="sxs-lookup"><span data-stu-id="32097-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="32097-156">Jede Datenbankfunktion (**DSUM**, **DAVERAGE**usw.), die auf eine Pivot-Tabelle verweist</span><span class="sxs-lookup"><span data-stu-id="32097-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="32097-157">**FEHLER. TYP**</span><span class="sxs-lookup"><span data-stu-id="32097-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="32097-158">**HYPERLINK**</span><span class="sxs-lookup"><span data-stu-id="32097-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="32097-159">Die folgenden Funktionen werden ausdrücklich als unsicher betrachtet:</span><span class="sxs-lookup"><span data-stu-id="32097-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="32097-160">Benutzerdefinierte VBA-Funktionen</span><span class="sxs-lookup"><span data-stu-id="32097-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="32097-161">Benutzerdefinierte COM-Add-In-Funktionen</span><span class="sxs-lookup"><span data-stu-id="32097-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="32097-162">Benutzerdefinierte XLM-Makroarbeitsblattfunktionen</span><span class="sxs-lookup"><span data-stu-id="32097-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="32097-163">XLL-Add-In-Funktionen, die nicht ausdrücklich als threadsicher registriert sind</span><span class="sxs-lookup"><span data-stu-id="32097-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="32097-164">Die Auswirkung ist, dass die folgenden Vorgänge und Funktionen nicht threadsicher sind und ein Fehler auftritt, wenn sie von einer XLL-Funktion aufgerufen werden, die als threadsicher registriert ist:</span><span class="sxs-lookup"><span data-stu-id="32097-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="32097-165">Anrufe an Informationen XLM-Funktionen, beispielsweise **XlfGetCell** (**GET. Zelle**).</span><span class="sxs-lookup"><span data-stu-id="32097-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="32097-166">Anrufe an **XlfSetName** (**SET.NAME**) und Löschen von XLL-interne Namen definieren.</span><span class="sxs-lookup"><span data-stu-id="32097-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="32097-167">Aufrufe an threadunsichere benutzerdefinierte Funktionen über **xlUDF**</span><span class="sxs-lookup"><span data-stu-id="32097-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="32097-168">Aufrufe an die Funktion [xlfEvaluate](xlfevaluate.md) für Ausdr�cke, die threadunsichere Funktionen oder definierte Namen enthalten, deren Definitionen threadunsichere Funktionen enthalten</span><span class="sxs-lookup"><span data-stu-id="32097-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="32097-169">Aufrufe an die Funktion [xlAbort](xlabort.md) zum Löschen einer Unterbrechungsbedingung</span><span class="sxs-lookup"><span data-stu-id="32097-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="32097-170">Aufrufe an die Funktion [xlCoerce](xlcoerce.md) zum Abrufen des Werts eines nicht berechneten Zellenbezugs</span><span class="sxs-lookup"><span data-stu-id="32097-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="32097-171">XLL-Arbeitsblattfunktionen dürfen keine C-API-Befehle wie **xlcSave** aufrufen, ungefähre davon, ob diese als threadsicher registriert wurden oder nicht.</span><span class="sxs-lookup"><span data-stu-id="32097-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="32097-p106">Angesichts der Tatsache, dass XLL-Funktionen, die als threadsicher deklariert sind, weder XLM-Informationsfunktionen aufrufen noch auf nicht berechnete Zellen verweisen können, lässt Excel nicht zu, dass XLL-Funktionen, die als Makroarbeitsblattentsprechungen registriert sind, auch als threadsicher registriert werden können. Daher führt der Versuch, den Wert eines nicht berechneten Zellenbezugs mithilfe von **xlCoerce** zu einem **xlretUncalced**-Fehler. Das Aufrufen einer XLM-Informationsfunktion führt zu einem **xlretFailed**-Fehler. Die anderen zuvor aufgeführten Funktionen führen zu einem in der Excel-C-API eingeführten Fehlercode: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="32097-p106">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe. Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error. Calling an XLM information function fails with an **xlretFailed** error. The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="32097-176">Die reinen C-API-Rückruffunktionen sind alle threadsicher:</span><span class="sxs-lookup"><span data-stu-id="32097-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="32097-177">**xlCoerce** (außer wenn dennoch ein Fehler bei der Koersion nicht berechneter Zellenbezüge auftritt)</span><span class="sxs-lookup"><span data-stu-id="32097-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="32097-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="32097-178">**xlFree**</span></span>
    
- <span data-ttu-id="32097-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="32097-179">**xlStack**</span></span>
    
- <span data-ttu-id="32097-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="32097-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="32097-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="32097-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="32097-182">**xlAbort** (außer bei Verwendung zum Löschen einer Unterbrechungsbedingung)</span><span class="sxs-lookup"><span data-stu-id="32097-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="32097-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="32097-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="32097-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="32097-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="32097-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="32097-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="32097-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="32097-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="32097-187">Die einzige Ausnahme ist die Funktion **xlSet**, die in jedem Fall eine Befehlsentsprechung ist und daher von keiner Arbeitsblattfunktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="32097-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="32097-p107">Eine XLL-Arbeitsblattfunktion kann bei Excel als threadsicher registriert werden. Dadurch wird Excel angewiesen, dass die Funktion sicher und gleichzeitig in mehreren Threads aufgerufen werden kann, Sie müssen jedoch sicherstellen, dass dies wirklich der Fall ist. Excel wird möglicherweise destabilisiert, wenn eine als threadsicher registrierte Funktion sich dann unsicher verhält.</span><span class="sxs-lookup"><span data-stu-id="32097-p107">An XLL worksheet function can be registered with Excel as thread safe. This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case. You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="32097-191">Registrieren von XLL-Funktionen als threadsicheren</span><span class="sxs-lookup"><span data-stu-id="32097-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="32097-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="32097-192"></span></span>

<span data-ttu-id="32097-193">Folgende Regeln muss ein Entwickler beim Schreiben threadsicherer Funktionen beachten:</span><span class="sxs-lookup"><span data-stu-id="32097-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="32097-194">Rufen Sie Ressourcen nicht in anderen DLLs auf, die möglicherweise nicht threadsicher sind.</span><span class="sxs-lookup"><span data-stu-id="32097-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="32097-195">F�hren Sie keine threadunsicheren Aufrufe über die C-API oder COM durch.</span><span class="sxs-lookup"><span data-stu-id="32097-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="32097-196">Sch�tzen Sie Ressourcen, die gleichzeitig von mehreren Threads werden können, mithilfe von kritischen Bereichen.</span><span class="sxs-lookup"><span data-stu-id="32097-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="32097-197">Verwenden Sie threadlokalen Speicher als threadspezifischen Speicher, und ersetzen Sie statische Variablen in Funktionen durch threadlokale Variablen.</span><span class="sxs-lookup"><span data-stu-id="32097-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="32097-198">Excel legt eine weitere Einschränkung auf: Threadsichere Funktionen können nicht als Makrovorlagenentsprechungen registriert werden und deshalb weder XLM-Informationsfunktionen aufrufen noch die Werte nicht neu berechneter Zellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="32097-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="32097-199">Arbeitsspeicher Konflikte</span><span class="sxs-lookup"><span data-stu-id="32097-199">Memory contention</span></span>
<span data-ttu-id="32097-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="32097-200"></span></span>

<span data-ttu-id="32097-201">Multithread-Systeme müssen zwei wichtige Probleme berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="32097-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="32097-202">Wie Speicher geschützt werden kann, aus dem von mehr als einem Thread gelesen bzw. an den von mehr als einem Thread geschrieben wird</span><span class="sxs-lookup"><span data-stu-id="32097-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="32097-203">Wie die Erstellung von und der Zugriff auf Speicher erfolgen soll, der dem ausführenden Thread zugeordnet und deshalb für diesen privat ist</span><span class="sxs-lookup"><span data-stu-id="32097-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="32097-p108">Das Windows-Betriebssystem und das Windows Software Development Kit (SDK) bieten Tools für beide F�lle: kritische Bereiche und die threadlokale Speicher-API (TLS-API). Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="32097-p108">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="32097-p109">Das erste Problem kann beispielsweise auftreten, wenn zwei Tabellenfunktionen (oder zwei gleichzeitig ausgeführte Instanzen derselben Funktion) auf eine globale Variable in einem DLL-Projekt zugreifen oder diese �ndern müssen. Denken Sie daran, dass eine solche globale Variable möglicherweise in einer global zugänglichen Instanz eines Klassenobjekts verborgen ist.</span><span class="sxs-lookup"><span data-stu-id="32097-p109">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project. Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="32097-p110">Das zweite Problem kann z. B. auftreten, wenn eine Tabellenfunktion eine statische Variable oder ein Objekt innerhalb des Funktionsrumpfcodes deklariert. Der C/C++-Compiler erstellt nur eine einzelne Kopie, die von allen Threads verwendet wird. Das bedeutet, dass eine Instanz der Funktion den Wert �ndern könnte, w�hrend eine andere in einem anderen Thread möglicherweise davon ausgeht, dass der Wert dem entspricht, was sie zuvor festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="32097-p110">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code. The C/C++ compiler only creates a single copy that all threads use. This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="32097-211">Beispiel-Clientanwendungen von MTR</span><span class="sxs-lookup"><span data-stu-id="32097-211">Example applications of MTR</span></span>
<span data-ttu-id="32097-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="32097-212"></span></span>

<span data-ttu-id="32097-p111">Alle XXLs, die Tabellenfunktionen exportieren, können die Multithread-Neuberechnung (MTR) in Excel nutzen, vorausgesetzt, dass diese Funktionen keine threadunsicheren Aktionen durchführen müssen. Damit kann Excel Arbeitsmappen, die von diesen abh�ngen, so schnell wie möglich neu berechnen, was ungefähre von der Anwendung w�nschenswert ist.</span><span class="sxs-lookup"><span data-stu-id="32097-p111">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions. This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="32097-p112">MTR hat insbesondere eine enorme Auswirkung auf die Neuberechnungszeit für Arbeitsmappen, die benutzerdefinierte Funktionen (User-Defined Functions, UDFs) aufrufen, die wiederum selbst externe Prozesse aufrufen, um das gewünschte Ergebnis abzurufen. Denken Sie insbesondere an eine UDF, die einen Remoteserver aufruft, der viele Anforderungen gleichzeitig verarbeiten kann, und eine Arbeitsmappe, die viele Aufrufe an diese Funktion enthält. Wenn eine Singlethread-Neuberechnung der Arbeitsmappe erfolgt, muss jeder Aufruf an die UDF, und damit an den Remoteserver, abgeschlossen werden, bevor der nächste erfolgen kann. Damit wird die Fähigkeit des Servers aufgehoben, viele Aufrufe auf einmal zu verarbeiten. Bei einer Multithread-Neuberechnung der Arbeitsmappe kann Excel mehrere Aufrufe gleichzeitig oder in schneller Folge durchführen.</span><span class="sxs-lookup"><span data-stu-id="32097-p112">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result. In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function. If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made. This wastes the server's ability to process many calls at once. If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="32097-p113">Wenn Excel für die Verwendung derselben Anzahl von Threads wie der Server konfiguriert ist � nennen wir es N � und die Topologie der Abhängigkeitsstruktur der Arbeitsmappe es zulässt, könnte die gesamte Neuberechnungszeit auf nahezu 1/N der Singlethread-Berechnungszeit verringert werden. Das trifft möglicherweise sogar zu, wenn der Clientcomputer (auf dem die Arbeitsmappe ausgeführt wird) nur einen Prozessor enthält, insbesondere, wenn die Zeit für den Aufruf an den Server relativ kurz im Vergleich zu der Zeit ist, den Server zum Verarbeiten des Aufrufs benötigt.</span><span class="sxs-lookup"><span data-stu-id="32097-p113">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time. This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="32097-p114">Für jeden zusätzlichen Thread gibt es einen Betriebssystemmehraufwand. Damit ist für eine bestimmte Arbeitsmappe sowie einen bestimmten Server und Clientcomputer möglicherweise ein gewisses Experimentieren erforderlich, um die optimale Anzahl von Threads zu finden, die Excel verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="32097-p114">There is operating system overhead for each additional thread. Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="32097-p115">Betrachten Sie beispielsweise einen Computer mit einem einzigen Prozessor, auf dem Excel und eine Arbeitsmappe mit 1.000 Zellen ausgeführt werden. Es erfolgt ein Aufruf an eine UDF, die wiederum einen oder mehrere Remoteserver aufruft. Nehmen wir an, dass die 1.000 Zellen nicht voneinander abhängig sind, sodass Excel nicht darauf warten muss, dass ein Aufruf abgeschlossen ist, bevor der nächste Aufruf erfolgen kann. (Eine gewisse Lockierung dieser Einschränkung ist ohne Auswirkung auf das Beispiel möglich.) Wenn die Server 100 Anforderungen gleichzeitig verarbeiten können und Excel für die Verwendung von 100 Threads konfiguriert ist, kann die Ausführungszeit auf nur 1/100 der Zeit reduziert werden, wenn nur ein einziger Thread verwendet wird. Die Mehraufwand, der damit verbunden ist, dass Excel Aufrufe zu jedem Thread zuordnet, und die Tatsache, dass das Betriebssystem 100 Threads verwaltet, bedeuten, dass die Reduzierung in der Praxis nicht ganz so gro� ausf�llt. Hier wird außerdem ausdr�cklick angenommen, dass der Server gut skaliert ist und sich die Aufforderung, 100 Aufgaben gleichzeitig zu verarbeiten, nicht signifikant auf die Abschlusszeiten einzelner Aufgaben auswirkt.</span><span class="sxs-lookup"><span data-stu-id="32097-p115">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells. It calls a UDF, which in turn calls one or more remote servers. Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next. (Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used. The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great. There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="32097-230">Eine praktische Anwendung, in der dieses Verfahren einen wichtigen Vorteil haben kann, sind die Monte-Carlo-Methode und andere zahlenintensive Aufgaben, die in kleinere Unteraufgaben aufgeteilt werden können, die an Server vergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="32097-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="32097-231">Excel Services-Überlegungen</span><span class="sxs-lookup"><span data-stu-id="32097-231">Excel Services considerations</span></span>
<span data-ttu-id="32097-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="32097-232"></span></span>

<span data-ttu-id="32097-p116">Excel Services unterstützt das Laden, Berechnen und Rendern von Excel-Tabellen auf einem Server. Benutzer können dann über Standardbrowsertools auf die Tabellen zugreifen und mit diesen interagieren.</span><span class="sxs-lookup"><span data-stu-id="32097-p116">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server. Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="32097-p117">Excel Services-UDFs werden mithilfe von verwaltetem Microsoft .NET Framework-Code erstellt und über eine .NET-Assembly zur Verfügung gestellt. XLLs werden von Excel Services nicht unterstützt. Eine Server-UDF-Ressource mit verwaltetem Code kann eine XLL aufrufen, um auf ihre Funktionalität zuzugreifen, sodass der Benutzer mit einer auf dem Server geladenen Arbeitsmappe dieselben Funktionen hat wie mit einer auf dem Client geladenen Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="32097-p117">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly. XLLs are not supported by Excel Services. A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="32097-p118">Um die Funktionen einer XLL auf diese Weise verfügbar zu machen, müssen sie von einer .NET-Assembly umschlossen werden, die Argumente und Rückgabewerte von den systemeigenen Datentypen in die verwalteten .NET Framework-Datentypen konvertiert und die XLL-Funktionen aufruft. Der .NET-Wrapper würde jeweils eine Server-UDF für jede XLL-Funktion exportieren, auf die zugegriffen wird. Eine weitere Voraussetzung ist, dass XLL-Funktionen, die auf diese Weise aufgerufen werden, threadsicher sein müssen. Da die XLL-Funktionen nicht auf dieselbe der Weise wie beim Excel-Client registriert sind, können der Server und der .NET-Wrapper nicht erzwingen, dass sie threadsicher sind. Es liegt in der Verantwortung des XLL-Entwicklers, dies sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="32097-p118">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions. The .NET wrapper would export one server UDF for each XLL function being accessed. An additional requirement is that any XLL functions called in this way must be thread safe. Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe. It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32097-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32097-243">See also</span></span>

- [<span data-ttu-id="32097-244">Excel-Neuberechnung</span><span class="sxs-lookup"><span data-stu-id="32097-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="32097-245">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="32097-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="32097-246">Zugriff auf XLL-Code in Excel (engl.)</span><span class="sxs-lookup"><span data-stu-id="32097-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="32097-247">Excel-Programmierkonzepte</span><span class="sxs-lookup"><span data-stu-id="32097-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="32097-248">Excel XLL-SDK-API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="32097-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

