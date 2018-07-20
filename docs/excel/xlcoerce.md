---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- XlCoerce-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790599"
---
# <a name="xlcoerce"></a><span data-ttu-id="02d87-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="02d87-104">xlCoerce</span></span>

 <span data-ttu-id="02d87-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02d87-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="02d87-106">Konvertiert einen Typ von **XLOPER**/ **XLOPER12** in eine andere oder sucht Werte von Zellen in einem Blatt.</span><span class="sxs-lookup"><span data-stu-id="02d87-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="02d87-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02d87-107">Parameters</span></span>

 <span data-ttu-id="02d87-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="02d87-108">_pxSource_</span></span>
  
<span data-ttu-id="02d87-109">Die Quelle **XLOPER**/ **XLOPER12** , die konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="02d87-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="02d87-110">_pxDestType_ (**vom Typ XltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="02d87-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="02d87-111">(Optional).</span><span class="sxs-lookup"><span data-stu-id="02d87-111">(Optional).</span></span> <span data-ttu-id="02d87-112">Eine Bitmaske der resultierenden Typen sind Sie bereit, akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="02d87-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="02d87-113">Sie sollten den bitweisen **OR** -Operator (|) verwenden, um mehrere möglichen Typen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="02d87-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="02d87-114">Wenn dieses Argument ausgelassen wird, werden Verweise auf einzelne Zellen konvertiert auf eine der der Wert Typen **XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeNil** (wenn die genannten Zelle leer ist) und Verweise auf blockiert Zellen werden in **XltypeMulti**konvertiert.</span><span class="sxs-lookup"><span data-stu-id="02d87-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="02d87-115">Auf diese Weise **XlCoerce** Weise Zellwerten nachzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="02d87-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="02d87-116">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02d87-116">Property value/Return value</span></span>

<span data-ttu-id="02d87-117">Gibt den umgewandelten Wert (**XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeNil**oder **XltypeMulti**) zurück.</span><span class="sxs-lookup"><span data-stu-id="02d87-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02d87-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02d87-118">Remarks</span></span>

 <span data-ttu-id="02d87-119">**XlCoerce** kann nicht zu oder von **XltypeBigData** oder **XltypeFlow**konvertiert.</span><span class="sxs-lookup"><span data-stu-id="02d87-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="02d87-120">Übergeben einen Typ **XltypeMissing** oder **XltypeNil** als _PxDestType_ entspricht das Argument auslassen.</span><span class="sxs-lookup"><span data-stu-id="02d87-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="02d87-121">In einigen Fällen kann Konvertierung fehl.</span><span class="sxs-lookup"><span data-stu-id="02d87-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="02d87-122">Beispielsweise können einige Zeichenfolgen in Zahlen, konvertiert werden, während andere Benutzer können.</span><span class="sxs-lookup"><span data-stu-id="02d87-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="02d87-123">Wenn ein Array oder ein mit mehreren Zellbezug zu einem einzelnen Wert umgewandelt wird, ist das Ergebnis der Wert des oberen linken Zelle oder Array-Elements an.</span><span class="sxs-lookup"><span data-stu-id="02d87-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="02d87-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02d87-124">Example</span></span>

<span data-ttu-id="02d87-125">Der folgende Code finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="02d87-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="02d87-126">Die Funktion **XlcAlert** versucht implizit Argument in eine Zeichenfolge zu konvertieren, damit der hier gezeigte Koersion Schritt tatsächlich entfernt konnte und **xInt** direkt an **XlcAlert**übergeben werden konnte.</span><span class="sxs-lookup"><span data-stu-id="02d87-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="02d87-127">Wie **XlcAlert** ein Makro mit Befehlen ist, funktioniert diesen Code nur ordnungsgemäß Wenn von einem Makroblatt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="02d87-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="02d87-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02d87-128">See also</span></span>



[<span data-ttu-id="02d87-129">gleich xlSet</span><span class="sxs-lookup"><span data-stu-id="02d87-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="02d87-130">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="02d87-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

