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
- tempactivecell12-Funktion [excel 2007], TempActiveCell-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790564"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="d8347-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="d8347-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="d8347-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8347-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d8347-106">Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine Zelle im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="d8347-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="d8347-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8347-107">Parameters</span></span>

 <span data-ttu-id="d8347-108">_Zeile_</span><span class="sxs-lookup"><span data-stu-id="d8347-108">_row_</span></span>
  
<span data-ttu-id="d8347-109">Die Zeile verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d8347-109">The row to be referenced.</span></span> <span data-ttu-id="d8347-110">Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d8347-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="d8347-111">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8347-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="d8347-112">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="d8347-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="d8347-113">Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="d8347-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="d8347-114">_Spalte_</span><span class="sxs-lookup"><span data-stu-id="d8347-114">_col_</span></span>
  
<span data-ttu-id="d8347-115">Die Spalte verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d8347-115">The column to be referenced.</span></span> <span data-ttu-id="d8347-116">Dies ist nullbasiert, sodass diese Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d8347-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="d8347-117">Der Höchstwert ist in Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8347-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="d8347-118">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1.</span><span class="sxs-lookup"><span data-stu-id="d8347-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="d8347-119">Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="d8347-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d8347-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d8347-120">Return value</span></span>

<span data-ttu-id="d8347-121">Gibt einen **XltypeRef** externer Verweis auf die Zelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="d8347-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d8347-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d8347-122">Example</span></span>

<span data-ttu-id="d8347-123">Das folgende Beispiel verwendet die **TempActiveCell12** zum Anzeigen des Inhalts der B94 auf dem aktiven Blatt.</span><span class="sxs-lookup"><span data-stu-id="d8347-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d8347-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8347-124">See also</span></span>



[<span data-ttu-id="d8347-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="d8347-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

