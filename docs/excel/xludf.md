---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430644"
---
# <a name="xludf"></a><span data-ttu-id="3f7fd-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="3f7fd-104">xlUDF</span></span>

<span data-ttu-id="3f7fd-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f7fd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f7fd-106">Ruft eine benutzerdefinierte Funktion (USERF) auf.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="3f7fd-107">Mit dieser Funktion kann eine DLL Visual Basic for Applications (VBA) benutzerdefinierte Funktionen, XLM-Makrosprachenfunktionen und registrierte Funktionen aufrufen, die in anderen Add-Ins enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="3f7fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f7fd-108">Parameters</span></span>

<span data-ttu-id="3f7fd-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** oder **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="3f7fd-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="3f7fd-110">Der Verweis auf die Funktion, die Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-110">The reference of the function you want to call.</span></span> <span data-ttu-id="3f7fd-111">Dies kann ein Makroblattzellenverweis, der registrierte Name der Funktion als Zeichenfolge oder die Register-ID der Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="3f7fd-112">Für XLL-Add-In-Funktionen, die mithilfe von **xlfRegister** oder **REGISTER** mit dem angegebenen Argument  _pxFunctionText_ registriert wurden, kann die ID mithilfe von **xlfEvaluate** zum Suchen nach dem Namen erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="3f7fd-113">_pxArg1, ..._</span><span class="sxs-lookup"><span data-stu-id="3f7fd-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="3f7fd-114">Null oder mehr Argumente für die benutzerdefinierte Funktion.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="3f7fd-115">Wenn Sie diese Funktion in Versionen vor Excel 2007 aufrufen, ist die maximale Anzahl zusätzlicher Argumente, die übergeben werden können, 29, d. h. 30 einschließlich _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="3f7fd-116">Ab Excel 2007 wird dieser Grenzwert auf 254 angehoben, d. h. 255 einschließlich _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3f7fd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f7fd-117">Return value</span></span>

<span data-ttu-id="3f7fd-118">Gibt den von der benutzerdefinierten Funktion zurückgegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="3f7fd-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f7fd-119">Example</span></span>

<span data-ttu-id="3f7fd-120">Im folgenden Beispiel wird **TestMacro auf** Blatt Macro1 in BOOK1.XLS.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="3f7fd-121">Stellen Sie sicher, dass sich das Makro auf einem Blatt mit dem Namen "Macro1" befindet.</span><span class="sxs-lookup"><span data-stu-id="3f7fd-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3f7fd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f7fd-122">See also</span></span>

- [<span data-ttu-id="3f7fd-123">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="3f7fd-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

