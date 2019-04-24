---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow-Funktion [Excel 2007], TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310416"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="52abd-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="52abd-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="52abd-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52abd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52abd-106">Framework-Bibliotheksfunktionen, mit denen ein temporäres **XLOPER**/ -**XLOPER12** erstellt wird, das einen externen Verweis auf eine ganze Zeile im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="52abd-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="52abd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52abd-107">Parameters</span></span>

 <span data-ttu-id="52abd-108">_Zeile_</span><span class="sxs-lookup"><span data-stu-id="52abd-108">_row_</span></span>
  
<span data-ttu-id="52abd-109">Die Zeile, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="52abd-109">The row to be referenced.</span></span> <span data-ttu-id="52abd-110">Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="52abd-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="52abd-111">In Microsoft Office Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 65.535 = 2 ^ 16-1 und ist der Höchstwert, der von einem Wort Integer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="52abd-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="52abd-112">Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="52abd-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="52abd-113">RW ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="52abd-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="52abd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52abd-114">Return value</span></span>

<span data-ttu-id="52abd-115">Gibt einen externen **externen xltypeRef** -Verweis auf Zeilen Zellen zurück, die übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="52abd-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="52abd-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52abd-116">Example</span></span>

<span data-ttu-id="52abd-117">In diesem Beispiel wird die **TempActiveRow12** -Funktion verwendet, um Zeile 113 zu markieren.</span><span class="sxs-lookup"><span data-stu-id="52abd-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="52abd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52abd-118">See also</span></span>



[<span data-ttu-id="52abd-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="52abd-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

