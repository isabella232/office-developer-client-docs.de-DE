---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405282"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="52cec-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="52cec-103">xlGetInstPtr</span></span>

<span data-ttu-id="52cec-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52cec-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52cec-105">Gibt den Instanz-Handle der Instanz von Microsoft Excel zurück, die derzeit eine DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="52cec-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="52cec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52cec-106">Parameters</span></span>

<span data-ttu-id="52cec-107">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="52cec-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="52cec-108">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52cec-108">Property value/Return value</span></span>

<span data-ttu-id="52cec-109">Der Instanzen Handler (**xltypeBigData**) befindet sich im Feld **Val. hdata. h.** .</span><span class="sxs-lookup"><span data-stu-id="52cec-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="52cec-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52cec-110">Remarks</span></span>

<span data-ttu-id="52cec-111">Diese Funktion kann verwendet werden, um zwischen mehreren laufenden Instanzen von Excel zu unterscheiden, die die DLL aufrufen.</span><span class="sxs-lookup"><span data-stu-id="52cec-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="52cec-112">Diese Funktion gibt einen korrekten Wert mit sowohl 32-Bit-als auch 64-Bit-Versionen von Excel zurück.</span><span class="sxs-lookup"><span data-stu-id="52cec-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="52cec-113">Es wurde in Excel 2010 als Erweiterung der [xlGetInst](xlgetinst.md) -Funktion eingeführt, die nur mit 32-Bit-Versionen von Excel ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="52cec-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="52cec-114">Diese Funktion funktioniert ordnungsgemäß, wenn Sie aufgerufen wird, indem sowohl die [Excel4-als auch die Excel12](excel4-excel12.md) -Vielzahl der API-Rückruffunktionen verwendet wird, da sowohl **XLOPER** als auch **XLOPER12** die gleiche Struktur aufweisen, die den **xltypeBigData** -Wert unterstützt. Typ.</span><span class="sxs-lookup"><span data-stu-id="52cec-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="52cec-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52cec-115">Example</span></span>

<span data-ttu-id="52cec-116">Im folgenden Beispiel wird die Instanz der letzten Excel-Kopie, die Sie aufgerufen hat, mit der aktuellen Excel-Kopie verglichen, die Sie aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="52cec-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="52cec-117">Wenn Sie identisch sind, wird 1 zurückgegeben; Wenn dies nicht der Fall ist, wird 0 zurückgegeben; Wenn die Funktion fehlschlägt, gibt Sie-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="52cec-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="52cec-118">Dieses Beispiel funktioniert sowohl mit 32-als auch 64-Bit-Versionen von Excel.</span><span class="sxs-lookup"><span data-stu-id="52cec-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="52cec-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52cec-119">See also</span></span>

- [<span data-ttu-id="52cec-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="52cec-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="52cec-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="52cec-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="52cec-122">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="52cec-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

