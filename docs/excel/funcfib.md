---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- Funcfib-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790501"
---
# <a name="funcfib"></a><span data-ttu-id="8a744-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="8a744-104">FuncFib</span></span>

 <span data-ttu-id="8a744-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8a744-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8a744-106">Beispiel Arbeitsblatt benutzerdefinierte Funktion, die die n-te Fibonacci-Zahl berechnet.</span><span class="sxs-lookup"><span data-stu-id="8a744-106">Example user-defined worksheet function that computes the Nth Fibonacci number.</span></span> <span data-ttu-id="8a744-107">Wenn GENERIC.xll geladen wird, registriert sie diese Funktion, damit sie aus dem Arbeitsblatt aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a744-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="8a744-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a744-108">Parameters</span></span>

 <span data-ttu-id="8a744-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="8a744-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="8a744-110">Der Wert von N für die die n-te Fibonacci-Zahl erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8a744-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8a744-111">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a744-111">Property value/Return value</span></span>

<span data-ttu-id="8a744-112">(**XltypeNum LPXLOPER12** bei erfolgreicher oder **XltypeErr** andernfalls)</span><span class="sxs-lookup"><span data-stu-id="8a744-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="8a744-113">Die n-te Fibonacci-Zahl.</span><span class="sxs-lookup"><span data-stu-id="8a744-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a744-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a744-114">Remarks</span></span>

<span data-ttu-id="8a744-115">Die Funktion verwendet eine statische Variable in der Funktionsblock als Rückgabewert **XLOPER12**definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8a744-115">The function uses a static variable defined within the function block as the return value **XLOPER12**.</span></span> <span data-ttu-id="8a744-116">Dies ist nicht threadsicheren und also diese Funktion und alle Arbeitsblattfunktion, die diese Strategie verwendet für die Rückgabe **XLOPER**s oder **XLOPER12**s, sollten nicht registriert werden als threadsicheren ab Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="8a744-116">This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="8a744-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8a744-117">Example</span></span>

<span data-ttu-id="8a744-118">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="8a744-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a744-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a744-119">See also</span></span>



[<span data-ttu-id="8a744-120">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="8a744-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

