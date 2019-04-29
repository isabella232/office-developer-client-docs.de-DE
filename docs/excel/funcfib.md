---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423671"
---
# <a name="funcfib"></a><span data-ttu-id="10619-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="10619-104">FuncFib</span></span>

 <span data-ttu-id="10619-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="10619-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="10619-106">Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die die n-te Fibonacci-Zahl berechnet.</span><span class="sxs-lookup"><span data-stu-id="10619-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="10619-107">Wenn generische. XLL geladen wird, wird diese Funktion registriert, sodass Sie vom Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="10619-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="10619-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10619-108">Parameters</span></span>

 <span data-ttu-id="10619-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="10619-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="10619-110">Der Wert von N, für den die te Fibonacci-Zahl erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="10619-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="10619-111">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10619-111">Property value/Return value</span></span>

<span data-ttu-id="10619-112">(**XLTYPENUM LPXLOPER12** wenn erfolgreich oder **xltypeErr** andernfalls)</span><span class="sxs-lookup"><span data-stu-id="10619-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="10619-113">Die n-te Fibonacci-Zahl.</span><span class="sxs-lookup"><span data-stu-id="10619-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10619-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10619-114">Remarks</span></span>

<span data-ttu-id="10619-115">Die Funktion verwendet eine statische Variable, die innerhalb des Funktionsblocks als Rückgabewert **XLOPER12**definiert ist.</span><span class="sxs-lookup"><span data-stu-id="10619-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="10619-116">Dies ist nicht threadsicher, und diese Funktion und jede Arbeitsblattfunktion, die diese Strategie zum Zurückgeben von **XLOPER**s oder **XLOPER12**s verwendet, sollten ab Excel 2007 nicht als threadsicher registriert werden.</span><span class="sxs-lookup"><span data-stu-id="10619-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="10619-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="10619-117">Example</span></span>

<span data-ttu-id="10619-118">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="10619-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10619-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10619-119">See also</span></span>



[<span data-ttu-id="10619-120">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="10619-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

