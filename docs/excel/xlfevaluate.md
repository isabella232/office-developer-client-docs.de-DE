---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439184"
---
# <a name="xlfevaluate"></a><span data-ttu-id="5ea50-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="5ea50-104">xlfEvaluate</span></span>

 <span data-ttu-id="5ea50-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ea50-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ea50-106">Verwendet den Microsoft Excel parser und den Funktionsevaluator, um einen beliebigen Ausdruck auszuwerten, der in eine Arbeitsblattzelle eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ea50-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="5ea50-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea50-107">Parameters</span></span>

 <span data-ttu-id="5ea50-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="5ea50-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="5ea50-109">Die zu bewertende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ea50-109">The string to be evaluated.</span></span> <span data-ttu-id="5ea50-110">Ein führendes Gleichheitszeichen (=) ist optional.</span><span class="sxs-lookup"><span data-stu-id="5ea50-110">A leading equal sign (=) is optional.</span></span> <span data-ttu-id="5ea50-111">Die Zeichenfolge kann ein beliebiger Text sein, der legal in eine Arbeitsblatt- oder Makroblattzelle eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ea50-111">The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ea50-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ea50-112">Property value/Return value</span></span>

<span data-ttu-id="5ea50-113">Gibt das Ergebnis der Auswertung der Zeichenfolge zurück, die einen der Typen **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti** sein kann.</span><span class="sxs-lookup"><span data-stu-id="5ea50-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ea50-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ea50-114">Remarks</span></span>

<span data-ttu-id="5ea50-115">Die Zeichenfolge kann nur Funktionen und keine Befehlsäquivalente enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ea50-115">The string can contain only functions, not command equivalents.</span></span> <span data-ttu-id="5ea50-116">Sie entspricht dem Drücken von **F9 aus** der Formelleiste.</span><span class="sxs-lookup"><span data-stu-id="5ea50-116">It is equivalent to pressing **F9** from the formula bar.</span></span> <span data-ttu-id="5ea50-117">Wenn **xlfEvaluate** von einer XLL-Arbeitsblattfunktion aufgerufen wird, die als threadsicher registriert wurde, darf der Ausdruck nur threadsichere Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ea50-117">If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="5ea50-118">Die primäre Verwendung der **xlfEvaluate-Funktion** besteht in der Möglichkeit, DLLs das Aufschlüsseln des Werts zu ermöglichen, der einem definierten Namen zugewiesen ist, der sich entweder auf einem Blatt oder einem in der DLL definierten ausgeblendeten Namen befindet.</span><span class="sxs-lookup"><span data-stu-id="5ea50-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="5ea50-119">Beachten Sie, dass einem Arbeitsblattnamen in einer DLL/XLL mindestens ein Ausrufezeichen (!) vorangestellt werden muss, um sicherzustellen, dass er als außerhalb der DLL interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="5ea50-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="5ea50-120">Weitere Informationen finden Sie unter [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="5ea50-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="5ea50-121">**xlfEvaluate** kann nicht zum Auswerten von Verweisen auf ein externes Blatt verwendet werden, das nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5ea50-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ea50-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ea50-122">Example</span></span>

<span data-ttu-id="5ea50-123">In diesem Beispiel **wird xlfEvaluate** verwendet, um den Text "! B38" zum Inhalt der Zelle B38.</span><span class="sxs-lookup"><span data-stu-id="5ea50-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="5ea50-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="5ea50-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="5ea50-125">Diese Funktion ruft ein Befehlsmakro (**xlcAlert**) auf und funktioniert nur dann ordnungsgemäß, wenn sie von einem Makroblatt oder als Makrobefehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5ea50-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="5ea50-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea50-126">See also</span></span>

- [<span data-ttu-id="5ea50-127">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ea50-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

