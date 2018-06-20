---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- Tempactiveref-Funktion [excel 2007], TempActiveRef12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790567"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="d6516-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="d6516-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="d6516-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6516-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d6516-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer externen Referenz zu rechteckigen zellenblocks auf dem aktiven Blatt.</span><span class="sxs-lookup"><span data-stu-id="d6516-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="d6516-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6516-107">Parameters</span></span>

 <span data-ttu-id="d6516-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="d6516-108">_rwFirst_</span></span>
  
<span data-ttu-id="d6516-109">Die Startzeile des Verweises.</span><span class="sxs-lookup"><span data-stu-id="d6516-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="d6516-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="d6516-110">_rwLast_</span></span>
  
<span data-ttu-id="d6516-111">Die letzte Zeile des Verweises.</span><span class="sxs-lookup"><span data-stu-id="d6516-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="d6516-112">Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6516-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="d6516-113">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6516-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="d6516-114">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="d6516-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="d6516-115">Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="d6516-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="d6516-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="d6516-116">_colFirst_</span></span>
  
<span data-ttu-id="d6516-117">Die Anfangs-Spaltennummer des Verweises.</span><span class="sxs-lookup"><span data-stu-id="d6516-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="d6516-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="d6516-118">_colLast_</span></span>
  
<span data-ttu-id="d6516-119">Die Spaltennummer der letzten, des Verweises.</span><span class="sxs-lookup"><span data-stu-id="d6516-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="d6516-120">Spalte Argumente sind nullbasiert, damit diese Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6516-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="d6516-121">Der Höchstwert ist in Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6516-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="d6516-122">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1.</span><span class="sxs-lookup"><span data-stu-id="d6516-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="d6516-123">Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="d6516-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d6516-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d6516-124">Return value</span></span>

<span data-ttu-id="d6516-125">Gibt einen **XltypeRef** externer Verweis auf rechteckigen zellenblocks übergeben.</span><span class="sxs-lookup"><span data-stu-id="d6516-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d6516-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6516-126">Example</span></span>

<span data-ttu-id="d6516-127">In diesem Beispiel wird die **TempActiveRef12** -Funktion verwendet, um Zellen A105:C110 auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d6516-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d6516-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6516-128">See also</span></span>



[<span data-ttu-id="d6516-129">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="d6516-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

