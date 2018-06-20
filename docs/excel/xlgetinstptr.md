---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790617"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="3576f-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="3576f-103">xlGetInstPtr</span></span>

<span data-ttu-id="3576f-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3576f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3576f-105">Gibt die Instanzzugriffsnummer der Instanz von Microsoft Excel, die derzeit eine DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="3576f-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="3576f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3576f-106">Parameters</span></span>

<span data-ttu-id="3576f-107">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="3576f-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3576f-108">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3576f-108">Property value/Return value</span></span>

<span data-ttu-id="3576f-109">Die Instanzzugriffsnummer (**XltypeBigData**) werden im Feld **val.bigdata.h.hdata** .</span><span class="sxs-lookup"><span data-stu-id="3576f-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3576f-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3576f-110">Remarks</span></span>

<span data-ttu-id="3576f-111">Diese Funktion kann mehrere ausgeführten Instanzen von Excel unterscheiden, die die DLL aufruft, sind verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3576f-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="3576f-112">Diese Funktion gibt den richtigen Wert mit 32-Bit- und 64-Bit-Versionen von Excel.</span><span class="sxs-lookup"><span data-stu-id="3576f-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="3576f-113">Es wurde in Excel 2010 als Erweiterung der Funktion [XlGetInst](xlgetinst.md) eingeführt die ordnungsgemäß nur mit 32-Bit-Versionen von Excel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3576f-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="3576f-114">Diese Funktion funktioniert ordnungsgemäß, wenn sie mithilfe der [Excel4 und Excel12](excel4-excel12.md) Varianten Rückruffunktionen API aufgerufen wird, da **XLOPER** und **XLOPER12** dieselbe Struktur aufweisen, die den Wert **XltypeBigData** unterstützt Geben Sie ein.</span><span class="sxs-lookup"><span data-stu-id="3576f-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3576f-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3576f-115">Example</span></span>

<span data-ttu-id="3576f-116">Das folgende Beispiel vergleicht die Instanz der letzten Kopie von Excel, die sie an der aktuellen Version von Excel aufgerufen, die diese aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3576f-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="3576f-117">Wenn sie identisch sind, gibt 1 zurück. Wenn dies nicht der Fall ist, sie gibt 0 zurück; Wenn die Funktion fehlschlägt, gibt-1 zurück.</span><span class="sxs-lookup"><span data-stu-id="3576f-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="3576f-118">Dieses Beispiel funktioniert mit 32-Bit- und 64-Bit-Versionen von Excel.</span><span class="sxs-lookup"><span data-stu-id="3576f-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3576f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3576f-119">See also</span></span>

- [<span data-ttu-id="3576f-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="3576f-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="3576f-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="3576f-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="3576f-122">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="3576f-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

