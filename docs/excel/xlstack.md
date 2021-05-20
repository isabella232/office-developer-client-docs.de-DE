---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429979"
---
# <a name="xlstack"></a><span data-ttu-id="3f3da-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="3f3da-104">xlStack</span></span>

<span data-ttu-id="3f3da-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f3da-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f3da-106">Überprüft den Speicherplatz, der auf dem Stapel bleibt.</span><span class="sxs-lookup"><span data-stu-id="3f3da-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="3f3da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f3da-107">Parameters</span></span>

<span data-ttu-id="3f3da-108">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f3da-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3f3da-109">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f3da-109">Property value/Return value</span></span>

<span data-ttu-id="3f3da-110">Gibt die Anzahl der Bytes (**xltypeInt**) zurück, die auf dem Stapel bleiben.</span><span class="sxs-lookup"><span data-stu-id="3f3da-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f3da-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f3da-111">Remarks</span></span>

<span data-ttu-id="3f3da-112">Die Menge des verfügbaren Stapelspeichers der letzten Versionen überläuft die 16-Bit-signierte ganze Zahl der **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="3f3da-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="3f3da-113">Dies bedeutet, **dass xlStack** einen Wert zwischen -32767 und 32768 zurückgeben kann, wenn er mithilfe von **XLOPER** s und **Excel4** oder **Excel4v** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f3da-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER** s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="3f3da-114">Um in diesem Fall den richtigen Wert zu erhalten, müssen Sie den zurückgegebenen Wert in eine nicht signierte Short umgedumst haben.</span><span class="sxs-lookup"><span data-stu-id="3f3da-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="3f3da-115">Ab Excel 2007 sollten Sie diese Funktion mithilfe von **XLOPER12** s und **Excel12** oder **Excel12v** aufrufen, in diesem Fall ist der zurückgegebene Wert der verfügbare Stapelspeicher oder 64 KB, unabhängig davon, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="3f3da-115">Starting in Excel 2007, you should call this function using **XLOPER12** s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="3f3da-116">Excel verfügt über einen begrenzten Speicherplatz auf dem Stapel, und Sie sollten darauf achten, diesen Speicherplatz nicht zu überziehen.</span><span class="sxs-lookup"><span data-stu-id="3f3da-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="3f3da-117">Legen Sie niemals sehr große Datenstrukturen auf den Stapel, und legen Sie so viele lokale Variablen wie möglich statisch fest.</span><span class="sxs-lookup"><span data-stu-id="3f3da-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="3f3da-118">Vermeiden Sie rekursives Aufrufen von Funktionen, da dadurch der Stapel schnell auffüllt wird.</span><span class="sxs-lookup"><span data-stu-id="3f3da-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="3f3da-119">Wenn Sie vermuten, dass Sie den Stapel überlaufen, rufen Sie diese Funktion häufig auf, um zu sehen, wie viel Stapelspeicherplatz übrig bleibt.</span><span class="sxs-lookup"><span data-stu-id="3f3da-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="3f3da-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f3da-120">Example</span></span>

<span data-ttu-id="3f3da-121">Im ersten Beispiel wird eine Benachrichtigung angezeigt, die die Menge an Stapelspeicherplatz enthält, die in enthalten  `\SAMPLES\EXAMPLE\EXAMPLE.C` ist.</span><span class="sxs-lookup"><span data-stu-id="3f3da-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="3f3da-122">Im zweiten Beispiel wird dasselbe Beispiel verwendet, das **mit XLOPER** s arbeitet und nicht im SDK-Beispielcode enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3f3da-122">The second example does the same thing, working with **XLOPER** s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3f3da-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f3da-123">See also</span></span>

- [<span data-ttu-id="3f3da-124">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="3f3da-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

