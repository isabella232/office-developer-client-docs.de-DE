---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlCoerce-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424833"
---
# <a name="xlcoerce"></a><span data-ttu-id="57bf1-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="57bf1-104">xlCoerce</span></span>

 <span data-ttu-id="57bf1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="57bf1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="57bf1-106">Konvertiert einen Typ von **XLOPER**/ **XLOPER12** in einen anderen oder sucht Zellenwerte in einem Blatt.</span><span class="sxs-lookup"><span data-stu-id="57bf1-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="57bf1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="57bf1-107">Parameters</span></span>

 <span data-ttu-id="57bf1-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="57bf1-108">_pxSource_</span></span>
  
<span data-ttu-id="57bf1-109">Die Quell- **XLOPER**/ **XLOPER12** , die konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="57bf1-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="57bf1-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="57bf1-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="57bf1-111">(Optional).</span><span class="sxs-lookup"><span data-stu-id="57bf1-111">(Optional).</span></span> <span data-ttu-id="57bf1-112">Eine Bitmaske der resultierenden Typen, die Sie akzeptieren möchten.</span><span class="sxs-lookup"><span data-stu-id="57bf1-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="57bf1-113">Sie sollten den bitweisen **or** -Operator (|) verwenden, um mehrere mögliche Typen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="57bf1-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="57bf1-114">Wenn dieses Argument ausgelassen wird, werden Verweise auf einzelne Zellen in einen der Wertetypen **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (wenn die referenzierte Zelle leer ist) und Verweise auf Blöcke konvertiert. von Zellen werden in **xltypeMulti**konvertiert.</span><span class="sxs-lookup"><span data-stu-id="57bf1-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="57bf1-115">Damit ist **xlCoerce** die bequemste Methode zum Nachschlagen von Zellwerten.</span><span class="sxs-lookup"><span data-stu-id="57bf1-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="57bf1-116">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57bf1-116">Property value/Return value</span></span>

<span data-ttu-id="57bf1-117">Gibt den umgewandelten Wert (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**oder **xltypeMulti**) zurück.</span><span class="sxs-lookup"><span data-stu-id="57bf1-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57bf1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57bf1-118">Remarks</span></span>

 <span data-ttu-id="57bf1-119">**xlCoerce** kann nicht in oder aus **xltypeBigData** oder **xltypeFlow**konvertieren.</span><span class="sxs-lookup"><span data-stu-id="57bf1-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="57bf1-120">Das Übergeben eines **xltypeMissing** -oder **xltypeNil** -Typs als _pxDestType_ entspricht dem Weglassen des Arguments.</span><span class="sxs-lookup"><span data-stu-id="57bf1-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="57bf1-121">In einigen Fällen kann die Konvertierung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="57bf1-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="57bf1-122">Einige Zeichenfolgen können beispielsweise nicht in Zahlen konvertiert werden, andere jedoch.</span><span class="sxs-lookup"><span data-stu-id="57bf1-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="57bf1-123">Wenn ein Array oder ein mehr zellenverweis in einen einzelnen Werttyp konvertiert wird, ist das Ergebnis der Wert der oberen linken Zelle oder des Arrayelements.</span><span class="sxs-lookup"><span data-stu-id="57bf1-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="57bf1-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57bf1-124">Example</span></span>

<span data-ttu-id="57bf1-125">Den folgenden Code finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="57bf1-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="57bf1-126">Die **xlcAlert** -Funktion versucht implizit, das Argument in eine Zeichenfolge umzuwandeln, sodass der hier gezeigte Umwandlungs Schritt tatsächlich entfernt werden kann und **XInt** direkt an **xlcAlert**übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="57bf1-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="57bf1-127">Da **xlcAlert** ein Befehlsmakro ist, funktioniert dieser Code nur dann ordnungsgemäß, wenn er von einem Makroblatt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57bf1-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="57bf1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57bf1-128">See also</span></span>



[<span data-ttu-id="57bf1-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="57bf1-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="57bf1-130">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="57bf1-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

