---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- Xlfevaluate-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790593"
---
# <a name="xlfevaluate"></a><span data-ttu-id="8de4c-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="8de4c-104">xlfEvaluate</span></span>

 <span data-ttu-id="8de4c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8de4c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8de4c-106">Verwendet Microsoft Excel-Parser und der Funktion Auswertung für ein beliebiger Ausdruck ausgewertet werden soll, die in einer Arbeitsblattzelle eingegeben werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8de4c-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="8de4c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de4c-107">Parameters</span></span>

 <span data-ttu-id="8de4c-108">_PxFormulaText (XltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="8de4c-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="8de4c-109">Die Zeichenfolge ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8de4c-109">The string to be evaluated.</span></span> <span data-ttu-id="8de4c-110">Ein führendes Gleichheitszeichen (=) ist optional.</span><span class="sxs-lookup"><span data-stu-id="8de4c-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="8de4c-111">Die Zeichenfolge kann Text sein, der in ein Arbeitsblatt oder Makroblatt Blatt Zelle gesetzlich eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="8de4c-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8de4c-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8de4c-112">Property value/Return value</span></span>

<span data-ttu-id="8de4c-113">Gibt das Ergebnis der Überprüfung der Zeichenfolge, die Typen **XltypeNum**, **XltypeStr**, **XltypeBool**, **XltypeErr**, **XltypeNil**, **XltypeMulti**angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="8de4c-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8de4c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8de4c-114">Remarks</span></span>

<span data-ttu-id="8de4c-115">Die Zeichenfolge kann nur Funktionen, nicht Befehl Entsprechungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8de4c-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="8de4c-116">Es ist gleichbedeutend mit dem Drücken von **F9** aus der Bearbeitungsleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8de4c-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="8de4c-117">Wenn **XlfEvaluate** eine XLL-Arbeitsblattfunktion aufgerufen wird, die als threadsicheren registriert wurde, muss der Ausdruck nur threadsicheren Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8de4c-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="8de4c-118">Die primäre Verwendung der **XlfEvaluate** -Funktion ist mit ermöglichen DLLs erhalten Sie Informationen zu einem definierten Namen, die entweder in einem Blatt zugewiesene Wert oder einen ausgeblendeten Namen in der DLL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8de4c-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="8de4c-119">Beachten Sie, dass innerhalb einer DLL/XLL, ein Arbeitsblatt mit dem Präfix werden muss mindestens ein Ausrufezeichen (!), um sicherzustellen, dass er auf die DLL als extern interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="8de4c-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="8de4c-120">Weitere Informationen finden Sie unter [Namen bewerten und andere Arbeitsblatt Formel Ausdrücke](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="8de4c-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="8de4c-121">**XlfEvaluate** kann nicht verwendet werden, um Verweise auf einem externen Blatt ausgewertet werden soll, die nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8de4c-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8de4c-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8de4c-122">Example</span></span>

<span data-ttu-id="8de4c-123">In diesem Beispiel wird die **XlfEvaluate** umzuwandelnde den Text "! B38 "auf den Inhalt der Zelle B38.</span><span class="sxs-lookup"><span data-stu-id="8de4c-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="8de4c-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="8de4c-124"></span></span> <span data-ttu-id="8de4c-125">Diese Funktion ruft ein Makro mit Befehlen (**XlcAlert**) und funktionieren ordnungsgemäß nur, wenn von einem Makroblatt oder als Makrobefehl aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8de4c-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8de4c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8de4c-126">See also</span></span>

- [<span data-ttu-id="8de4c-127">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8de4c-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

