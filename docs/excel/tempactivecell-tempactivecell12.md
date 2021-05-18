---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- tempactivecell12-Funktion [excel 2007],TempActiveCell-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413192"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="18eff-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="18eff-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="18eff-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="18eff-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="18eff-106">Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine Zelle im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="18eff-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="18eff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="18eff-107">Parameters</span></span>

 <span data-ttu-id="18eff-108">_row_</span><span class="sxs-lookup"><span data-stu-id="18eff-108">_row_</span></span>
  
<span data-ttu-id="18eff-109">Die Zeile, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18eff-109">The row to be referenced.</span></span> <span data-ttu-id="18eff-110">Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="18eff-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="18eff-111">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18eff-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="18eff-112">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="18eff-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="18eff-113">RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="18eff-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="18eff-114">_col_</span><span class="sxs-lookup"><span data-stu-id="18eff-114">_col_</span></span>
  
<span data-ttu-id="18eff-115">Die Spalte, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18eff-115">The column to be referenced.</span></span> <span data-ttu-id="18eff-116">Dies ist nullbasierte, sodass Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="18eff-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="18eff-117">In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 – 1 und der Höchstwert, der von einer ganzzahligen BYTE verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18eff-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="18eff-118">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="18eff-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="18eff-119">COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.</span><span class="sxs-lookup"><span data-stu-id="18eff-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="18eff-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18eff-120">Return value</span></span>

<span data-ttu-id="18eff-121">Gibt einen **externen xltypeRef-Verweis** auf die übergebene Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="18eff-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="18eff-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="18eff-122">Example</span></span>

<span data-ttu-id="18eff-123">Im folgenden Beispiel wird **TempActiveCell12 verwendet,** um den Inhalt von B94 auf dem aktiven Blatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18eff-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="18eff-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18eff-124">See also</span></span>



[<span data-ttu-id="18eff-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="18eff-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

