---
title: XlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Xladdinmanagerinfo-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790573"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="7436e-104">XlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="7436e-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="7436e-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7436e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7436e-106">Wird von Microsoft Excel aufgerufen, wenn der Add-In-Manager zum ersten Mal in einer Excel-Sitzung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7436e-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="7436e-107">Diese Funktion wird das Add-In-Manager Informationen über das Add-in bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7436e-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="7436e-108">Excel 2007 und spätere Versionen aufrufen **xlAddInManagerInfo12** anstelle von **XlAddInManagerInfo** , wenn durch die XLL exportiert.</span><span class="sxs-lookup"><span data-stu-id="7436e-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="7436e-109">Die Funktion **xlAddInManagerInfo12** sollte auf die gleiche Weise als **XlAddInManagerInfo** zur Vermeidung von versionsspezifischen Unterschiede im Verhalten von XLL funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7436e-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="7436e-110">Excel erwartet **xlAddInManagerInfo12** einen **XLOPER12** -Datentyp zurück, während ein **XLOPER** **XlAddInManagerInfo** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7436e-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="7436e-111">Die **xlAddInManagerInfo12** -Funktion wird nicht von früheren Versionen von Excel als Excel 2007 aufgerufen, wie diese **XLOPER12**nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7436e-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="7436e-112">Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7436e-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="7436e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7436e-113">Parameters</span></span>

 <span data-ttu-id="7436e-114">_PxAction:_ Ein Zeiger auf eine numerische **XLOPER/XLOPER12** (**vom Typ XltypeInt** oder **XltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="7436e-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="7436e-115">Die Informationen, der für Excel Listenbereich anfordert.</span><span class="sxs-lookup"><span data-stu-id="7436e-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7436e-116">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7436e-116">Property value/Return value</span></span>

<span data-ttu-id="7436e-117">_PxAction_ umgewandelt werden kann, um die Zahl 1 oder ist, sollte die Implementierung von dieser Funktion eine Zeichenfolge mit einige Informationen über das Add-in, in der Regel seinen Namen und möglicherweise eine Versionsnummer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7436e-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="7436e-118">Andernfalls sollte es #VALUE zurück!.</span><span class="sxs-lookup"><span data-stu-id="7436e-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="7436e-119">Wenn Sie keine Zeichenfolge zurückzugeben, versucht Excel den zurückgegebenen Wert in eine Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7436e-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7436e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7436e-120">Remarks</span></span>

<span data-ttu-id="7436e-121">Wenn die zurückgegebene Zeichenfolge an dynamisch zugewiesenen Puffer verweist, müssen Sie sicherstellen, dass dieser Puffer schließlich freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7436e-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="7436e-122">Wenn die Zeichenfolge von Excel belegt wurde, Sie zu diesem Zweck **XlbitXLFree**festlegen.</span><span class="sxs-lookup"><span data-stu-id="7436e-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="7436e-123">Wenn die Zeichenfolge von der DLL belegt wurde, zu diesem Zweck Einstellung **XlbitDLLFree**und müssen Sie auch in implementieren [XlAutoFree](xlautofree-xlautofree12.md) (Wenn Sie eine **XLOPER**zurückgeben) oder **xlAutoFree12** (Wenn Sie eine **XLOPER12**zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="7436e-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="7436e-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7436e-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="7436e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7436e-125">See also</span></span>



[<span data-ttu-id="7436e-126">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7436e-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

