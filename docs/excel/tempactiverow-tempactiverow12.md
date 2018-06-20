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
- Tempactiverow-Funktion [excel 2007], TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790565"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="50e2b-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="50e2b-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="50e2b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50e2b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="50e2b-106">Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine gesamte Zeile im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="50e2b-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="50e2b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e2b-107">Parameters</span></span>

 <span data-ttu-id="50e2b-108">_Zeile_</span><span class="sxs-lookup"><span data-stu-id="50e2b-108">_row_</span></span>
  
<span data-ttu-id="50e2b-109">Die Zeile verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="50e2b-109">The row to be referenced.</span></span> <span data-ttu-id="50e2b-110">Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="50e2b-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="50e2b-111">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="50e2b-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="50e2b-112">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="50e2b-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="50e2b-113">Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="50e2b-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="50e2b-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="50e2b-114">Return value</span></span>

<span data-ttu-id="50e2b-115">Gibt einen **XltypeRef** externer Verweis zu übergeben, die Zellen in der Zeile zurück.</span><span class="sxs-lookup"><span data-stu-id="50e2b-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="50e2b-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="50e2b-116">Example</span></span>

<span data-ttu-id="50e2b-117">In diesem Beispiel wird die **TempActiveRow12** -Funktion verwendet, um 113 Zeile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="50e2b-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="50e2b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50e2b-118">See also</span></span>



[<span data-ttu-id="50e2b-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="50e2b-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

