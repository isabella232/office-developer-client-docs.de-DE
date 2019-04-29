---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428130"
---
# <a name="xlgetinst"></a><span data-ttu-id="1cbe4-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="1cbe4-104">xlGetInst</span></span>

 <span data-ttu-id="1cbe4-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1cbe4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1cbe4-106">Gibt den Instanz-Handle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="1cbe4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cbe4-107">Parameters</span></span>

<span data-ttu-id="1cbe4-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1cbe4-109">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cbe4-109">Property value/Return value</span></span>

<span data-ttu-id="1cbe4-110">Der Instanz-handle (**xltypeInt**) befindet sich im **Val. w** -Feld.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1cbe4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cbe4-111">Remarks</span></span>

<span data-ttu-id="1cbe4-112">Diese Funktion kann verwendet werden, um zwischen mehreren laufenden Instanzen von Excel zu unterscheiden, die die DLL aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="1cbe4-113">Wenn Sie diese Funktion mithilfe von [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, handelt es sich bei der zurückgegebenen XLOPER-ganzzahligen Variablen um einen signierten 16-Bit-short-int-Wert. Dies kann nur die niedrigen 16 Bits des Windows-Handles von 32-Bit enthalten.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="1cbe4-114">Beginnend mit Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit int und enthält daher das gesamte handle, sodass nicht alle geöffneten Fenster durchlaufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1cbe4-115">Wenn die **xlGetInst** -Funktion mit der 64-Bit-Version von Microsoft Excel verwendet wird, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="1cbe4-116">Der Grund ist, dass der **xltypeInt** -Werttyp nicht breit genug ist, um das von Excel zurückgegebene 64-Bit Long-Handle in diesem Fall zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="1cbe4-117">Zu diesem Zweck hat Excel 2010 eine neue Funktion namens [xlGetInstPtr](xlgetinstptr.md)eingeführt, die sowohl mit der 32-Bit-als auch der 64-Bit-Version von Excel ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1cbe4-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1cbe4-118">Example</span></span>

<span data-ttu-id="1cbe4-119">Im folgenden Beispiel wird die Instanz der letzten Excel-Kopie, die Sie aufgerufen hat, mit der aktuellen Excel-Kopie verglichen, die Sie aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="1cbe4-120">Wenn Sie identisch sind, wird 1 zurückgegeben; Wenn dies nicht der Fall ist, wird 0 zurückgegeben; Wenn die Funktion fehlschlägt, gibt Sie-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="1cbe4-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="1cbe4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cbe4-121">See also</span></span>



[<span data-ttu-id="1cbe4-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="1cbe4-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="1cbe4-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="1cbe4-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="1cbe4-124">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="1cbe4-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

