---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- XlGetHwnd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790618"
---
# <a name="xlgethwnd"></a><span data-ttu-id="986ea-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="986ea-104">xlGetHwnd</span></span>

<span data-ttu-id="986ea-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="986ea-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="986ea-106">Gibt den Fensterhandle des Fensters auf oberster Ebene Microsoft Excel zurück.</span><span class="sxs-lookup"><span data-stu-id="986ea-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="986ea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="986ea-107">Parameters</span></span>

<span data-ttu-id="986ea-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="986ea-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="986ea-109">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="986ea-109">Property value/Return value</span></span>

<span data-ttu-id="986ea-110">Enthält das Handle des Fensters (**vom Typ XltypeInt**) im Feld **val.w** .</span><span class="sxs-lookup"><span data-stu-id="986ea-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="986ea-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="986ea-111">Remarks</span></span>

<span data-ttu-id="986ea-112">Diese Funktion ist hilfreich für das Schreiben von Code für Windows-API.</span><span class="sxs-lookup"><span data-stu-id="986ea-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="986ea-113">Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, wird die zurückgegebene XLOPER ganzzahlige Variable einer signierten 16-Bit-short int Dies ist nur die unteren 16 Bits der 32-Bit-Windows-Handle enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="986ea-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="986ea-114">Damit oberer Teil ermittelt wird, muss alle geöffneten Fenster Nachrichtensymbol eine Übereinstimmung mit den unteren Teil des Codes durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="986ea-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="986ea-115">Ab Excel 2007, die ganzzahlige Variable der **XLOPER12** ist eine signierte 32-Bit-Int und aus diesem Grund enthält das gesamte Handle, entfernen alle geöffneten Fenster durchlaufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="986ea-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="986ea-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="986ea-116">Example</span></span>

<span data-ttu-id="986ea-117">Anzeigen des Codes für die [fShowDialog-Funktion](fshowdialog.md) in `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="986ea-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="986ea-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="986ea-118">See also</span></span>

- [<span data-ttu-id="986ea-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="986ea-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="986ea-120">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="986ea-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

