---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407795"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="c68d8-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="c68d8-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="c68d8-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c68d8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c68d8-106">Wird von Microsoft Excel aufgerufen, wenn der Add-In-Manager zum ersten Mal in einer Excel wird.</span><span class="sxs-lookup"><span data-stu-id="c68d8-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="c68d8-107">Diese Funktion wird verwendet, um dem Add-In-Manager Informationen zu Ihrem Add-In zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="c68d8-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="c68d8-108">Excel 2007 und höher wird **xlAddInManagerInfo12** vor **xlAddInManagerInfo** angezeigt, wenn sie von der XLL exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="c68d8-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="c68d8-109">Die **xlAddInManagerInfo12-Funktion** sollte auf die gleiche Weise wie **xlAddInManagerInfo** funktionieren, um versionsspezifische Unterschiede im Verhalten der XLL zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c68d8-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="c68d8-110">Excel erwartet, **dass xlAddInManagerInfo12** einen **XLOPER12-Datentyp** zurück gibt, **während xlAddInManagerInfo** einen **XLOPER zurückgeben sollte.**</span><span class="sxs-lookup"><span data-stu-id="c68d8-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="c68d8-111">Die **xlAddInManagerInfo12-Funktion** wird nicht von Versionen von Excel vor Excel 2007 aufgerufen, da diese **xlOPER12** nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c68d8-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="c68d8-112">Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c68d8-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="c68d8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68d8-113">Parameters</span></span>

 <span data-ttu-id="c68d8-114">_pxAction:_ Ein Zeiger auf eine numerische **XLOPER/XLOPER12** (**xltypeInt** oder **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="c68d8-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="c68d8-115">Die Von Excel verlangten Informationen.</span><span class="sxs-lookup"><span data-stu-id="c68d8-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c68d8-116">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c68d8-116">Property value/Return value</span></span>

<span data-ttu-id="c68d8-117">Wenn  _pxAction_ die Zahl 1 ist oder zu ihr gecced werden kann, sollte Ihre Implementierung dieser Funktion eine Zeichenfolge zurückgeben, die einige Informationen zum Add-In enthält, in der Regel seinen Namen und möglicherweise eine Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="c68d8-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="c68d8-118">Andernfalls sollte #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="c68d8-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="c68d8-119">Wenn Sie keine Zeichenfolge zurückgeben, versucht Excel, den zurückgegebenen Wert in eine Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c68d8-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c68d8-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c68d8-120">Remarks</span></span>

<span data-ttu-id="c68d8-121">Wenn die zurückgegebene Zeichenfolge auf dynamisch zugewiesenen Puffer verweist, müssen Sie sicherstellen, dass dieser Puffer schließlich frei wird.</span><span class="sxs-lookup"><span data-stu-id="c68d8-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="c68d8-122">Wenn die Zeichenfolge von der Excel zugewiesen wurde, verwenden Sie dazu **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="c68d8-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="c68d8-123">Wenn die Zeichenfolge von der DLL zugewiesen wurde, verwenden Sie dazu **xlbitDLLFree** und müssen auch in [xlAutoFree](xlautofree-xlautofree12.md) (wenn Sie einen **XLOPER** zurückgeben) oder **xlAutoFree12** implementieren (wenn Sie einen **XLOPER12** zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="c68d8-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="c68d8-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c68d8-124">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c68d8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c68d8-125">See also</span></span>



[<span data-ttu-id="c68d8-126">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="c68d8-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

