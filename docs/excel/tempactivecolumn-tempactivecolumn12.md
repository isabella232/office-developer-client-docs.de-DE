---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12-Funktion [excel 2007], TempActiveColumn-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790570"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="207c2-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="207c2-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="207c2-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="207c2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="207c2-106">Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine ganze Spalte im aktiven Blatt enthält.</span><span class="sxs-lookup"><span data-stu-id="207c2-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="207c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="207c2-107">Parameters</span></span>

 <span data-ttu-id="207c2-108">_Spalte_ (**BYTE**)</span><span class="sxs-lookup"><span data-stu-id="207c2-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="207c2-109">Die Spalte verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="207c2-109">The column to be referenced.</span></span> <span data-ttu-id="207c2-110">Dies ist nullbasiert, sodass diese Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="207c2-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="207c2-111">Der Höchstwert ist in Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="207c2-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="207c2-112">Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1.</span><span class="sxs-lookup"><span data-stu-id="207c2-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="207c2-113">Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.</span><span class="sxs-lookup"><span data-stu-id="207c2-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="207c2-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="207c2-114">Return value</span></span>

<span data-ttu-id="207c2-115">Gibt einen **XltypeRef** externer Verweis auf die Spalte übergebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="207c2-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="207c2-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="207c2-116">Example</span></span>

<span data-ttu-id="207c2-117">Das folgende Beispiel verwendet die **TempActiveColumn12** , wählen Sie die gesamte Spalte B.</span><span class="sxs-lookup"><span data-stu-id="207c2-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="207c2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="207c2-118">See also</span></span>



[<span data-ttu-id="207c2-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="207c2-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

