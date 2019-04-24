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
- tempactivecell12-Funktion [Excel 2007], TempActiveCell-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301575"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="56b87-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="56b87-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="56b87-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56b87-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="56b87-106">Framework-Bibliotheksfunktionen, mit denen ein temporäres **XLOPER**/ -**XLOPER12** erstellt wird, das einen externen Verweis auf eine Zelle im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="56b87-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="56b87-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b87-107">Parameters</span></span>

 <span data-ttu-id="56b87-108">_Zeile_</span><span class="sxs-lookup"><span data-stu-id="56b87-108">_row_</span></span>
  
<span data-ttu-id="56b87-109">Die Zeile, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="56b87-109">The row to be referenced.</span></span> <span data-ttu-id="56b87-110">Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="56b87-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="56b87-111">In Microsoft Office Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 65.535 = 2 ^ 16-1 und ist der Höchstwert, der von einem Wort Integer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="56b87-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="56b87-112">Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="56b87-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="56b87-113">RW ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="56b87-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="56b87-114">_Spalte_</span><span class="sxs-lookup"><span data-stu-id="56b87-114">_col_</span></span>
  
<span data-ttu-id="56b87-115">Die Spalte, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="56b87-115">The column to be referenced.</span></span> <span data-ttu-id="56b87-116">Dies ist nullbasiert, sodass Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="56b87-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="56b87-117">In Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 255 = 2 ^ 8-1 und ist der Maximalwert, der von einer BYTE-Ganzzahl verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="56b87-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="56b87-118">Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="56b87-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="56b87-119">COL ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="56b87-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="56b87-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56b87-120">Return value</span></span>

<span data-ttu-id="56b87-121">Gibt einen externen **externen xltypeRef** -Verweis auf die übergebene Zelle zurück.</span><span class="sxs-lookup"><span data-stu-id="56b87-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="56b87-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="56b87-122">Example</span></span>

<span data-ttu-id="56b87-123">Im folgenden Beispiel wird **TempActiveCell12** verwendet, um den Inhalt von B94 im aktiven Blatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56b87-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="56b87-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56b87-124">See also</span></span>



[<span data-ttu-id="56b87-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="56b87-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

