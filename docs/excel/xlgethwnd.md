---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425456"
---
# <a name="xlgethwnd"></a><span data-ttu-id="4155e-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="4155e-104">xlGetHwnd</span></span>

<span data-ttu-id="4155e-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4155e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4155e-106">Gibt das Fensterhandle des Fensters auf oberster Microsoft Excel zurück.</span><span class="sxs-lookup"><span data-stu-id="4155e-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="4155e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4155e-107">Parameters</span></span>

<span data-ttu-id="4155e-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="4155e-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4155e-109">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4155e-109">Property value/Return value</span></span>

<span data-ttu-id="4155e-110">Enthält das Fensterhandle (**xltypeInt**) im **Feld val.w.**</span><span class="sxs-lookup"><span data-stu-id="4155e-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4155e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4155e-111">Remarks</span></span>

<span data-ttu-id="4155e-112">Diese Funktion ist nützlich, um Windows-API-Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4155e-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="4155e-113">Wenn Sie diese Funktion mithilfe von [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, ist die zurückgegebene XLOPER-Ganzzahlvariable eine signierte 16-Bit-Short-Int. Dies kann nur die niedrigen 16 Bit des 32-Bit-Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="4155e-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="4155e-114">Um den hohen Teil zu finden, muss Ihr Code alle geöffneten Fenster durch iterieren, die nach einer Übereinstimmung mit dem niedrigen Teil suchen.</span><span class="sxs-lookup"><span data-stu-id="4155e-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="4155e-115">Ab Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit-Int und enthält daher das gesamte Handle, ohne dass alle geöffneten Fenster durch iteriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4155e-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="4155e-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4155e-116">Example</span></span>

<span data-ttu-id="4155e-117">Weitere Informationen finden Sie im Code für [die fShowDialog-Funktion](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="4155e-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4155e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4155e-118">See also</span></span>

- [<span data-ttu-id="4155e-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="4155e-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="4155e-120">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="4155e-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

