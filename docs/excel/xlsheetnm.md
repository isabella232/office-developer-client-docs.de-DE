---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437413"
---
# <a name="xlsheetnm"></a><span data-ttu-id="c63ca-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="c63ca-104">xlSheetNm</span></span>

<span data-ttu-id="c63ca-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c63ca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c63ca-106">Gibt den Namen eines Arbeitsblatts oder Makroblatts aus seiner internen Blatt-ID zurück, die in einem externen Verweis enthalten ist, oder den Namen des aktuellen Blatts, wenn ein interner Verweis übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c63ca-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="c63ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c63ca-107">Parameters</span></span>

<span data-ttu-id="c63ca-108">_pxExtref_ (**xltypeRef** oder **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="c63ca-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="c63ca-109">Ein Verweis auf das Blatt, dessen Name Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c63ca-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="c63ca-110">Wenn Sie einen externen Verweis (**xltypeRef**) übergeben, muss er nur die ID des Blatts enthalten.</span><span class="sxs-lookup"><span data-stu-id="c63ca-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="c63ca-111">Die Datenstrukturen, die die Zellen im Arbeitsblatt beschreiben, werden ignoriert und müssen nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c63ca-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="c63ca-112">Wenn die ID auf Null festgelegt ist, **gibt xlSheetNm** den Namen des aktuellen Blatts zurück.</span><span class="sxs-lookup"><span data-stu-id="c63ca-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="c63ca-113">Wenn Sie einen internen Verweis übergeben (**xltypeSef**), **gibt xlSheetNm** den Namen des aktuellen Blatts zurück.</span><span class="sxs-lookup"><span data-stu-id="c63ca-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c63ca-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c63ca-114">Property value/Return value</span></span>

<span data-ttu-id="c63ca-115">Gibt den Namen des Blatts (**xltypeStr**) im Formular  `[Book1]Sheet1` zurück.</span><span class="sxs-lookup"><span data-stu-id="c63ca-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="c63ca-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c63ca-116">Example</span></span>

<span data-ttu-id="c63ca-117">Im folgenden Beispiel wird der Name des Blatts angezeigt, aus dem die Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c63ca-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="c63ca-118">Die Funktion funktioniert nur ordnungsgemäß, wenn sie während der Ausführung eines XLM-Befehlsmakros aus einem Makroblatt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c63ca-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="c63ca-119">Dies liegt daran, dass **xlcAlert** aufgerufen wird, was nur befehle möglich ist, und es muss von einem Blatt anstatt von einem Dialogfeld, Menü oder einer Befehlsleiste aufgerufen werden, damit **xlfCaller** einen Verweis zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="c63ca-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c63ca-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c63ca-120">See also</span></span>

- [<span data-ttu-id="c63ca-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="c63ca-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="c63ca-122">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="c63ca-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

