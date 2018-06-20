---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- Xlsheetnm-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790622"
---
# <a name="xlsheetnm"></a><span data-ttu-id="4342d-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="4342d-104">xlSheetNm</span></span>

<span data-ttu-id="4342d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4342d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4342d-106">Gibt den Namen des ein Arbeitsblatt oder eine Makrovorlage aus der internen Blatt-ID, die ein externer Verweis oder den Namen des aktuellen Blatts enthaltenen, wenn einen internen Verweis übergeben zurück.</span><span class="sxs-lookup"><span data-stu-id="4342d-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="4342d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4342d-107">Parameters</span></span>

<span data-ttu-id="4342d-108">_pxExtref_ (**XltypeRef** oder **XltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="4342d-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="4342d-109">Ein Verweis auf das Blatt, deren Namen Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="4342d-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="4342d-110">Wenn Sie einen externen Verweis (**XltypeRef**) übergeben müssen sie nur die ID des Blatts enthalten.</span><span class="sxs-lookup"><span data-stu-id="4342d-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="4342d-111">Die Datenstrukturen, die die Zellen im Arbeitsblatt beschreiben werden ignoriert und müssen nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4342d-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="4342d-112">Wenn die ID 0 (null) festgelegt ist, wird der Name des das aktuelle Blatt von **XlSheetNm** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4342d-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="4342d-113">Wenn Sie einen internen Verweis (**XltypeSef**) übergeben, wird der Name des aktuellen Blatts von **XlSheetNm** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4342d-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4342d-114">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4342d-114">Property value/Return value</span></span>

<span data-ttu-id="4342d-115">Gibt den Namen des Blatts (**XltypeStr**) in das Formular `[Book1]Sheet1`.</span><span class="sxs-lookup"><span data-stu-id="4342d-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="4342d-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4342d-116">Example</span></span>

<span data-ttu-id="4342d-117">Das folgende Beispiel zeigt den Namen des Blatts, von dem die Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="4342d-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="4342d-118">Die Funktion funktioniert nur, wenn Sie von einem Makroblatt aufgerufen wird, während der Ausführung eines XLM-Makros Befehl.</span><span class="sxs-lookup"><span data-stu-id="4342d-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="4342d-119">Dies ist, da es aufruft, **XlcAlert**, die nur Befehle führen können, und sie muss von einem Blatt statt ein Dialogfeld, im Menü oder Befehlsleiste in der Reihenfolge für **XlfCaller** zum Zurückgeben eines Verweises aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4342d-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="4342d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4342d-120">See also</span></span>

- [<span data-ttu-id="4342d-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="4342d-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="4342d-122">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="4342d-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

