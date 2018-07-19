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
- Temperr-Funktion [excel 2007], TempErr12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790566"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="ce913-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="ce913-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="ce913-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ce913-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ce913-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer Microsoft Excel-Arbeitsblatt-Fehler.</span><span class="sxs-lookup"><span data-stu-id="ce913-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="ce913-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce913-107">Parameters</span></span>

 <span data-ttu-id="ce913-108">_Err_</span><span class="sxs-lookup"><span data-stu-id="ce913-108">_err_</span></span>
  
<span data-ttu-id="ce913-109">Die gewünschte Fehlercode oder deren Literale numerische Entsprechung, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce913-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="ce913-110">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="ce913-110">**Error**</span></span>|<span data-ttu-id="ce913-111">**Fehlercode in XLCALL definiert. H**</span><span class="sxs-lookup"><span data-stu-id="ce913-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="ce913-112">**Dezimalzahl**</span><span class="sxs-lookup"><span data-stu-id="ce913-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce913-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="ce913-113">#NULL</span></span>  <br/> |<span data-ttu-id="ce913-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="ce913-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="ce913-115">0</span><span class="sxs-lookup"><span data-stu-id="ce913-115">0</span></span>  <br/> |
|<span data-ttu-id="ce913-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="ce913-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="ce913-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="ce913-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="ce913-118">7</span><span class="sxs-lookup"><span data-stu-id="ce913-118">7</span></span>  <br/> |
|<span data-ttu-id="ce913-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="ce913-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="ce913-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="ce913-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="ce913-121">15</span><span class="sxs-lookup"><span data-stu-id="ce913-121">15</span></span>  <br/> |
|<span data-ttu-id="ce913-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="ce913-122">#REF!</span></span>  <br/> |<span data-ttu-id="ce913-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="ce913-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="ce913-124">23</span><span class="sxs-lookup"><span data-stu-id="ce913-124">23</span></span>  <br/> |
|<span data-ttu-id="ce913-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="ce913-125">#NAME?</span></span>  <br/> |<span data-ttu-id="ce913-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="ce913-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="ce913-127">29</span><span class="sxs-lookup"><span data-stu-id="ce913-127">29</span></span>  <br/> |
|<span data-ttu-id="ce913-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="ce913-128">#NUM!</span></span>  <br/> |<span data-ttu-id="ce913-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="ce913-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="ce913-130">36</span><span class="sxs-lookup"><span data-stu-id="ce913-130">36</span></span>  <br/> |
|<span data-ttu-id="ce913-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="ce913-131">#N/A</span></span>  <br/> |<span data-ttu-id="ce913-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="ce913-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="ce913-133">42</span><span class="sxs-lookup"><span data-stu-id="ce913-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ce913-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce913-134">Return value</span></span>

<span data-ttu-id="ce913-135">Gibt ein **XltypeBool** mit den Fehlercode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce913-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ce913-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ce913-136">Example</span></span>

<span data-ttu-id="ce913-137">In diesem Beispiel wird die **TempErr12** -Funktion verwendet, um eine #VALUE zurück!</span><span class="sxs-lookup"><span data-stu-id="ce913-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="ce913-138">Fehler in Excel.</span><span class="sxs-lookup"><span data-stu-id="ce913-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ce913-139">Die Bibliothek Framework-Funktion **TempErr12** reserviert Speicher aus einem internen Puffer, die normalerweise freigegeben wird, wenn die Framework-Funktion **Excel12f** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ce913-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="ce913-140">Wenn diese Beispielfunktion ohne **Excel12f** aufgerufen wird wiederholt aufgerufen wird, tritt ein, Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="ce913-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="ce913-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce913-141">See also</span></span>



[<span data-ttu-id="ce913-142">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="ce913-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

