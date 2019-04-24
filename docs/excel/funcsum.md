---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304060"
---
# <a name="funcsum"></a><span data-ttu-id="3d41d-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="3d41d-104">FuncSum</span></span>

 <span data-ttu-id="3d41d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d41d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3d41d-106">Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die 1 bis 29 Argumente verwendet und deren Summe berechnet.</span><span class="sxs-lookup"><span data-stu-id="3d41d-106">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum.</span></span> <span data-ttu-id="3d41d-107">Jedes Argument kann eine einzelne Zahl, ein Bereich oder ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="3d41d-107">Each argument can be a single number, a range, or an array.</span></span> <span data-ttu-id="3d41d-108">Wenn generische. XLL geladen wird, wird diese Funktion registriert, sodass Sie vom Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d41d-108">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="3d41d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d41d-109">Parameters</span></span>

 <span data-ttu-id="3d41d-110">_PX1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="3d41d-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="3d41d-111">Zeiger auf **XLOPER12** -Argumente.</span><span class="sxs-lookup"><span data-stu-id="3d41d-111">Pointers to **XLOPER12** arguments.</span></span> <span data-ttu-id="3d41d-112">Die Funktion akzeptiert jede Art von Eingabetyp, ist jedoch nur codiert, um Zahlen, Literale Arrays von Zahlen und Bereichen zu verwenden, die nur Zahlen oder leere Zellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d41d-112">The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells.</span></span> <span data-ttu-id="3d41d-113">Wenn weniger als 29 Argumente angegeben werden, werden die restlichen Argumente als **xltypeMissing**angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d41d-113">If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3d41d-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d41d-114">Property value/Return value</span></span>

<span data-ttu-id="3d41d-115">(**LPXLOPER12 xltypeNum** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="3d41d-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="3d41d-116">Die Summe der Argumente oder #VALUE!</span><span class="sxs-lookup"><span data-stu-id="3d41d-116">The sum of the arguments or #VALUE!</span></span> <span data-ttu-id="3d41d-117">Wenn es sich nicht um numerische Werte in der angegebenen Argumentliste oder in einer Zelle in einem Bereich oder Element in einem Array handelt.</span><span class="sxs-lookup"><span data-stu-id="3d41d-117">if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="3d41d-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3d41d-118">Example</span></span>

<span data-ttu-id="3d41d-119">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="3d41d-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d41d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d41d-120">See also</span></span>



[<span data-ttu-id="3d41d-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="3d41d-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

