---
title: Funktionen in der Framework-Bibliothek
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Framework-Bibliotheksfunktionen [Excel 2007], Funktionen [Excel 2007], Framework-Bibliothek
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304053"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="27c6a-104">Funktionen in der Framework-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27c6a-104">Functions in the Framework Library</span></span>

<span data-ttu-id="27c6a-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="27c6a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="27c6a-106">Die Framework-Bibliothek wurde erstellt, um das Schreiben von XLLs zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="27c6a-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="27c6a-107">Sie enthält einfache Funktionen zum Verwalten des **XLOPER**/ -**XLOPER12** -Speichers, zum Erstellen temporärer **XLOPER**/ -**XLOPER12**und zum robusten Aufrufen der Microsoft Excel-Rückruffunktionen (**Excel4**, **Excel4v** , \* \* Excel12 \* \*, \* \* Excel12v \* \*) und Drucken von Debug-Zeichenfolgen auf einem angefügten Terminal.</span><span class="sxs-lookup"><span data-stu-id="27c6a-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="27c6a-108">Die in dieser Bibliothek enthaltenen Funktionen vereinfachen einen Code, der wie folgt aussieht.</span><span class="sxs-lookup"><span data-stu-id="27c6a-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="27c6a-109">Der vereinfachte Code sieht wie im folgenden Beispiel aus.</span><span class="sxs-lookup"><span data-stu-id="27c6a-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="27c6a-110">Die folgenden Funktionen sind in der Framework-Bibliothek enthalten:</span><span class="sxs-lookup"><span data-stu-id="27c6a-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="27c6a-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="27c6a-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="27c6a-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="27c6a-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="27c6a-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="27c6a-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="27c6a-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="27c6a-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="27c6a-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="27c6a-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="27c6a-116">**Mit XLOPERs verwendete Funktionen**</span><span class="sxs-lookup"><span data-stu-id="27c6a-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="27c6a-117">**Mit XLOPER12s verwendete Funktionen**</span><span class="sxs-lookup"><span data-stu-id="27c6a-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27c6a-118">Excel</span><span class="sxs-lookup"><span data-stu-id="27c6a-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="27c6a-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="27c6a-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="27c6a-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="27c6a-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="27c6a-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="27c6a-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="27c6a-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="27c6a-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="27c6a-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="27c6a-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="27c6a-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="27c6a-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="27c6a-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="27c6a-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="27c6a-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="27c6a-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="27c6a-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="27c6a-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="27c6a-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="27c6a-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="27c6a-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="27c6a-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="27c6a-130">TempErierung</span><span class="sxs-lookup"><span data-stu-id="27c6a-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="27c6a-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="27c6a-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="27c6a-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="27c6a-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="27c6a-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="27c6a-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="27c6a-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="27c6a-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="27c6a-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="27c6a-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="27c6a-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="27c6a-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="27c6a-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="27c6a-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="27c6a-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="27c6a-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="27c6a-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="27c6a-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="27c6a-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="27c6a-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="27c6a-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="27c6a-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="27c6a-142">Die Verwendung dieser Funktionen verkürzt die Zeitdauer, die zum Schreiben einer DLL oder XLL benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="27c6a-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="27c6a-143">Das Starten der Entwicklung aus der Beispielanwendung GENERIC verkürzt auch die Entwicklungszeit.</span><span class="sxs-lookup"><span data-stu-id="27c6a-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="27c6a-144">Verwenden Sie GENERIC. C als Vorlage zum Einrichten des Frameworks einer XLL und ersetzen Sie dann den vorhandenen Code durch eigene.</span><span class="sxs-lookup"><span data-stu-id="27c6a-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="27c6a-145">Die temporären **XLOPER**/ **-XLOPER12** -Funktionen erstellen **XLOPER**/ -**XLOPER12** Werte, indem Sie Arbeitsspeicher aus einem lokalen Heap verwenden, der von der Framework-Bibliothek verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="27c6a-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="27c6a-146">Die **XLOPER**/ **XLOPER12** -Werte bleiben gültig, bis Sie die **FreeAllTempMemory** -Funktion oder eine der **Excel** -oder **Excel12f** -Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27c6a-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="27c6a-147">(Der **Excel** -und der **Excel12f** -Funktion werden alle temporären Arbeitsspeicher freigegeben, bevor Sie zurückkehren.)</span><span class="sxs-lookup"><span data-stu-id="27c6a-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="27c6a-148">Um die Framework-Bibliotheksfunktionen verwenden zu können, müssen Sie die GERIPPE. H-Datei in Ihrem C-Code, und fügen Sie die GERIPPE. C oder FRMWRK32. LIB-Dateien für Ihr Codeprojekt.</span><span class="sxs-lookup"><span data-stu-id="27c6a-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27c6a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c6a-149">See also</span></span>

- [<span data-ttu-id="27c6a-150">Excel XLL SDK – API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="27c6a-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

