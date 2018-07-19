---
title: Funktionen in der Framework-Klassenbibliothek
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen der Framework-Bibliothek [excel 2007], Funktionen [Excel 2007], Framework-Klassenbibliothek
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790516"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="ec5c6-104">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="ec5c6-104">Functions in the Framework Library</span></span>

<span data-ttu-id="ec5c6-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ec5c6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ec5c6-106">Der Framework-Klassenbibliothek erstellt wurde, um das Schreiben von XLLs leichter machen.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="ec5c6-107">Sie enthält einfache Funktionen für die Verwaltung von **XLOPER**/ **XLOPER12** Arbeitsspeicher, zum Erstellen der temporären **XLOPER**/ **XLOPER12**, die Microsoft Excel-Rückruffunktionen (**Excel4**, **Excel4v** robust aufrufen ** Excel12 **, ** Excel12v **) und Debuggen von Zeichenfolgen auf eine angefügte Terminal drucken.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="ec5c6-108">Die in dieser Bibliothek enthaltenen Funktionen vereinfachen Codeabschnitte, die wie folgt aussieht.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="ec5c6-109">Der vereinfachte Code sieht wie im folgenden Beispiel wird.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="ec5c6-110">Die folgenden Funktionen sind in der Framework-Bibliothek enthalten:</span><span class="sxs-lookup"><span data-stu-id="ec5c6-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="ec5c6-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="ec5c6-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="ec5c6-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="ec5c6-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="ec5c6-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="ec5c6-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="ec5c6-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="ec5c6-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="ec5c6-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="ec5c6-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="ec5c6-116">**Funktionen, die mit XLOPERs verwendet werden.**</span><span class="sxs-lookup"><span data-stu-id="ec5c6-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="ec5c6-117">**Funktionen, die mit XLOPER12s verwendet werden.**</span><span class="sxs-lookup"><span data-stu-id="ec5c6-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec5c6-118">Excel</span><span class="sxs-lookup"><span data-stu-id="ec5c6-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="ec5c6-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="ec5c6-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="ec5c6-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="ec5c6-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="ec5c6-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="ec5c6-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="ec5c6-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="ec5c6-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="ec5c6-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="ec5c6-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="ec5c6-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="ec5c6-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="ec5c6-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="ec5c6-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="ec5c6-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="ec5c6-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="ec5c6-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="ec5c6-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="ec5c6-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="ec5c6-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="ec5c6-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="ec5c6-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="ec5c6-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="ec5c6-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="ec5c6-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="ec5c6-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="ec5c6-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="ec5c6-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="ec5c6-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="ec5c6-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="ec5c6-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="ec5c6-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="ec5c6-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="ec5c6-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="ec5c6-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="ec5c6-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="ec5c6-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="ec5c6-142">Verwendung dieser Funktionen verkürzt die Zeitdauer, die erforderlich sind, einer DLL oder XLL zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-142">Use of these functions shortens the amount of time required to write a DLL or XLL.</span></span> <span data-ttu-id="ec5c6-143">Beginn der Entwicklung von der beispielanwendung verkürzt generische Entwicklungszeit.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-143">Starting development from the sample application GENERIC also shortens development time.</span></span> <span data-ttu-id="ec5c6-144">Verwenden Sie Allgemeines. C als Vorlage, die im Rahmen der eine XLL eingerichtet, und Ersetzen Sie den vorhandenen Code durch Ihren eigenen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-144">Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="ec5c6-145">Die temporäre **XLOPER**/ **XLOPER12** Funktionen erstellen **XLOPER**/ **XLOPER12** Werte mithilfe der Speicher von einem lokalen Heap Framework-Klassenbibliothek verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-145">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library.</span></span> <span data-ttu-id="ec5c6-146">Die **XLOPER**/ **XLOPER12** Werte bleiben gültig, bis Sie die **FreeAllTempMemory** -Funktion oder eine **Excel-** oder **Excel12f** -Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-146">The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions.</span></span> <span data-ttu-id="ec5c6-147">(Die Funktionen von **Excel** und **Excel12f** frei alle temporären Speicher vor der Rückgabe).</span><span class="sxs-lookup"><span data-stu-id="ec5c6-147">(The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="ec5c6-148">Um die Funktionen der Framework-Bibliothek verwenden, müssen Sie die FRAMEWRK einbeziehen. H-Datei in Ihrem C#-Code, und fügen Sie die FRAMEWRK. C oder FRMWRK32. LIB-Dateien auf Ihr Codeprojekt.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ec5c6-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec5c6-149">See also</span></span>

- [<span data-ttu-id="ec5c6-150">Excel XLL-SDK-API-Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="ec5c6-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

