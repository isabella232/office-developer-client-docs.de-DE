---
title: Aufrufen von Excel von der DLL oder XLL aus
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- dialog boxes [excel 2007], invoking excel commands,DLLs [Excel 2007], calling into Excel,passing arguments to C API functions [Excel 2007],commands [Excel 2007], invoking with dialog boxes,commands [Excel 2007], accessible from DLL/XLL,Excel4 function [Excel 2007],Excel12 function [Excel 2007],XLCallVer function [Excel 2007],operRes argument [Excel 2007],functions [Excel 2007], accessible from DLL/XLL,Excel12v function [Excel 2007],DLL-only functions [Excel 2007],C API [Excel 2007], passing arguments,count argument [Excel 2007],commands [Excel 2007], calling in international versions,DLL-only commands [Excel 2007],international versions [Excel 2007], calling functions and commands,XLLs [Excel 2007], calling into Excel,Excel 4v function [Excel 2007],xlfn argument [Excel 2007],functions [Excel 2007], calling in international versions
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726120"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="f5831-104">Aufrufen von Excel von der DLL oder XLL aus</span><span class="sxs-lookup"><span data-stu-id="f5831-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="f5831-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5831-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f5831-p101">Mit Microsoft Excel können DLL-Dateien auf integrierte Excel-Befehle, Arbeitsblattfunktionen und Makrovorlagenfunktionen zugreifen. Diese sind �ber in Visual Basic for Applications (VBA) aufgerufene DLL-Befehle und -Funktionen und �ber direkt in Excel aufgerufene registrierte XLL-Befehle und Funktionen verf�gbar.</span><span class="sxs-lookup"><span data-stu-id="f5831-p101">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions. These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="f5831-108">Excel4-, Excel4v-, Excel12- und Excel12v-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f5831-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="f5831-109">Mit Excel können DLL_Dateien �ber die [Excel4](excel4-excel12.md)-, [Excel4v](excel4v-excel12v.md)-, [Excel12](excel4-excel12.md)- und [Excel12v](excel4v-excel12v.md)-R�ckruffunktionen auf Befehle und Funktionen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f5831-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="f5831-p102">Die **Excel4**- und **Excel4v**-Funktionen wurden in Excel, Version 4 eingef�hrt. Sie arbeiten mit der **XLOPER**-Datenstruktur. In Excel 2007 wurden zwei neue R�ckruffunktionen eingef�hrt, **Excel12** und **Excel12v**, die mit der **XLOPER12**-Datenstruktur arbeiten. Die **Excel4**- und **Excel4v**-Funktionen werden von der Bibliothek �Xlcall32.lib" in Ihrem DLL- oder XLL-Projekt exportiert. **Excel12** und **Excel12v** sind in der SDK C++-Quelldatei �Xlcall.cpp" enthalten, die in Ihrem Projekt enthalten sein muss, wenn Sie mit **XLOPER12**-Strukturen auf Excel-Funktionen zugreifen m�chten .</span><span class="sxs-lookup"><span data-stu-id="f5831-p102">The **Excel4** and **Excel4v** functions were introduced in Excel version 4. They work with the **XLOPER** data structure. Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure. The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project. **Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="f5831-p103">Der folgende Code zeigt die Funktionsprototypen für diese vier Funktionen. Die ersten drei Argumente sind bis auf die Ausnahme,dass das zweite Argument auf ein **XLOPER**-Objekt im ersten Paar und auf ein **XLOPER12**-Objekt im zweiten Paar zeigt, identisch. Die Aufrufkonvention ist **_cdecl** in **Excel4** und **Excel12**, um Variablenargumentlisten zuzulassen. Die drei Punkte geben die Zeiger auf **XLOPER**-Werte für **Excel4** und **XLOPER12**-Werte für **Excel12** an. Die Anzahl der Zeiger entspricht dem Wert des  _count_-Parameters.</span><span class="sxs-lookup"><span data-stu-id="f5831-p103">The following code shows the function prototypes for these four functions. The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair. The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists. The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**. The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="f5831-120">**Alle Excel-Versionen**</span><span class="sxs-lookup"><span data-stu-id="f5831-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="f5831-121">**Ab Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="f5831-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="f5831-p104">Damit die DLL **Excel4**, **Excel4v**, **Excel12** oder **Excel12v** aufrufen kann, muss Excel das Steuerelement an die DLL �bergeben. Dies bedeutet, dass diese C-API-Rückrufe nur in den folgenden Szenarien aufgerufen werden können:</span><span class="sxs-lookup"><span data-stu-id="f5831-p104">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL. This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="f5831-124">Von einem XLL-Befehl aus, der Excel direkt oder über VBA aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="f5831-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="f5831-125">Von einer XLL-Arbeitsblatt- oder Makrovorlagenfunktion aus, die Excel direkt oder über VBA aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="f5831-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="f5831-126">Sie können die Excel-C-API in den folgenden Szenarien nicht aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f5831-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="f5831-127">Von einem Betriebssystemereignis aus (z.�B. von der [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)-Funktion aus).</span><span class="sxs-lookup"><span data-stu-id="f5831-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="f5831-128">Von einem Hintergrundthread aus, den die DLL erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="f5831-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="f5831-129">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f5831-129">Return values</span></span>

<span data-ttu-id="f5831-p105">Alle diese vier Funktionen geben eine ganze Zahl zur�ck, mit der dem Aufrufer mitgeteilt wird, ob die Funktion oder der Befehl erfolgreich aufgerufen wurden. Die zur�ckgegebenen Werte können die folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="f5831-p105">All four of these functions return an integer value that informs the caller whether the function or command was called successfully. The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="f5831-132">**R�ckgabewert**</span><span class="sxs-lookup"><span data-stu-id="f5831-132">**Return value**</span></span>|<span data-ttu-id="f5831-133">**Definiert in Xlcall.h als**</span><span class="sxs-lookup"><span data-stu-id="f5831-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="f5831-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5831-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5831-135">0</span><span class="sxs-lookup"><span data-stu-id="f5831-135">0</span></span>  <br/> |<span data-ttu-id="f5831-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="f5831-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="f5831-p106">Die Funktion oder der Befehl wurde erfolgreich ausgef�hrt. Dies bedeutet jedoch nicht, dass die Ausf�hrung ohne Fehler erfolgte. **Excel4** k�nnte z.�B. **xlretSuccess** beim Aufrufen der **FIND**-Funktion zur�ckgeben, obwohl **#VALUE!** als Wert ermittelt wurde, da der Suchtext nicht gefunden werden konnte. Sie sollten den Typ und den Wert des zur�ckgegebenen **XLOPER/XLOPER12**-Objekts pr�fen, bei dem dies m�glich ist.  </span><span class="sxs-lookup"><span data-stu-id="f5831-p106">The function or command executed successfully. This does not mean that the execution was error free. For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!** because the search text could not be found. You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.  </span></span><br/> |
|<span data-ttu-id="f5831-142">1</span><span class="sxs-lookup"><span data-stu-id="f5831-142">1</span></span>  <br/> |<span data-ttu-id="f5831-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="f5831-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="f5831-144">Ein Makrobefehl wurde durch Klicken des Benutzers auf die Schaltfl�che **Abbrechen** oder durch Dr�cken der ESC-Taste beendet.</span><span class="sxs-lookup"><span data-stu-id="f5831-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="f5831-145">2</span><span class="sxs-lookup"><span data-stu-id="f5831-145">2</span></span>  <br/> |<span data-ttu-id="f5831-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="f5831-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="f5831-p107">Die angegebene Funktion oder der angegebene Befehlscode ist ung�ltig. Dieser Fehler kann auftreten, wenn die aufgerufene Funktion nicht �ber die Berechtigung zum Aufrufen der Funktion oder des Befehls verf�gt. Eine Arbeitsblattfunktion z.�B. kann eine Makrovorlagenfunktion oder eine Befehlsfunktion nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5831-p107">The supplied function or command code is not valid. This error can occur when the calling function does not have permission to call the function or command. For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="f5831-150">4</span><span class="sxs-lookup"><span data-stu-id="f5831-150">4</span></span>  <br/> |<span data-ttu-id="f5831-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="f5831-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="f5831-152">Die Anzahl der im Aufruf angegebenen Argumente ist falsch.</span><span class="sxs-lookup"><span data-stu-id="f5831-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="f5831-153">8</span><span class="sxs-lookup"><span data-stu-id="f5831-153">8</span></span>  <br/> |<span data-ttu-id="f5831-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="f5831-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="f5831-155">Mindestens eines der **XLOPER**- oder **XLOPER12**-Argumentwerte ist falsch formatiert oder aufgef�llt.</span><span class="sxs-lookup"><span data-stu-id="f5831-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="f5831-156">16</span><span class="sxs-lookup"><span data-stu-id="f5831-156">16</span></span>  <br/> |<span data-ttu-id="f5831-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="f5831-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="f5831-158">Excel hat ein festgestellt, dass der Vorgang möglicherweise zum Stapelüberlauf führt und hat die Funktion deshalb nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f5831-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="f5831-159">32</span><span class="sxs-lookup"><span data-stu-id="f5831-159">32</span></span>  <br/> |<span data-ttu-id="f5831-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="f5831-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="f5831-p108">Beim Ausf�hren des Befehls oder der Funktion ist ein Fehler aufgetreten, dessen Ursache nicht von einem der anderen R�ckgabewerte beschrieben wird. Ein Vorgang, der zu viel Speicher erfordert, w�rde z.�B. diesen Fehler zur�ckgeben. Dies kann bei dem Versuch auftreten, einen sehr gro�en Verweis in ein **xltypeMulti**-Array mithilfe der [xlCoerce](xlcoerce.md)-Funktion zu konvertieren.  </span><span class="sxs-lookup"><span data-stu-id="f5831-p108">The command or function failed for a reason not described by one of the other return values. An operation that would require too much memory, for example, would fail with this error. This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.  </span></span><br/> |
|<span data-ttu-id="f5831-164">64</span><span class="sxs-lookup"><span data-stu-id="f5831-164">64</span></span>  <br/> |<span data-ttu-id="f5831-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="f5831-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="f5831-p109">Bei dem Vorgang wurde versucht, den Wert einer nicht berechneten Zelle abzurufen. Um Integrit�t der Neuberechnung in Excel zu erhalten, ist dies für Excel-Arbeitsblattfunktionen nicht zul�ssig. Als Makrovorlagenfunktionen registrierte XLL-Befehle und Funktionen d�rfen jedoch auf nicht berechnete Zellwerte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f5831-p109">The operation attempted to retrieve the value of an uncalculated cell. To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this. However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="f5831-169">128</span><span class="sxs-lookup"><span data-stu-id="f5831-169">128</span></span>  <br/> |<span data-ttu-id="f5831-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="f5831-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="f5831-p110">(Ab Excel 2007) Eine als threadsicher registrierte XLL-Arbeitsblattfunktion hat versucht, eine C-API-Funktion aufzurufen, die nicht threadsicher ist. Eine threadsichere Funktion darf z.�B. die XLM-Funktion **xlfGetCell** nicht aufrufen.  </span><span class="sxs-lookup"><span data-stu-id="f5831-p110">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe. For example, a thread-safe function cannot call the XLM function **xlfGetCell**.  </span></span><br/> |
|<span data-ttu-id="f5831-173">256</span><span class="sxs-lookup"><span data-stu-id="f5831-173">256</span></span>  <br/> |<span data-ttu-id="f5831-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="f5831-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="f5831-175">(AbExcel 2010) Das asynchrone Behandeln von Funktionen ist ung�ltig.</span><span class="sxs-lookup"><span data-stu-id="f5831-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="f5831-176">512</span><span class="sxs-lookup"><span data-stu-id="f5831-176">512</span></span>  <br/> |<span data-ttu-id="f5831-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="f5831-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="f5831-178">(Ab Excel 2010) Der Aufruf wird auf Clustern nicht unterst�tzt.</span><span class="sxs-lookup"><span data-stu-id="f5831-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="f5831-p111">Gibt die Funktion einen der Fehlerwerte in der Tabelle zur�ck(d.�h. sie gibt nicht **xlretSuccess** zur�ck), wird der zur�ckgegebene **XLOPER**- oder **XLOPER12**-Wert auch auf **#VALUE!** festgelegt. Unter bestimmten Umst�nden reicht es m�glicherweise aus, dies zu pr�fen. Beachten Sie jedoch, dass ein Aufruf sowohl **xlretSuccess** als auch **#VALUE!** zur�ckgeben kann.</span><span class="sxs-lookup"><span data-stu-id="f5831-p111">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**. In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="f5831-181">Wenn ein Aufruf der C-API zu **xlretUncalced** oder **xlretAbort** f�hrt, sollte der DLL- oder XLL-Code ein Steuerelement an Excel zur�ckgeben, bevor weitere C-API-Aufrufe durchgef�hrt werden (andere als Aufrufe der [xlfree](xlfree.md)-Funktion zum Freigeben der an Excel zugewiesenen Arbeitsspeicherressourcen in **XLOPER**- und **XLOPER12**-Werten).</span><span class="sxs-lookup"><span data-stu-id="f5831-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="f5831-182">Befehls- oder Funktionsenumerationsargument: xlfn</span><span class="sxs-lookup"><span data-stu-id="f5831-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="f5831-p112">Das  _xlfn_-Argument ist das erste Argument der R�ckruffunktionen und ist eine ganze 32-Bit-Zahl mit Vorzeichen. Der Wert des Arguments sollte eine der in der SDK-Headerdatei �Xlcall.h" definierten Funktions- oder Befehlsenumerationen sein, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5831-p112">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer. Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="f5831-185">Alle Arbeitsblatt- und Makrovorlagenfunktionen stellen Hexadezimalwerte zwischen 0 (**xlfCount**) und 0x0fff dar, wobei die höchste zugewiesen Zahl in Excel 2013 die Dezimalzahl 547 ist, Hexadezimalwert 0x0223 (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="f5831-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="f5831-186">Alle Befehlsfunktionen stellen Hexadezimalwerte zwischen 0x8000 (**xlcBeep**) und 0x8fff dar, wobei die höchste zugewiesen Zahl in Excel 2013 die Hexadezimalzahl 0x8328 ist (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="f5831-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="f5831-187">Sie werden in der Headerdatei als  `(n | xlCommand)` definiert, wobei  `n` als eine Dezimalzahl gr��er als oder gleich 0 und **xlCommand** als Hexadezimalzahl 0x8000 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f5831-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="f5831-188">Aufrufen von Excel-Befehlen, die Dialogfelder verwenden</span><span class="sxs-lookup"><span data-stu-id="f5831-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="f5831-p114">Einige der Befehlcodes entsprechen Aktionen in Excel, die Dialogfelder verwenden. **xlcFileDelete** verwendet z. B. ein einzelnes Argument: einen Dateinamen oder eine Dateimaske. Dieser Befehl kann mit dem Dialogfeld aufgerufen werden, sodass der Benutzer den Löschvorgang abbrechen oder ändern kann. Er kann auch ohne das Dialogfeld aufgerufen werden. In diesem Fall werden die Dateien ohne jegliche weitere Interaktion gelöscht, wobei vorausgesetzt wird, dass sie vorhanden sind und der Aufrufer über die entsprechende Berechtigung verfügt. Um solche Befehle im Dialogfeldformat aufrufen zu können, muss die Befehlsenumeration durch den bitweisen OR-Operator mit 0x1000 (**xlPrompt**) verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="f5831-p114">Some of the command codes correspond to actions in Excel that use dialog boxes. For example, **xlcFileDelete** takes a single argument: a file name or mask. This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation. It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission. To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="f5831-194">Im folgenden Codebeispiel werden die Dateien im aktuellen Verzeichnis gel�scht, die der Maske �my_data\*.bak" entsprechen, wobei ein Dialogfeld nur angezeigt wird, wenn das Argument wahr ist.</span><span class="sxs-lookup"><span data-stu-id="f5831-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="f5831-195">Aufrufen von Funktionen und Befehlen in internationalen Versionen</span><span class="sxs-lookup"><span data-stu-id="f5831-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="f5831-p115">Sie können Excel zum Anzeigen von Funktionen und der XLM-Befehlsnamen in einer Vielzahl von Sprachen konfigurieren. Einige C-API-Befehle und -Funktionen verwenden Zeichenfolgen, die als Funktions- oder Befehlsnamen interpretiert werden. **xlcFormula** verwendet z. B. ein Zeichenfolgenargument, das in einer angegebenen Zelle eingefügt werden soll. Damit Ihr Add-In mit allen Spracheinstellungen funktioniert, können Sie die Zeichenfolgennamen in Englisch angeben und das Bit 0x2000 (**xlIntl**) in der Funktions- oder Befehlsenumeration festlegen.</span><span class="sxs-lookup"><span data-stu-id="f5831-p115">You can configure Excel to display functions and XLM command names in a variety of languages. Some C API commands and functions operate on strings that are interpreted as function or command names. For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell. For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="f5831-p116">Im folgenden Code wird das �quivalent von  `=SUM(X1:X100)` in Zelle A2 des aktiven Arbeitsblatts platziert. Beachten Sie, dass die Framework-Funktion **TempActiveRef** zum Erstellen des tempor�ren Verweises **XLOPER** verwendet wird. Die Formel wird in Zelle A2 in der vom Gebietsschema vorgegebenen Sprache angezeigt (z.�B.  `=SOMME(X1:X100)`, wenn Franz�sisch festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="f5831-p116">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet. Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**. The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="f5831-p117">Da das Ergebnis des Aufrufs von **Excel12** nicht erforderlich ist, kann 0 (NULL) als zweites Argument anstelle der Adresse des **xResult**-Objekts �bergeben werden. Dies wird im n�chsten Abschnitt genauer erl�utert.</span><span class="sxs-lookup"><span data-stu-id="f5831-p117">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**. This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="f5831-205">Nur DLL-Funktionen und -Befehle</span><span class="sxs-lookup"><span data-stu-id="f5831-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="f5831-p118">Excel unterst�tzt eine kleine Anzahl von Funktionen, auf die nur von einer DLL oder XLL aus zugegriffen werden kann. Sie werden in der Headerdatei als  `(n | xlSpecial)` definiert, wobei  `n` als eine Dezimalzahl gr��er als oder gleich 0 und  `xlSpecial` als Hexadezimalzahl 0x4000 definiert ist. Diese Funktionen sind in der folgenden Tabelle und unter [Referenz zur API-Funktion](excel-xll-sdk-api-function-reference.md) aufgef�hrt.</span><span class="sxs-lookup"><span data-stu-id="f5831-p118">Excel supports a small number of functions that are only accessible from a DLL or XLL. These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal. These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="f5831-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="f5831-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="f5831-210">0</span><span class="sxs-lookup"><span data-stu-id="f5831-210">0</span></span> | <span data-ttu-id="f5831-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-212">Gibt die für Excel zugewiesenen Arbeitsspeicherressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="f5831-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="f5831-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="f5831-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="f5831-214">1</span><span class="sxs-lookup"><span data-stu-id="f5831-214">1</span></span> | <span data-ttu-id="f5831-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-216">Gibt den freien Speicherplatz im Excel-Stapel zurück.</span><span class="sxs-lookup"><span data-stu-id="f5831-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="f5831-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="f5831-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="f5831-218">2</span><span class="sxs-lookup"><span data-stu-id="f5831-218">2</span></span> | <span data-ttu-id="f5831-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-220">Konvertiert zwischen **XLOPER**- und **XLOPER12**-Typen.</span><span class="sxs-lookup"><span data-stu-id="f5831-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="f5831-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="f5831-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="f5831-222">3</span><span class="sxs-lookup"><span data-stu-id="f5831-222">3</span></span> | <span data-ttu-id="f5831-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-224">Bietet eine schnelle Methode zum Festlegen von Zellwerten.</span><span class="sxs-lookup"><span data-stu-id="f5831-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="f5831-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="f5831-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="f5831-226">4</span><span class="sxs-lookup"><span data-stu-id="f5831-226">4</span></span> | <span data-ttu-id="f5831-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-228">Ruft einen Arbeitsblattnamen aus seiner internen ID ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="f5831-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="f5831-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="f5831-230">5</span><span class="sxs-lookup"><span data-stu-id="f5831-230">5</span></span> | <span data-ttu-id="f5831-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-232">Ruft eine interne Arbeitsblatt-ID aus dem zugehörigen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="f5831-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="f5831-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="f5831-234">6</span><span class="sxs-lookup"><span data-stu-id="f5831-234">6</span></span> | <span data-ttu-id="f5831-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-236">�berpr�ft, ob der Benutzer auf die Schaltfl�che **Abbrechen** geklickt oder die ESC-Taste gedr�ckt hat.</span><span class="sxs-lookup"><span data-stu-id="f5831-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="f5831-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="f5831-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="f5831-238">7</span><span class="sxs-lookup"><span data-stu-id="f5831-238">7</span></span> | <span data-ttu-id="f5831-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-240">Ruft das Excel-Instanzhandle ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="f5831-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="f5831-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="f5831-242">8</span><span class="sxs-lookup"><span data-stu-id="f5831-242">8</span></span> | <span data-ttu-id="f5831-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-244">Ruft die Zugriffsnummer des Excel-Hauptfensters ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="f5831-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="f5831-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="f5831-246">9</span><span class="sxs-lookup"><span data-stu-id="f5831-246">9</span></span> | <span data-ttu-id="f5831-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-248">Ruft den Pfad und den Dateinamen der DLL-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="f5831-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="f5831-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="f5831-250">10</span><span class="sxs-lookup"><span data-stu-id="f5831-250">10</span></span> | <span data-ttu-id="f5831-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-252">Diese Funktion ist veraltet und wird nicht mehr aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f5831-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="f5831-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="f5831-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="f5831-254">11</span><span class="sxs-lookup"><span data-stu-id="f5831-254">11</span></span> | <span data-ttu-id="f5831-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-256">Diese Funktion ist veraltet und wird nicht mehr aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f5831-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="f5831-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="f5831-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="f5831-258">12</span><span class="sxs-lookup"><span data-stu-id="f5831-258">12</span></span> | <span data-ttu-id="f5831-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-260">Definiert den Namen eines dauerhaften binären Speichers.</span><span class="sxs-lookup"><span data-stu-id="f5831-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="f5831-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="f5831-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="f5831-262">13</span><span class="sxs-lookup"><span data-stu-id="f5831-262">13</span></span> | <span data-ttu-id="f5831-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="f5831-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="f5831-264">Ruft die Namensdaten eines dauerhaften binären Speichers ab.</span><span class="sxs-lookup"><span data-stu-id="f5831-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="f5831-265">Rückgabewert XLOPER/XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="f5831-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="f5831-266">Das _operRes_-Argument ist das zweite Argument für die Rückrufe und ist ein Zeiger auf ein **XLOPER**- (**Excel4** und **Excel4v**) oder **XLOPER12**-Objekt (**Excel12** und **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="f5831-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="f5831-267">Nach einem erfolgreichen Aufruf enthält es den Rückgabewert der Funktion oder des Befehls.</span><span class="sxs-lookup"><span data-stu-id="f5831-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="f5831-268">**operRes** kann auf 0 (null) (NULL-Zeiger) festgelegt werden, wenn kein R�ckgabewert erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5831-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="f5831-269">Die vorherigen Inhalte von **operRes** werden �berschrieben, sodass der vollst�ndige Arbeitsspeicher, auf den gezeigt wurde, vor dem Aufruf freigegeben werden muss, um Arbeitsspeicherverluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f5831-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="f5831-p120">Wenn die Funktion oder der Befehl nicht aufgerufen werden kann (z.�B. wenn die Argumente falsch sind), wird für **operRes** der Fehler **#VALUE!** festgelegt. Ein Befehl gibt immer **Boolean** **TRUE** zur�ck, wenn dieser erfolgreich war, oder **FALSE**, wenn dabei ein Fehler aufgetreten ist oder dieser vom Benutzer abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="f5831-p120">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**. A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="f5831-272">Anzahl nachfolgender Argumente: count</span><span class="sxs-lookup"><span data-stu-id="f5831-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="f5831-p121">Das  _count_-Argument ist das dritte Argument für die Rückrufe und ist eine ganze 32-Bit-Zahl mit Vorzeichen. Es sollte auf die Anzahl der nachfolgenden Argumente, beginnend bei 1, festgelegt werden. Wenn eine Funktion oder ein Befehl keine Argumente verwendet, sollte sie bzw. es auf 0 (null) festgelegt werden. In Microsoft Office Excel 2003 betr�gt die maximale Anzahl an Argumenten, die jede Funktion verwenden kann, 30, wobei die meisten weniger verwenden. Ab Excel 2007, wurde die maximale Anzahl von Argumenten, die jede Funktion verwenden kann, auf 255 erh�ht.</span><span class="sxs-lookup"><span data-stu-id="f5831-p121">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer. It should be set to the number of subsequent arguments, counting from 1. If a function or command takes no arguments, it should be set to zero. In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this. Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="f5831-p122">In **Excel4** und **Excel12** ist  _count_ die Anzahl der Zeiger auf **XLOPER**- oder **XLOPER12**-Werte, die �bergeben werden. Achten Sie darauf, nicht weniger Argumente zu �bergeben, als der Wert, auf den  _count_ festgelegt ist. Dies w�rde dazu f�hren, dass Excel im Stapel liest und versucht, ung�ltige **XLOPER**- oder **XLOPER12**-Werte zu verarbeiten, was zum Absturz der Anwendung f�hren kann.</span><span class="sxs-lookup"><span data-stu-id="f5831-p122">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed. You should be very careful not to pass fewer arguments than the value that  _count_ is set to. This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="f5831-p123">In **Excel4v** und **Excel12v** ist  _count_ die Gr��e des Arrays der Zeiger auf **XLOPER**- oder **XLOPER12**-Werte, die als n�chstes und letztes Argument �bergeben werden. Auch hier sollten Sie darauf achten, dass das �bergebene Array nicht kleiner ist als die  _count_-Elemente, da dies zu Grenz�berschreitungen des Arrays f�hren kann.</span><span class="sxs-lookup"><span data-stu-id="f5831-p123">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument. Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="f5831-283">Übergeben von Argumenten an C-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f5831-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="f5831-p124">**Excel4** und **Excel12** verwenden nach  _count_ jeweils Variablenl�ngen-Argumentlisten, die als Zeiger auf **XLOPER**- und **XLOPER12**-Werte interpretiert werden. **Excel4v** und **Excel12v** verwenden nach  _count_ ein einzelnes Argument, das bei **Excel4v** einen Zeiger auf ein Array von Zeigern auf **XLOPER**-Werte und bei **Excel12v** auf **XLOPER12**-Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5831-p124">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively. **Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="f5831-p125">Die Arrayformen **Excel4v** und **Excel12v** erm�glichen es Ihnen, einen Aufruf an die C-API ordnungsgem�� zu codieren, wenn die Anzahl der Argumente variabel ist. Das folgende Beispiel zeigt eine Funktion, die ein Array mit Zahlen von variabler Gr��e verwendet und �ber die C-API Excel-Arbeitsblattfunktionen nutzt, um Summe, Mittelwert, Minimum und Maximum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f5831-p125">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable. The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="f5831-p126">Beim Ersetzen von Verweisen auf **XLOPER12**-Werte durch **XLOPER**, und von **Excel12v** durch **Excel4v**, w�re im vorangehenden Code eine Funktion das Ergebnis, die mit allen Versionen von Excel funktioniert. Dieser Vorgang der Excel-Funktionen **SUM**, **AVERAGE**, **MIN** und **MAX** ist so einfach, dass es effizienter w�re, diese in C zu codieren, statt Vorbereitung der Argumente und des Aufrufs in Excel. Viele der Excel-Funktionen sind jedoch komplexer, sodass dieser Ansatz in bestimmten Szenarien hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="f5831-p126">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel. This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel. However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="f5831-p127">Im Thema [xlfRegister](xlfregister-form-1.md) ist ein weiteres Beispiel für die Verwendung mit **Excel4v** und **Excel12v** enthalten. Beim Registrieren einer XLL-Arbeitsblattfunktion können Sie eine beschreibende Zeichenfolge für jedes Argument angeben, das im Dialogfeld **Funktion einf�gen** verwendet wird. Die Gesamtanzahl der für **xlfRegister** angegebenen Argumente h�ngt daher von der Anzahl der Argumente ab, die Ihre XLL-Funktion verwendet, und variiert je nach Funktion.</span><span class="sxs-lookup"><span data-stu-id="f5831-p127">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**. When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box. Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="f5831-p128">Beim Aufrufen einer C-API-Funktion oder eines -Befehls mit der gleichen Anzahl von Argumenten, m�chten Sie den zus�tzlichen Schritt vermeiden und kein Array von Zeigern für diese Argumente erstellen. In diesen F�llen ist es einfacher, **Excel4** und **Excel12** zu verwenden. Beim Registrieren von XLL-Funktionen und -Befehlen z.�B. m�ssen Sie den vollst�ndigen Pfad und Dateinamen der DLL oder XLL angeben. Sie können den Dateinamen in einem Aufruf von **xlfGetName** abrufen und diesen anschlie�end mit einem Aufruf von **xlFree** freigeben, wie im folgenden Beispiel für **Excel4** und **Excel12** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5831-p128">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments. In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**. For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL. You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="f5831-298">In der Praxis kann die **Excel12v_example**-Funktion effizienter codiert werden, indem ein einziges **xltypeMulti** **XLOPER12**-Argument erstellt und die C-API mithilfe von **Excel12** aufgerufen wird, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5831-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="f5831-p129">In diesem Fall wird der R�ckgabewert von **Excel12** ignoriert. Stattdessen �berpr�ft der Code, ob das zur�ckgegebene **XLOPER12**-Objekt **xltypeNum** aufweist, um zu ermitteln, ob der Aufruf erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f5831-p129">In this case, the return value of **Excel12** is ignored. The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="f5831-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="f5831-301">XLCallVer</span></span>

<span data-ttu-id="f5831-302">Neben den Rückrufen **Excel4**, **Excel4v**, **Excel12** und **Excel12v** exportiert Excel eine **XLCallVer**-Funktion, die die Version der aktuell ausgeführten C-API zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f5831-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="f5831-303">Der Funktionsprototyp lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f5831-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="f5831-304">Sie können diese threadsichere Funktion von einem beliebigen XLL-Befehl oder einer -Funktion aus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f5831-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="f5831-p130">In Excel 97 bis Excel 2003 gibt **XLCallVer**den Wert 1280 = 0x0500 hex = 5 x 256 zur�ck, was auf Excel Version�5 hinweist. Ab Excel 2007 wird 3072 = 0x0c00 hex = 12 x 256 zur�ckgegeben, was auf Version 12 hinweist.</span><span class="sxs-lookup"><span data-stu-id="f5831-p130">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5. Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="f5831-p131">Obwohl Sie auf diese Weise feststellen können, ob die neue C-API zur Laufzeit verf�gbar ist, m�chten Sie m�glicherweise unter Verwendung von `Excel4(xlfGetWorkspace, &version, 1, &arg)` die ausgef�hrte Excel-Version ermitteln, wobei  `arg` ist ein numerischer Wert **XLOPER**, der auf 2 festgelegt ist. Die Funktion gibt eine Zeichenfolge **XLOPER** zur�ck, d.�h. die Version, die dann in eine ganze Zahl umgewandelt werden kann. Der Grund für die Verwendung der Excel-Version statt der C-API-Version stellen Unterschiede zwischen Excel 2000, Excel 2002 und Excel 2003 dar, die das Add-In ggf. auch erkennen muss. Es wurden beispielsweise �nderungen an der Genauigkeit einiger Statistikfunktionen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="f5831-p131">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2. The function returns a string **XLOPER**, version, which can then be coerced to an integer. The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect. For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5831-311">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5831-311">See also</span></span>

- [<span data-ttu-id="f5831-312">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="f5831-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="f5831-313">Zugreifen auf XLL-Code in Excel</span><span class="sxs-lookup"><span data-stu-id="f5831-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="f5831-314">Excel XLL SDK – API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="f5831-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="f5831-315">C-API-Rückruffunktionen Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="f5831-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="f5831-316">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="f5831-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

