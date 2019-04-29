---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12-Funktion [Excel 2007], TempNum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426632"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="1fb64-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="1fb64-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="1fb64-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1fb64-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1fb64-106">Framework-Bibliotheksfunktion, mit der ein temporäres **XLOPER**/ -**XLOPER12** mit einer Microsoft Excel-Arbeitsblatt Nummer (ein IEEE 8-Byte-Double) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1fb64-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="1fb64-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fb64-107">Parameters</span></span>

 <span data-ttu-id="1fb64-108">_d_ (**Double**)</span><span class="sxs-lookup"><span data-stu-id="1fb64-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="1fb64-109">Der vorgesehene Wert.</span><span class="sxs-lookup"><span data-stu-id="1fb64-109">The intended value.</span></span> <span data-ttu-id="1fb64-110">Beachten Sie, dass IEEE-Sub-normal zahlen derzeit nicht unterstützt werden und auf NULL gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="1fb64-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="1fb64-111">Negative Unendlichkeit wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fb64-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1fb64-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fb64-112">Return value</span></span>

<span data-ttu-id="1fb64-113">Gibt eine numerische **XltypeNum** zurück, die den übergebenen Wert enthält, oder NULL, wenn der übergebene Wert unter normal ist.</span><span class="sxs-lookup"><span data-stu-id="1fb64-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1fb64-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1fb64-114">Example</span></span>

<span data-ttu-id="1fb64-115">In diesem Beispiel wird die **TempNum12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace**zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="1fb64-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="1fb64-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fb64-116">See also</span></span>



[<span data-ttu-id="1fb64-117">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="1fb64-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

