---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperer-Funktion [Excel 2007], TempErr12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410609"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="4653a-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="4653a-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="4653a-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4653a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4653a-106">Framework-Bibliotheksfunktion, mit der ein temporäres **XLOPER**/ -**XLOPER12** mit einem Microsoft Excel-Arbeitsblattfehler erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4653a-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="4653a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4653a-107">Parameters</span></span>

 <span data-ttu-id="4653a-108">_err_</span><span class="sxs-lookup"><span data-stu-id="4653a-108">_err_</span></span>
  
<span data-ttu-id="4653a-109">Den gewünschten Fehlercode oder dessen numerisches Äquivalent, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4653a-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="4653a-110">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="4653a-110">**Error**</span></span>|<span data-ttu-id="4653a-111">**In XLCALL definierter Fehlercode. H**</span><span class="sxs-lookup"><span data-stu-id="4653a-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="4653a-112">**Decimal-Äquivalent**</span><span class="sxs-lookup"><span data-stu-id="4653a-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4653a-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="4653a-113">#NULL</span></span>  <br/> |<span data-ttu-id="4653a-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="4653a-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="4653a-115">0</span><span class="sxs-lookup"><span data-stu-id="4653a-115">0</span></span>  <br/> |
|<span data-ttu-id="4653a-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="4653a-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="4653a-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="4653a-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="4653a-118">7</span><span class="sxs-lookup"><span data-stu-id="4653a-118">7</span></span>  <br/> |
|<span data-ttu-id="4653a-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="4653a-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="4653a-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="4653a-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="4653a-121">15 </span><span class="sxs-lookup"><span data-stu-id="4653a-121">15</span></span>  <br/> |
|<span data-ttu-id="4653a-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="4653a-122">#REF!</span></span>  <br/> |<span data-ttu-id="4653a-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="4653a-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="4653a-124">23</span><span class="sxs-lookup"><span data-stu-id="4653a-124">23</span></span>  <br/> |
|<span data-ttu-id="4653a-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="4653a-125">#NAME?</span></span>  <br/> |<span data-ttu-id="4653a-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="4653a-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="4653a-127">29</span><span class="sxs-lookup"><span data-stu-id="4653a-127">29</span></span>  <br/> |
|<span data-ttu-id="4653a-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="4653a-128">#NUM!</span></span>  <br/> |<span data-ttu-id="4653a-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="4653a-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="4653a-130">36</span><span class="sxs-lookup"><span data-stu-id="4653a-130">36</span></span>  <br/> |
|<span data-ttu-id="4653a-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="4653a-131">#N/A</span></span>  <br/> |<span data-ttu-id="4653a-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="4653a-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="4653a-133">42</span><span class="sxs-lookup"><span data-stu-id="4653a-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="4653a-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4653a-134">Return value</span></span>

<span data-ttu-id="4653a-135">Gibt einen **xltypeBool** -Wert zurück, der den übergebenen Fehlercode enthält.</span><span class="sxs-lookup"><span data-stu-id="4653a-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4653a-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4653a-136">Example</span></span>

<span data-ttu-id="4653a-137">In diesem Beispiel wird die **TempErr12** -Funktion verwendet, um eine #VALUE zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4653a-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="4653a-138">Fehler bei Excel.</span><span class="sxs-lookup"><span data-stu-id="4653a-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4653a-139">Die Framework-Bibliotheksfunktion **TempErr12** reserviert Arbeitsspeicher aus einem internen Puffer, der normalerweise freigegeben wird, wenn die Frameworkfunktion **Excel12f** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4653a-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="4653a-140">Wenn diese Beispielfunktion wiederholt aufgerufen wird, ohne dass **Excel12f** aufgerufen wird, tritt ein Speicherverlust auf.</span><span class="sxs-lookup"><span data-stu-id="4653a-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="4653a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4653a-141">See also</span></span>



[<span data-ttu-id="4653a-142">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="4653a-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

