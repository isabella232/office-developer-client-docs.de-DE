---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- Excel12v-Funktion [excel 2007], Excel4v-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790505"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="e307d-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="e307d-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="e307d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e307d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e307d-106">Ruft auf einer internen Microsoft Excel-Arbeitsblatt-Funktion, Blatt Makrofunktion oder Befehls, oder XLL-only Sonderfunktion bzw., innerhalb einer DLL, XLL oder Code-Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="e307d-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="e307d-107">Alle aktuelle Versionen von Excel unterstützen **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="e307d-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="e307d-108">Ab Excel 2007 wird **Excel12v** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e307d-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="e307d-109">Nur, wenn Excel Steuerelement an die DLL oder XLL übergeben wurde, können diese Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e307d-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="e307d-110">Sie können auch aufgerufen werden, wenn Excel Steuerelement indirekt über einen Aufruf zu Visual Basic für Applikationen (VBA) übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e307d-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="e307d-111">Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e307d-111">They cannot be called at any other time.</span></span> <span data-ttu-id="e307d-112">Beispielsweise können nicht sie während der Anrufe von der DllMain-Funktion oder anderen Zeiten, wenn das Betriebssystem die DLL aufgerufen wurde, oder von der DLL erstellten Thread aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e307d-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="e307d-113">Die Funktionen [Excel4 und Excel12](excel4-excel12.md) annehmen deren Argumente als Liste variabler Länge auf dem Stapel, während die Funktionen **Excel4v** und **Excel12v** deren Argumente als Array annehmen.</span><span class="sxs-lookup"><span data-stu-id="e307d-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="e307d-114">In jeder anderen Hinsicht **Excel4** verhält sich wie **Excel4v**und **Excel12** verhält sich **Excel12v**identisch.</span><span class="sxs-lookup"><span data-stu-id="e307d-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="e307d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e307d-115">Parameters</span></span>

 <span data-ttu-id="e307d-116">_iFunction_ (**Int**)</span><span class="sxs-lookup"><span data-stu-id="e307d-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="e307d-117">Eine Zahl, die den Befehl, Function- oder Sonderfunktion gibt an, die Sie anrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="e307d-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="e307d-118">Eine Liste der gültigen _iFunction_ Werte finden Sie unter den folgenden Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="e307d-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="e307d-119">_pxRes_ (**LPXLOPER** oder **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="e307d-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="e307d-120">Ein Zeiger auf eine **XLOPER** (im Fall von **Excel4v**) oder ein **XLOPER12** (im Fall von **Excel12v**), die das Ergebnis der ausgewertete Funktion enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="e307d-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="e307d-121">_iCount_ (**Int**)</span><span class="sxs-lookup"><span data-stu-id="e307d-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="e307d-122">Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e307d-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="e307d-123">In Versionen von Excel bis zu 2003 kann dies eine beliebige Zahl von 0 bis 30 sein.</span><span class="sxs-lookup"><span data-stu-id="e307d-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="e307d-124">Ab Excel 2007, kann dies eine beliebige Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="e307d-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="e307d-125">_rgx_ (**LPXLOPER []** oder **[LPXLOPER12]**)</span><span class="sxs-lookup"><span data-stu-id="e307d-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="e307d-126">Ein Array, das die Argumente für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="e307d-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="e307d-127">Alle Argumente im Array müssen Zeiger auf **XLOPER** oder **XLOPER12** Werten sein.</span><span class="sxs-lookup"><span data-stu-id="e307d-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="e307d-128">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e307d-128">Return value</span></span>

<span data-ttu-id="e307d-129">Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="e307d-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e307d-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e307d-130">Remarks</span></span>

<span data-ttu-id="e307d-131">Diese Funktionen sind nützlich, in dem die Anzahl von Argumenten, die an den Operator übergeben Variable ist.</span><span class="sxs-lookup"><span data-stu-id="e307d-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="e307d-132">Beispielsweise sind **Excel4v** und **Excel12v** hilfreich beim Registrieren Funktionen mithilfe von [XlfRegister](xlfregister-form-1.md) , in dem die Anzahl der Argumente, die von der Funktion registrierende geschaltet hängt der Anzahl der insgesamt Argumente.</span><span class="sxs-lookup"><span data-stu-id="e307d-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="e307d-133">**Excel4v** und **Excel12v** sind ebenfalls hilfreich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12**schreiben.</span><span class="sxs-lookup"><span data-stu-id="e307d-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="e307d-134">In diesen Fällen müssen Sie eine Variable Argumentliste convert-normalerweise für einen einzelnen Array-Argument variabler Größe einen Rückruf in Excel mithilfe von **Excel4v** oder **Excel12v** **Excel4** oder **Excel12**bereitgestellt werden würde.</span><span class="sxs-lookup"><span data-stu-id="e307d-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="e307d-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e307d-135">Example</span></span>

<span data-ttu-id="e307d-136">Codebeispiele finden Sie in den Code für die **Excel** und **Excel12f** Funktionen in Excel 2010 XLL SDK am folgenden Speicherort, in dem Sie das SDK installiert:</span><span class="sxs-lookup"><span data-stu-id="e307d-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="e307d-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="e307d-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e307d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e307d-138">See also</span></span>



[<span data-ttu-id="e307d-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="e307d-139">Excel4/Excel12</span></span>](excel4-excel12.md)

