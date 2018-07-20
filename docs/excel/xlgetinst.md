---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Xlgetinst-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790605"
---
# <a name="xlgetinst"></a><span data-ttu-id="33b96-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="33b96-104">xlGetInst</span></span>

 <span data-ttu-id="33b96-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="33b96-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="33b96-106">Gibt die Instanzzugriffsnummer der Instanz von Microsoft Excel, die derzeit eine DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="33b96-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="33b96-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="33b96-107">Parameters</span></span>

<span data-ttu-id="33b96-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="33b96-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="33b96-109">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33b96-109">Property value/Return value</span></span>

<span data-ttu-id="33b96-110">Die Instanzzugriffsnummer (**vom Typ XltypeInt**) werden im Feld **val.w** .</span><span class="sxs-lookup"><span data-stu-id="33b96-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="33b96-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33b96-111">Remarks</span></span>

<span data-ttu-id="33b96-112">Diese Funktion kann mehrere ausgeführten Instanzen von Excel unterscheiden, die die DLL aufruft, sind verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33b96-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="33b96-113">Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, wird die zurückgegebene XLOPER ganzzahlige Variable einer signierten 16-Bit-short int Dies ist nur die unteren 16 Bits der 32-Bit-Windows-Handle enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="33b96-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="33b96-114">Ab Excel 2007, die ganzzahlige Variable der **XLOPER12** ist eine signierte 32-Bit-Int und aus diesem Grund enthält das gesamte Handle, entfernen alle geöffneten Fenster durchlaufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="33b96-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="33b96-115">Wenn die **XlGetInst** -Funktion mit der 64-Bit-Version von Microsoft Excel verwendet wird, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="33b96-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="33b96-116">Dies ist, da der Werttyp **vom Typ XltypeInt** nicht breit genug für das lange 64-Bit-Handle zurückgegeben von Excel in diesem Fall enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="33b96-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="33b96-117">Für diesen Zweck eingeführt Excel 2010 eine neue Funktion mit dem Namen [XlGetInstPtr](xlgetinstptr.md), der mit der 32-Bit- und 64-Bit-Versionen von Excel ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33b96-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="33b96-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="33b96-118">Example</span></span>

<span data-ttu-id="33b96-119">Das folgende Beispiel vergleicht die Instanz der letzten Kopie von Excel, die sie an der aktuellen Version von Excel aufgerufen, die diese aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="33b96-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="33b96-120">Wenn sie identisch sind, gibt 1 zurück. Wenn dies nicht der Fall ist, sie gibt 0 zurück; Wenn die Funktion fehlschlägt, gibt-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="33b96-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="33b96-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b96-121">See also</span></span>



[<span data-ttu-id="33b96-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="33b96-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="33b96-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="33b96-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="33b96-124">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="33b96-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

