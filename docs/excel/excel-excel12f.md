---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Excel-Funktion [excel 2007], Excel12f-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790432"
---
# <a name="excelexcel12f"></a><span data-ttu-id="b679f-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="b679f-104">Excel/Excel12f</span></span>

 <span data-ttu-id="b679f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b679f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b679f-106">Funktionen von Framework-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b679f-106">Framework library functions.</span></span> <span data-ttu-id="b679f-107">**Excel** ist ein Wrapper für die [Excel4](excel4-excel12.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b679f-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="b679f-108">**Excel12f** ist ein Wrapper für die [Excel12](excel4-excel12.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b679f-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="b679f-109">Jede überprüft, um anzuzeigen, dass keines der Argumente 0 (null) ist, bedeuten würde, dass die Erstellung einer temporären **XLOPER** oder **XLOPER12** ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="b679f-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="b679f-110">Wenn ein Fehler auftritt, wird jeweils eine Debug-Meldung gedruckt.</span><span class="sxs-lookup"><span data-stu-id="b679f-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="b679f-111">Abschließend frei jeweils alle temporären Speicher, der für die temporäre **XLOPER**s und **XLOPER12**s erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b679f-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="b679f-112">**Excel12f** kann nur aus einer DLL, beginnend mit der C-API für Excel 2007-Bibliothek aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b679f-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="b679f-113">Darüber hinaus nur bei der Ausführung, beginnend mit Excel 2007 und Funktionsweise andernfalls schlägt mit **xlretFailed zurück** .</span><span class="sxs-lookup"><span data-stu-id="b679f-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="b679f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b679f-114">Parameters</span></span>

 <span data-ttu-id="b679f-115">_iFunction_ (**Int**)</span><span class="sxs-lookup"><span data-stu-id="b679f-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="b679f-116">Eine Zahl, die den Befehl oder die Funktion angibt, die Sie anrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="b679f-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="b679f-117">Weitere Informationen finden Sie unter [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="b679f-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="b679f-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="b679f-118">_pxRes_</span></span>
  
<span data-ttu-id="b679f-119">Ein Zeiger auf Ergebnis der Funktion ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="b679f-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="b679f-120">Alle Speicher im das Ergebnis gezeigt wird von Excel zugeordnet worden sein und sollte im Gespräch zu [XlFree](xlfree.md) , sobald diese nicht mehr erforderlich ist, oder durch **XlbitXLFree** festlegen, wenn nach Excel zurückgegeben freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b679f-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="b679f-121">_iCount_ (**Int**)</span><span class="sxs-lookup"><span data-stu-id="b679f-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="b679f-122">Die Anzahl von Argumenten, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b679f-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="b679f-123">Ab Excel 2007 ist die Grenze 255 Argumente.</span><span class="sxs-lookup"><span data-stu-id="b679f-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="b679f-124">In früheren Versionen ist die Grenze 30.</span><span class="sxs-lookup"><span data-stu-id="b679f-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="b679f-125">_argument1..._</span><span class="sxs-lookup"><span data-stu-id="b679f-125">_argument1, ..._</span></span>
  
<span data-ttu-id="b679f-126">Die optionalen Argumente an die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b679f-126">The optional arguments to the function.</span></span> <span data-ttu-id="b679f-127">Alle Argumente müssen Zeiger auf **XLOPER**s im Fall von **Excel**oder **XLOPER12**s im Fall von **Excel12f**sein.</span><span class="sxs-lookup"><span data-stu-id="b679f-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b679f-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b679f-128">Return value</span></span>

<span data-ttu-id="b679f-129">Beide Funktionen zurückgegeben derselbe Fehler und Erfolgscodes als **Excel4**, **Excel4v**, **Excel12**und **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="b679f-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="b679f-130">Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="b679f-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="b679f-131">Darüber hinaus Rückgabewerte diese Funktionen Framework **xlretFailed zurück** , ohne einen Aufruf der C-API, wenn ein NULL-Zeiger auf einen Parameter erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="b679f-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b679f-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b679f-132">Example</span></span>

<span data-ttu-id="b679f-133">In diesem Beispiel werden ein ungültiges Argument an die Funktion **Excel12f** , sendet eine Meldung an den Debugger übergibt.</span><span class="sxs-lookup"><span data-stu-id="b679f-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b679f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b679f-134">See also</span></span>



[<span data-ttu-id="b679f-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="b679f-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="b679f-136">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="b679f-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

