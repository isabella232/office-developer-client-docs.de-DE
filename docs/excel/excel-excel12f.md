---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Excel-Funktion [Excel 2007], Excel12f-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431673"
---
# <a name="excelexcel12f"></a><span data-ttu-id="32982-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="32982-104">Excel/Excel12f</span></span>

 <span data-ttu-id="32982-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="32982-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="32982-106">Framework-Bibliotheksfunktionen.</span><span class="sxs-lookup"><span data-stu-id="32982-106">Framework library functions.</span></span> <span data-ttu-id="32982-107">**Excel** ist ein Wrapper für die [Excel4](excel4-excel12.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="32982-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="32982-108">**Excel12f** ist ein Wrapper für die [Excel12](excel4-excel12.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="32982-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="32982-109">Jeder überprüft, ob keines der Argumente NULL ist, was darauf hinweist, dass die Erstellung eines temporären **XLOPER** oder **XLOPER12** fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="32982-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="32982-110">Wenn ein Fehler auftritt, wird jeweils eine Debug-Meldung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="32982-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="32982-111">Wenn der Vorgang abgeschlossen ist, werden alle temporären Speicher freigegeben, die für temporäre **XLOPER**s und **XLOPER12**s erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="32982-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="32982-112">**Excel12f** kann nur von einer DLL aufgerufen werden, die mit der Excel 2007 C-API-Bibliothek beginnt.</span><span class="sxs-lookup"><span data-stu-id="32982-112">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library.</span></span> <span data-ttu-id="32982-113">Außerdem funktioniert es nur, wenn es ab Excel 2007 ausgeführt wird, und schlägt mit **xlretFailed** andernfalls fehl.</span><span class="sxs-lookup"><span data-stu-id="32982-113">Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="32982-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="32982-114">Parameters</span></span>

 <span data-ttu-id="32982-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="32982-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="32982-116">Eine Zahl, die den anzurufenden Befehl oder die Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="32982-116">A number indicating the command or function you want to call.</span></span> <span data-ttu-id="32982-117">Weitere Informationen finden Sie unter [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="32982-117">For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="32982-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="32982-118">_pxRes_</span></span>
  
<span data-ttu-id="32982-119">Ein Zeiger auf das Ergebnis der ausgewertet-Funktion.</span><span class="sxs-lookup"><span data-stu-id="32982-119">A pointer to result of the evaluated function.</span></span> <span data-ttu-id="32982-120">Jeder Arbeitsspeicher, auf den im Ergebnis verwiesen wird, wird von Excel zugewiesen und sollte bei einem Aufruf von [xlFree](xlfree.md) freigegeben werden, wenn er nicht mehr benötigt wird, oder indem **xlbitXLFree** festgelegt wird, wenn es an Excel zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="32982-120">Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="32982-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="32982-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="32982-122">Die Anzahl der Argumente, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="32982-122">The number of arguments that will be passed to the function.</span></span> <span data-ttu-id="32982-123">Ab Excel 2007 ist der Grenzwert 255 Argumente.</span><span class="sxs-lookup"><span data-stu-id="32982-123">Starting in Excel 2007, the limit is 255 arguments.</span></span> <span data-ttu-id="32982-124">In früheren Versionen beträgt die Grenze 30.</span><span class="sxs-lookup"><span data-stu-id="32982-124">In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="32982-125">_Argument1,..._</span><span class="sxs-lookup"><span data-stu-id="32982-125">_argument1, ..._</span></span>
  
<span data-ttu-id="32982-126">Die optionalen Argumente für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="32982-126">The optional arguments to the function.</span></span> <span data-ttu-id="32982-127">Alle Argumente müssen Zeiger auf **XLOPER**s im Fall von **Excel**oder **XLOPER12**s im Fall von **Excel12f**sein.</span><span class="sxs-lookup"><span data-stu-id="32982-127">All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="32982-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32982-128">Return value</span></span>

<span data-ttu-id="32982-129">Beide Funktionen geben dieselben Fehler-und Erfolgscodes zurück wie **Excel4**, **Excel4v**, **Excel12**und **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="32982-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="32982-130">Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12](excel4-excel12.md) .</span><span class="sxs-lookup"><span data-stu-id="32982-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="32982-131">Darüber hinaus geben diese Frameworkfunktionen **xlretFailed** ohne Aufrufen der C-API zurück, wenn ein NULL-Zeiger auf einen Parameter erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="32982-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="32982-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="32982-132">Example</span></span>

<span data-ttu-id="32982-133">In diesem Beispiel wird ein ungültiges Argument an die **Excel12f** -Funktion übergeben, die eine Nachricht an den Debugger sendet.</span><span class="sxs-lookup"><span data-stu-id="32982-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="32982-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32982-134">See also</span></span>



[<span data-ttu-id="32982-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="32982-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="32982-136">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="32982-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

