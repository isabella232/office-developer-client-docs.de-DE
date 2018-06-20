---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- XlStack-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790613"
---
# <a name="xlstack"></a><span data-ttu-id="02f70-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="02f70-104">xlStack</span></span>

<span data-ttu-id="02f70-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02f70-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="02f70-106">Überprüft die Menge freier Speicherplatz auf dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="02f70-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="02f70-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02f70-107">Parameters</span></span>

<span data-ttu-id="02f70-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="02f70-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="02f70-109">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02f70-109">Property value/Return value</span></span>

<span data-ttu-id="02f70-110">Gibt die Anzahl von Bytes (**vom Typ XltypeInt**) auf dem Stapel verbleibenden zurück.</span><span class="sxs-lookup"><span data-stu-id="02f70-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02f70-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02f70-111">Remarks</span></span>

<span data-ttu-id="02f70-112">Die Menge an verfügbaren Stapelspeicher aktueller Versionen überschreitet die 16-Bit-Ganzzahl mit Vorzeichen von der **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="02f70-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="02f70-113">Dies bedeutet, dass diese **XlStack** einen Wert zwischen-32767 und 32768 bei einem Aufruf mit **XLOPER**s und **Excel4** oder **Excel4v**zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="02f70-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="02f70-114">Um müssen den richtigen Wert in diesem Fall abzurufen, Sie den zurückgegebenen Wert in eine nicht signierte kurze umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="02f70-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="02f70-115">Starten in Excel 2007, müssen Sie diese Funktion mithilfe von **XLOPER12**s und **Excel12** aufrufen oder **Excel12v**, in dem Fall den zurückgegebenen Wert Stack verfügbaren Speicherplatz oder 64 KB, ist der kleinere der Werte ist.</span><span class="sxs-lookup"><span data-stu-id="02f70-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="02f70-116">Excel verfügt über eine begrenzte Menge an Speicherplatz auf dem Stapel und sollte nicht zum Überschreitung dieses Speicherplatz sorgfältig.</span><span class="sxs-lookup"><span data-stu-id="02f70-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="02f70-117">Sehr große Datenstrukturen nie auf dem Stapel zu platzieren und wie viele lokale Variablen möglichst statische erleichtern.</span><span class="sxs-lookup"><span data-stu-id="02f70-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="02f70-118">Vermeiden Sie die Funktionen rekursiv aufrufen, da, die den Stapel schnell gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="02f70-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="02f70-119">Wenn Sie annehmen, dass Sie den Stapel dieses sind, rufen Sie diese Funktion häufig, um festzustellen, wie viel Speicherplatz bleibt.</span><span class="sxs-lookup"><span data-stu-id="02f70-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="02f70-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02f70-120">Example</span></span>

<span data-ttu-id="02f70-121">Im ersten Beispiel wird eine Meldung mit der Menge an Speicherplatz Stack und in enthalten ist `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="02f70-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="02f70-122">Im zweite Beispiel werden dieselben, arbeiten mit **XLOPER**s und nicht in der SDK-Beispiel-Code enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="02f70-122">The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="02f70-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02f70-123">See also</span></span>

- [<span data-ttu-id="02f70-124">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="02f70-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

