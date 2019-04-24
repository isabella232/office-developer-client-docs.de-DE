---
title: Excel-Neuberechnung
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 07deec5ad104c59074567725d6abf9b66711e351
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304116"
---
# <a name="excel-recalculation"></a><span data-ttu-id="52408-104">Excel-Neuberechnung</span><span class="sxs-lookup"><span data-stu-id="52408-104">Excel Recalculation</span></span>

<span data-ttu-id="52408-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52408-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52408-106">Eine Neuberechnung kann in Microsoft Excel auf verschiedene Weisen ausgelöst werden, beispielsweise durch folgende Aktionen:</span><span class="sxs-lookup"><span data-stu-id="52408-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="52408-107">Eingeben neuer Daten (wenn Excel sich im automatischen Neuberechnungsmodus befindet, siehe Beschreibung weiter unten in diesem Thema)</span><span class="sxs-lookup"><span data-stu-id="52408-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="52408-108">Ausgeben der expliziten Anweisung, dass Excel eine Arbeitsmappe ganz oder teilweise neu berechnen soll</span><span class="sxs-lookup"><span data-stu-id="52408-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="52408-109">Löschen oder Einfügen einer Zeile oder Spalte</span><span class="sxs-lookup"><span data-stu-id="52408-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="52408-110">Speichern einer Arbeitsmappe bei aktivierter Option **Vor dem Speichern neu berechnen**</span><span class="sxs-lookup"><span data-stu-id="52408-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="52408-111">Durchführen bestimmter Autofilter-Aktionen</span><span class="sxs-lookup"><span data-stu-id="52408-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="52408-112">Doppelklicken auf eine Zeilen- oder Spaltentrennlinie (im automatischen Berechnungsmodus)</span><span class="sxs-lookup"><span data-stu-id="52408-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="52408-113">Hinzufügen, Bearbeiten oder Löschen eines definierten Namens</span><span class="sxs-lookup"><span data-stu-id="52408-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="52408-114">Umbenennen eines Arbeitsblatts</span><span class="sxs-lookup"><span data-stu-id="52408-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="52408-115">Ändern der Position eines Arbeitsblatts in Bezug auf andere Arbeitsblätter</span><span class="sxs-lookup"><span data-stu-id="52408-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="52408-116">Ausblenden oder Einblenden von Zeilen, nicht aber Spalten</span><span class="sxs-lookup"><span data-stu-id="52408-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="52408-p101">In diesem Thema wird kein Unterschied dazwischen gemacht, ob der Benutzer direkt eine Taste drückt oder mit der Maus klickt und ob die entsprechenden Aufgaben von einem Befehl oder einem Makro ausgeführt werden. Der Benutzer führt den Befehl aus oder veranlasst die Ausführung des Befehls durch eine Aktion, sodass dies als Benutzeraktion angesehen wird. Daher bedeutet bedeutet der Ausdruck "der Benutzer": "der Benutzer oder ein vom Benutzer gestarteter Befehl oder Prozess".</span><span class="sxs-lookup"><span data-stu-id="52408-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="52408-120">Abhängigkeit, geänderte Zellen und neu berechnete Zellen</span><span class="sxs-lookup"><span data-stu-id="52408-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="52408-121">Die Berechnung von Arbeitsblättern in Excel kann als dreistufiger Prozess betrachtet werden:</span><span class="sxs-lookup"><span data-stu-id="52408-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="52408-122">Erstellen einer Abhängigkeitsstruktur</span><span class="sxs-lookup"><span data-stu-id="52408-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="52408-123">Erstellen einer Berechnungskette</span><span class="sxs-lookup"><span data-stu-id="52408-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="52408-124">Neuberechnen von Zellen</span><span class="sxs-lookup"><span data-stu-id="52408-124">Recalculation of cells</span></span>
    
<span data-ttu-id="52408-p102">Die Abhängigkeitsstruktur informiert Excel darüber, welche Zellen von anderen abhängen, bzw. welche Zellen Vorgänger von anderen sind. Aus dieser Struktur erstellt Excel eine Berechnungskette. Die Berechnungskette listet alle Zellen mit Formeln in der Reihenfolge auf, in der sie berechnet werden sollen. Während der Neuberechnung überarbeitet Excel diese Kette, wenn eine Formel gefunden wird, die von einer noch nicht berechneten Zelle abhängt. In diesem Fall werden die Zelle, die gerade berechnet wird, und die davon abhängigen Zellen in der Kette nach unten verschoben. Aus diesem Grund können Berechnungszeiten in einem Arbeitsblatt, das gerade erst geöffnet wurde, häufig in den ersten paar Berechnungszyklen verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="52408-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="52408-p103">Wenn eine Änderung an der Struktur einer Arbeitsmappe vorgenommen wird (z. B. durch Eingabe einer neuen Formel), erstellt Excel die Abhängigkeitsstruktur und die Berechnungskette neu. Wenn neue Daten oder neue Formeln eingegeben werden, markiert Excel alle Zellen, die von den neuen Daten abhängen, als Zellen, für die eine Neuberechnung erforderlich ist. Auf diese Weise markierte Zellen werden als  *geändert*  bezeichnet. Alle direkt und indirekt abhängigen Zellen werden als geändert markiert; dies bedeutet Folgendes: Wenn B1 von A1 und C1 von B1 abhängt, werden bei einer Änderung von A1 sowohl B1 als auch C1 als geändert markiert.</span><span class="sxs-lookup"><span data-stu-id="52408-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="52408-p104">Wenn eine Zelle direkt oder indirekt von sich selbst abhängt, erkennt Excel den Zirkelbezug und gibt eine Warnung aus. Dies ist normalerweise eine Fehlerbedingung, die der Benutzer beheben muss, und Excel zeigt sehr hilfreiche grafische und Navigationstools an, die den Benutzer bei der Suche nach dem Ursprung des Zirkelbezugs unterstützen. In einigen Fällen ist diese Bedingung sogar wünschenswert, z. B. wenn Sie eine iterative Berechnung durchführen möchten, bei der der Startpunkt der jeweils nächsten Iteration das Ergebnis der vorherigen Iteration ist. Excel unterstützt die Steuerung von iterativen Berechnungen über das Dialogfeld mit Berechnungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="52408-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="52408-p105">Nachdem Zellen als geändert markiert wurden, wird bei der nächsten Neuberechnung der Inhalt jeder geänderten Zelle von Excel erneut ausgewertet, und zwar in der von der Berechnungskette vorgegebenen Reihenfolge. Für das vorherige Beispiel bedeutet dies, dass zuerst B1 und dann C1 ausgewertet wird. Diese Neuberechnung findet im automatischen Neuberechnungsmodus unmittelbar nach dem Markieren der Zellen als geändert statt, andernfalls erst später.</span><span class="sxs-lookup"><span data-stu-id="52408-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="52408-p106">Ab Microsoft Excel 2002 unterstützt das **Range**-Objekt in Microsoft Visual Basic for Applications (VBA) die **Range.Dirty**-Methode, die Zellen mit der Markierung versieht, dass eine Berechung erforderlich ist. Wenn diese Methode zusammen mit der **Range.Calculate**-Methode verwendet wird (siehe nächster Abschnitt), wird die erzwungene Neuberechnung von Zellen in einem angegebenen Bereich aktiviert. Dies ist bei der Durchführung einer eingeschränkten Berechnung im manuellen Berechnungsmodus während eines Makros hilfreich, um zu vermeiden, dass unnötigerweise Zellen berechnet werden, die nicht mit der Makrofunktion in Zusammenhang stehen. Berechnungsmethoden für Bereiche stehen in der C-API nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="52408-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="52408-p107">In Excel 2002 und früheren Versionen wurde von Excel für jedes Arbeitsblatt in jeder geöffneten Arbeitsmappe eine Berechnungskette erstellt. Dies führte dazu, dass die Verarbeitung von Verknüpfungen zwischen Arbeitsblättern ziemlich kompliziert war, und erforderte einige Sorgfalt, um eine effiziente Neuberechnung sicherzustellen. Insbesondere sollten Sie in Excel 2000 arbeitsblattübergreifende Abhängigkeiten möglichst vermeiden und Arbeitsblätter in alphabetischer Reihenfolge benennen, sodass Arbeitsblätter, die von anderen Arbeitsblättern abhängig sind, alphabetisch nach den Arbeitsblättern kommen, von denen sie abhängen.</span><span class="sxs-lookup"><span data-stu-id="52408-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="52408-p108">In Excel 2007 wurde die Logik verbessert und ermöglicht die Neuberechnung in mehreren Threads, sodass Abschnitte der Berechnungskette nicht voneinander abhängig sind und gleichzeitig berechnet werden können. Sie können Excel so konfigurieren, dass mehrere Threads auf einem Computer mit einem einzelnen Prozessor verwendet werden, oder dass ein einzelner Thread auf einem Computer mit mehreren Prozessoren oder Prozessorkernen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52408-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="52408-152">Asynchrone benutzerdefinierte Funktionen (User-Defined Functions, UDFs)</span><span class="sxs-lookup"><span data-stu-id="52408-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="52408-p109">Wenn eine Berechnung eine asynchrone UDF erkennt, wird der Status der aktuellen Formel gespeichert, die UDF-Datei gestartet und die Auswertung der restlichen Zellen fortgesetzt. Nach Abschluss der Zellenauswertung wartet Excel auf den Abschluss der asynchronen Funktionen, sofern noch asynchrone Funktionen ausgeführt werden. Nachdem die einzelnen asynchronen Funktionen Ergebnisse gemeldet haben, beendet Excel die Formel und führt dann einen neuen Berechnungslauf durch, um Zellen neu zu berechnen, die die Zelle mit dem Verweis auf die asynchrone Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="52408-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="52408-156">Veränderliche und nicht veränderliche Funktionen</span><span class="sxs-lookup"><span data-stu-id="52408-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="52408-p110">Excel unterstützt das Konzept einer veränderlichen Funktion; dies ist eine Funktion, deren Wert sich auch dann von einem Moment zum nächsten ändern kann, wenn keines ihrer Argumente (sofern vorhanden) geändert wurde. Excel wertet Zellen mit veränderliche Funktionen und alle untergeordneten Zellen bei jeder Neuberechnung neu aus. Aus diesem Grund kann die Verwendung einer großen Anzahl von veränderlichen Funktionen die Neuberechnung verlangsamen. Verwenden Sie diese Funktionen möglichst selten.</span><span class="sxs-lookup"><span data-stu-id="52408-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="52408-161">Die folgenden Excel-Funktionen sind veränderlich:</span><span class="sxs-lookup"><span data-stu-id="52408-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="52408-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="52408-162">**NOW**</span></span>
    
- <span data-ttu-id="52408-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="52408-163">**TODAY**</span></span>
    
- <span data-ttu-id="52408-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="52408-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="52408-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="52408-165">**OFFSET**</span></span>
    
- <span data-ttu-id="52408-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="52408-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="52408-167">**INFO** (abhängig von den Argumenten)</span><span class="sxs-lookup"><span data-stu-id="52408-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="52408-168">**CELL** (abhängig von den Argumenten)</span><span class="sxs-lookup"><span data-stu-id="52408-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="52408-169">**SUMIF** (abhängig von den Argumenten)</span><span class="sxs-lookup"><span data-stu-id="52408-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="52408-p111">Sowohl VBA als auch die C-API bieten Möglichkeiten, Excel darüber zu informieren, dass eine benutzerdefinierte Funktion (UDF) als veränderlich behandelt werden soll. Bei Verwendung von VBA wird die UDF wie folgt als veränderlich deklariert.</span><span class="sxs-lookup"><span data-stu-id="52408-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="52408-p112">Standardmäßig geht Excel davon aus, dass VBA-UDFs nicht veränderlich sind. Excel erfährt erst beim ersten Aufruf einer UDF, dass diese veränderlich ist. Eine veränderliche UDF kann wie in diesem Beispiel gezeigt wieder als nicht veränderlich festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="52408-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="52408-p113">Mit der C-API können Sie eine XLL-Funktion schon vor dem ersten Aufruf als veränderlich registrieren. Außerdem können Sie den veränderlichen Status einer Arbeitsblattfunktion damit ein- und ausschalten.</span><span class="sxs-lookup"><span data-stu-id="52408-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="52408-p114">Standardmäßig werden XLL-UDFs, die Bereichsargumente akzeptieren und als Makrovorlagenentsprechungen deklariert sind, von Excel als unveränderlich behandelt. Sie können diesen Standardstatus beim ersten Aufruf der UDF mit der **xlfVolatile**-Funktion deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="52408-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="52408-179">Berechnungsmodi, Befehle, selektive Neuberechnung und Datentabellen</span><span class="sxs-lookup"><span data-stu-id="52408-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="52408-180">Excel verfügt über drei Berechnungsmodi:</span><span class="sxs-lookup"><span data-stu-id="52408-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="52408-181">Automatic</span><span class="sxs-lookup"><span data-stu-id="52408-181">Automatic</span></span>
    
- <span data-ttu-id="52408-182">Automatisch außer bei Datentabellen</span><span class="sxs-lookup"><span data-stu-id="52408-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="52408-183">Manual</span><span class="sxs-lookup"><span data-stu-id="52408-183">Manual</span></span>
    
<span data-ttu-id="52408-p115">Im automatischen Berechnungsmodus erfolgt die Neuberechnung nach jeder Dateneingabe und nach bestimmten Ereignissen, wie z. B. den im vorherigen Abschnitt genannten Beispielen. Für sehr große Arbeitsmappen ist die Neuberechnungszeit möglicherweise so lang, dass Benutzer Neuberechnungen auf absolut erforderliche Fälle beschränken müssen. Hierzu unterstützt Excel den manuellen Modus. Der Benutzer kann den Modus über das Excel-Menüsystem oder programmgesteuert mithilfe von VBA, COM oder der C-API auswählen.</span><span class="sxs-lookup"><span data-stu-id="52408-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="52408-p116">Datentabellen sind spezielle Strukturen in einem Arbeitsblatt. Der Benutzer richtet zuerst die Berechnung des Ergebnisses auf einem Arbeitsblatt ein. Diese hängt von einer oder zwei veränderbaren Schlüsseleingaben und anderen Parametern ab. Der Benutzer kann dann eine Tabelle mit Ergebnissen für einen Satz von Werten für eine oder beide Schlüsseleingaben erstellen. Die Tabelle wird mit dem **Assistenten für Datentabellen** erstellt. Nachdem die Tabelle eingerichtet wurde, fügt Excel die Eingaben einzeln nacheinander in die Berechnung ein und kopiert den resultierenden Wert in die Tabelle. Da eine oder zwei Eingaben verwendet werden können, können Datentabellen ein- oder zweidimensional sein.</span><span class="sxs-lookup"><span data-stu-id="52408-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="52408-195">Die Neuberechnung von Datentabellen wird etwas anders gehandhabt:</span><span class="sxs-lookup"><span data-stu-id="52408-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="52408-196">Die Neuberechnung erfolgt asynchron zur normalen Neuberechnung der Arbeitsmappe, sodass die Neuberechnung großer Tabellen länger dauern kann der Vorgang für den Rest der Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="52408-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="52408-p117">Zirkelbezüge sind zulässig. Wenn die zur Ermittlung des Ergebnisses verwendete Berechnung von einem oder mehreren Werten aus der Datentabelle abhängt, gibt Excel keinen Fehler für den Zirkelbezug zurück.</span><span class="sxs-lookup"><span data-stu-id="52408-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 

- <span data-ttu-id="52408-199">Datentabellen verwenden keine Multithreadberechnung.</span><span class="sxs-lookup"><span data-stu-id="52408-199">Data tables do not use multi-threaded calculation.</span></span>
    
<span data-ttu-id="52408-p118">Da Excel die Neuberechnung von Datentabellen anders handhabt und die Berechnung großer Tabellen, die komplexe oder langwierige Berechnungen erfordern, sehr lange dauern kann, haben Sie in Excel die Möglichkeit, die automatische Berechnung von Datentabellen zu deaktivieren. Legen Sie hierzu den Berechnungsmodus auf "Automatisch außer bei Datentabellen" fest. Wenn dieser Berechnungsmodus aktiv ist, drückt der Benutzer F9 oder führt einen entsprechenden Programmiervorgang aus, um die Datentabellen neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="52408-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="52408-p119">Excel stellt Methoden zur Verfügung, mit denen Sie den Neuberechnungsmodus ändern und die Neuberechnung steuern können. Diese Methoden wurden von Version zu Version verbessert, um eine präzisere Steuerung zu ermöglichen. Die betreffenden Funktionen der C-API entsprechen denen in Excel, Version 5, und bieten daher nicht das Maß an Steuerung, von dem Sie bei Verwendung von VBA in neueren Versionen profitieren.</span><span class="sxs-lookup"><span data-stu-id="52408-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="52408-206">Diese Methoden werden am häufigsten verwendet, wenn sich Excel im manuellen Berechnungsmodus befindet, und erlauben die selektive Berechnung von Arbeitsmappen, Arbeitsblättern und Bereichen, die vollständige Neuberechnung aller geöffneten Arbeitsmappen und sogar die vollständige Neuerstellung der Abhängigkeitsstruktur und der Berechnungskette.</span><span class="sxs-lookup"><span data-stu-id="52408-206">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="52408-207">Bereichsberechnung</span><span class="sxs-lookup"><span data-stu-id="52408-207">Range Calculation</span></span>

<span data-ttu-id="52408-208">Tastenkombination: keine</span><span class="sxs-lookup"><span data-stu-id="52408-208">Keystroke: None</span></span>
  
<span data-ttu-id="52408-209">VBA: **Range.Calculate** (eingeführt in Excel 2000, geändert in Excel 2007) und **Range.CalculateRowMajorOrder** (eingeführt in Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="52408-209">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="52408-210">C-API: nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52408-210">C API: Not supported</span></span>
  
- <span data-ttu-id="52408-211">**Manueller Modus**</span><span class="sxs-lookup"><span data-stu-id="52408-211">**Manual mode**</span></span>
    
    <span data-ttu-id="52408-p120">Berechnet nur die Zellen im angegebenen Bereich neu, unabhängig davon, ob sie geändert wurden oder nicht. Das Verhalten der **Range.Calculate**-Methode wurde in Excel 2007 geändert; das alte Verhalten wird jedoch noch von der **Range.CalculateRowMajorOrder** -Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52408-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="52408-214">**Modi "Automatisch" und "Automatisch außer bei Datentabellen"**</span><span class="sxs-lookup"><span data-stu-id="52408-214">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="52408-215">Berechnet die Arbeitsmappe neu, erzwingt jedoch keine Neuberechnung des Bereichs oder einer Zelle im Bereich.</span><span class="sxs-lookup"><span data-stu-id="52408-215">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="52408-216">Berechnung des aktiven Arbeitsblatts</span><span class="sxs-lookup"><span data-stu-id="52408-216">Active Worksheet Calculation</span></span>

<span data-ttu-id="52408-217">Tastenkombination: UMSCHALT + F9</span><span class="sxs-lookup"><span data-stu-id="52408-217">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="52408-218">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="52408-218">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="52408-219">C-API: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="52408-219">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="52408-220">**Alle Modi**</span><span class="sxs-lookup"><span data-stu-id="52408-220">**All modes**</span></span>
    
    <span data-ttu-id="52408-221">Berechnet nur die Zellen neu, die im aktiven Arbeitsblatt als zu berechnen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="52408-221">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="52408-222">Berechnung des angegebenen Arbeitsblatts</span><span class="sxs-lookup"><span data-stu-id="52408-222">Specified Worksheet Calculation</span></span>

<span data-ttu-id="52408-223">Tastenkombination: keine</span><span class="sxs-lookup"><span data-stu-id="52408-223">Keystroke: None</span></span>
  
<span data-ttu-id="52408-224">VBA: **Worksheets(** Reference **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="52408-224">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="52408-225">C-API: nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52408-225">C API: Not supported</span></span>
  
- <span data-ttu-id="52408-226">**Alle Modi**</span><span class="sxs-lookup"><span data-stu-id="52408-226">**All modes**</span></span>
    
    <span data-ttu-id="52408-p121">Berechnet nur die geänderten Zellen und ihre abhängigen Zellen innerhalb des angegebenen Arbeitsblatts neu. "Reference" ist der Name des Arbeitsblatts als Zeichenfolge oder die Indexnummer in der entsprechenden Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="52408-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="52408-p122">In Excel 2000 und späteren Versionen steht eine **Boolean**-Arbeitsblatteigenschaft zur Verfügung, die **EnableCalculation**-Eigenschaft. Durch Festlegen dieser Eigenschaft auf **True** von **False** werden alle Zellen im angegebenen Arbeitsblatt als geändert definiert. In automatischen Modi löst dies außerdem eine Neuberechnung der gesamten Arbeitsmappe aus.</span><span class="sxs-lookup"><span data-stu-id="52408-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="52408-232">Im manuellen Modus bewirkt der folgende Code, dass nur das aktive Blatt neu berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="52408-232">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="52408-233">Neuerstellung der Arbeitsmappenstruktur und erzwungene Neuberechnung</span><span class="sxs-lookup"><span data-stu-id="52408-233">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="52408-234">Tastenkombination: STRG + ALT + UMSCHALT + F9 (eingeführt in Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="52408-234">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="52408-235">VBA: **Workbooks(** Reference **).ForceFullCalculation** (eingeführt in Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="52408-235">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="52408-236">C-API: nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52408-236">C API: Not supported</span></span>
  
- <span data-ttu-id="52408-237">**Alle Modi**</span><span class="sxs-lookup"><span data-stu-id="52408-237">**All modes**</span></span>
    
    <span data-ttu-id="52408-238">Bewirkt, dass Excel die Abhängigkeitsstruktur und die Berechnungskette für eine bestimmte Arbeitsmappe neu berechnet, und erzwingt eine Neuberechnung aller Zellen, die Formeln enthalten.</span><span class="sxs-lookup"><span data-stu-id="52408-238">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="52408-239">Alle geöffneten Arbeitsmappen</span><span class="sxs-lookup"><span data-stu-id="52408-239">All Open Workbooks</span></span>

<span data-ttu-id="52408-240">Tastenkombination: F9</span><span class="sxs-lookup"><span data-stu-id="52408-240">Keystroke: F9</span></span>
  
<span data-ttu-id="52408-241">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="52408-241">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="52408-242">C-API: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="52408-242">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="52408-243">**Alle Modi**</span><span class="sxs-lookup"><span data-stu-id="52408-243">**All modes**</span></span>
    
    <span data-ttu-id="52408-p123">Berechnet alle Zellen neu, die Excel als geändert markiert hat, d. h. abhängige Elemente von veränderlichen oder geänderten Daten sowie programmgesteuert als geändert markierte Zellen. Im Berechnungsmodus "Automatisch außer bei Datentabellen" werden die Tabellen berechnet, die aktualisiert werden müssen, sowie alle veränderlichen Funktionen und ihre abhängigen Elemente.</span><span class="sxs-lookup"><span data-stu-id="52408-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="52408-246">Neuerstellung der Struktur und erzwungene Berechnung für alle geöffneten Arbeitsmappen</span><span class="sxs-lookup"><span data-stu-id="52408-246">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="52408-247">Tastenkombination: STRG + ALT + F9.</span><span class="sxs-lookup"><span data-stu-id="52408-247">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="52408-248">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="52408-248">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="52408-249">C-API: nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52408-249">C API: Not supported</span></span>
  
- <span data-ttu-id="52408-250">**Alle Modi**</span><span class="sxs-lookup"><span data-stu-id="52408-250">**All modes**</span></span>
    
    <span data-ttu-id="52408-p124">Berechnet alle Zellen in allen geöffneten Arbeitsmappen neu. Im Berechnungsmodus "Automatisch außer bei Datentabellen" wird die Neuberechnung der Tabellen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="52408-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52408-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52408-253">See also</span></span>



[<span data-ttu-id="52408-254">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="52408-254">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="52408-255">Datentypen von Excel verwendet</span><span class="sxs-lookup"><span data-stu-id="52408-255">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="52408-256">Speicherverwaltung in Excel</span><span class="sxs-lookup"><span data-stu-id="52408-256">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="52408-257">Excel-Programmierkonzepte</span><span class="sxs-lookup"><span data-stu-id="52408-257">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

