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
- tempnum12-Funktion [excel 2007], TempNum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790572"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="b6414-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="b6414-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="b6414-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6414-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b6414-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer Microsoft Excel-Arbeitsblatt-Zahl (einer IEEE-8-Byte-Double).</span><span class="sxs-lookup"><span data-stu-id="b6414-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="b6414-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6414-107">Parameters</span></span>

 <span data-ttu-id="b6414-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="b6414-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="b6414-109">Der vorgesehene Wert.</span><span class="sxs-lookup"><span data-stu-id="b6414-109">The intended value.</span></span> <span data-ttu-id="b6414-110">Beachten Sie, dass IEEE Unterseite normale Zahlen derzeit nicht unterstützt werden und sind auf 0 (null) gerundet.</span><span class="sxs-lookup"><span data-stu-id="b6414-110">Note that IEEE sub-normal numbers are not currently supported and are rounded to zero.</span></span> <span data-ttu-id="b6414-111">Negativ unendlich wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6414-111">Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b6414-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b6414-112">Return value</span></span>

<span data-ttu-id="b6414-113">Gibt einen numerischen **XltypeNum** mit dem Wert übergeben, oder NULL, wenn der übergebene Wert Unterseite normalen wurde.</span><span class="sxs-lookup"><span data-stu-id="b6414-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b6414-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b6414-114">Example</span></span>

<span data-ttu-id="b6414-115">In diesem Beispiel wird die **TempNum12** -Funktion verwendet, um **XlfGetWorkspace**ein Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="b6414-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b6414-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6414-116">See also</span></span>



[<span data-ttu-id="b6414-117">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="b6414-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

