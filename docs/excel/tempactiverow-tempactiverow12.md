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
- tempactiverow-Funktion [excel 2007],TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413108"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="5caf1-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="5caf1-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="5caf1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5caf1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5caf1-106">Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine gesamte Zeile im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="5caf1-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="5caf1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5caf1-107">Parameters</span></span>

 <span data-ttu-id="5caf1-108">_row_</span><span class="sxs-lookup"><span data-stu-id="5caf1-108">_row_</span></span>
  
<span data-ttu-id="5caf1-109">Die Zeile, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5caf1-109">The row to be referenced.</span></span> <span data-ttu-id="5caf1-110">Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5caf1-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="5caf1-111">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5caf1-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="5caf1-112">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="5caf1-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="5caf1-113">RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="5caf1-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="5caf1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5caf1-114">Return value</span></span>

<span data-ttu-id="5caf1-115">Gibt einen **externen xltypeRef-Verweis** auf die übergebenen Zeilenzellen zurück.</span><span class="sxs-lookup"><span data-stu-id="5caf1-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5caf1-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5caf1-116">Example</span></span>

<span data-ttu-id="5caf1-117">In diesem Beispiel wird die **TempActiveRow12-Funktion** verwendet, um Zeile 113 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5caf1-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="5caf1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5caf1-118">See also</span></span>



[<span data-ttu-id="5caf1-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="5caf1-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

