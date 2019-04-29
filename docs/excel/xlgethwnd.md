---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlGetHwnd-Funktion [Excel 2007]
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
# <a name="xlgethwnd"></a><span data-ttu-id="5b952-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="5b952-104">xlGetHwnd</span></span>

<span data-ttu-id="5b952-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5b952-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5b952-106">Gibt das Fensterhandle des Microsoft Excel-Fensters auf oberster Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="5b952-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="5b952-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b952-107">Parameters</span></span>

<span data-ttu-id="5b952-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="5b952-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5b952-109">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b952-109">Property value/Return value</span></span>

<span data-ttu-id="5b952-110">Enthält das Fensterhandle (**xltypeInt**) im Feld **Val. w** .</span><span class="sxs-lookup"><span data-stu-id="5b952-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b952-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b952-111">Remarks</span></span>

<span data-ttu-id="5b952-112">Diese Funktion ist nützlich, um Windows-API-Code zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5b952-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="5b952-113">Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, handelt es sich bei der zurückgegebenen XLOPER-ganzzahligen Variablen um einen signierten 16-Bit-short-int-Wert. Dies kann nur die niedrigen 16 Bits des Windows-Handles von 32-Bit enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b952-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="5b952-114">Um den hohen Anteil zu ermitteln, muss der Code alle geöffneten Fenster durchlaufen, um eine Übereinstimmung mit dem niedrigen Webpart zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5b952-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="5b952-115">Beginnend mit Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit int und enthält daher das gesamte handle, sodass nicht alle geöffneten Fenster durchlaufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5b952-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="5b952-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b952-116">Example</span></span>

<span data-ttu-id="5b952-117">Weitere Informationen finden Sie im Code für die `SAMPLES\GENERIC\GENERIC.C`fShowDialog- [Funktion](fshowdialog.md) in.</span><span class="sxs-lookup"><span data-stu-id="5b952-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b952-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b952-118">See also</span></span>

- [<span data-ttu-id="5b952-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="5b952-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="5b952-120">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="5b952-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

