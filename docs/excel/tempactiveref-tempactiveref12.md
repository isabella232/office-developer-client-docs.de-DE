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
- tempactiveref-Funktion [excel 2007],TempActiveRef12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415544"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="e682f-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="e682f-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="e682f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e682f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e682f-106">Framework library function that creates a temporary **XLOPER** /  **XLOPER12** containing an external reference to rechteckige block of cells on the active sheet.</span><span class="sxs-lookup"><span data-stu-id="e682f-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="e682f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e682f-107">Parameters</span></span>

 <span data-ttu-id="e682f-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="e682f-108">_rwFirst_</span></span>
  
<span data-ttu-id="e682f-109">Die Anfangszeile des Verweises.</span><span class="sxs-lookup"><span data-stu-id="e682f-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="e682f-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="e682f-110">_rwLast_</span></span>
  
<span data-ttu-id="e682f-111">Die endende Zeile des Verweises.</span><span class="sxs-lookup"><span data-stu-id="e682f-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="e682f-112">Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e682f-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="e682f-113">In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e682f-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="e682f-114">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="e682f-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="e682f-115">RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="e682f-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="e682f-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="e682f-116">_colFirst_</span></span>
  
<span data-ttu-id="e682f-117">Die Nummer der Anfangsspalte des Verweises.</span><span class="sxs-lookup"><span data-stu-id="e682f-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="e682f-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="e682f-118">_colLast_</span></span>
  
<span data-ttu-id="e682f-119">Die Nummer der Endspalte des Verweises.</span><span class="sxs-lookup"><span data-stu-id="e682f-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="e682f-120">Spaltenargumente sind nullbasierte, sodass Spalte A als 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e682f-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="e682f-121">In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 – 1 und der Höchstwert, der von einer ganzzahligen BYTE verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e682f-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="e682f-122">Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="e682f-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="e682f-123">COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.</span><span class="sxs-lookup"><span data-stu-id="e682f-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e682f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e682f-124">Return value</span></span>

<span data-ttu-id="e682f-125">Gibt einen **externen xltypeRef-Verweis** auf einen rechteckigen Zellenblock zurück, der übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e682f-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e682f-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e682f-126">Example</span></span>

<span data-ttu-id="e682f-127">In diesem Beispiel wird die **TempActiveRef12-Funktion** zum Auswählen der Zellen A105:C110 verwendet.</span><span class="sxs-lookup"><span data-stu-id="e682f-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e682f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e682f-128">See also</span></span>



[<span data-ttu-id="e682f-129">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="e682f-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

