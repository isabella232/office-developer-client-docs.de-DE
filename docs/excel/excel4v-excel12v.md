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
- Excel12v-Funktion [Excel 2007], Excel4v-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414991"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="60fdf-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="60fdf-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="60fdf-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="60fdf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="60fdf-106">Ruft eine interne Microsoft Excel-Arbeitsblattfunktion, eine Makroblatt Funktion oder einen Befehl oder eine XLL-spezifische Funktion oder einen Befehl aus einer DLL-, XLL-oder Coderessource auf.</span><span class="sxs-lookup"><span data-stu-id="60fdf-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="60fdf-107">Alle neueren Versionen von Excel unterstützen **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="60fdf-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="60fdf-108">Ab Excel 2007 wird **Excel12v** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60fdf-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="60fdf-109">Diese Funktionen können nur aufgerufen werden, wenn Excel die Steuerung an die DLL oder XLL übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="60fdf-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="60fdf-110">Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic für Applikationen (VBA) übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="60fdf-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="60fdf-111">Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="60fdf-111">They cannot be called at any other time.</span></span> <span data-ttu-id="60fdf-112">Beispielsweise können Sie nicht während der Aufrufe an die DllMain-Funktion oder zu anderen Zeiten aufgerufen werden, wenn das Betriebssystem die DLL aufgerufen hat, oder aus einem von der DLL erstellten Thread.</span><span class="sxs-lookup"><span data-stu-id="60fdf-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="60fdf-113">Die [Excel4-und Excel12](excel4-excel12.md) -Funktionen akzeptieren ihre Argumente als Variable Längen Liste im Stapel, wohingegen die **Excel4v** -und die **Excel12v** -Funktion Ihre Argumente als Array akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="60fdf-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="60fdf-114">In allen anderen Aspekten verhält sich **Excel4** wie **Excel4v**, und **Excel12** verhält sich genauso wie **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="60fdf-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="60fdf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="60fdf-115">Parameters</span></span>

 <span data-ttu-id="60fdf-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="60fdf-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="60fdf-117">Eine Zahl, die den Befehl, die Funktion oder die spezielle Funktion angibt, die Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="60fdf-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="60fdf-118">Eine Liste gültiger _iFunction_ -Werte finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="60fdf-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="60fdf-119">_pxRes_ (**LPXLOPER** oder **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="60fdf-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="60fdf-120">Ein Zeiger auf ein **XLOPER** (im Fall von **Excel4v**) oder ein **XLOPER12** (im Fall von **Excel12v**), das das Ergebnis der ausgewerteten Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="60fdf-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="60fdf-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="60fdf-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="60fdf-122">Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="60fdf-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="60fdf-123">In Excel-Versionen bis zu 2003 kann es sich um eine beliebige Zahl zwischen 0 und 30 handeln.</span><span class="sxs-lookup"><span data-stu-id="60fdf-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="60fdf-124">Ab Excel 2007 kann es sich um eine beliebige Zahl zwischen 0 und 255 handeln.</span><span class="sxs-lookup"><span data-stu-id="60fdf-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="60fdf-125">_RGX_ (**LPXLOPER []** oder **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="60fdf-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="60fdf-126">Ein Array, das die Argumente für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="60fdf-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="60fdf-127">Alle Argumente im Array müssen Zeiger auf **XLOPER** -oder **XLOPER12** -Werte sein.</span><span class="sxs-lookup"><span data-stu-id="60fdf-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="60fdf-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60fdf-128">Return value</span></span>

<span data-ttu-id="60fdf-129">Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12**zurück.</span><span class="sxs-lookup"><span data-stu-id="60fdf-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60fdf-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60fdf-130">Remarks</span></span>

<span data-ttu-id="60fdf-131">Diese Funktionen sind nützlich, wenn die Anzahl der an den Operator übergebenen Argumente variabel ist.</span><span class="sxs-lookup"><span data-stu-id="60fdf-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="60fdf-132">Beispielsweise sind **Excel4v** und **Excel12v** hilfreich, wenn Sie Funktionen mithilfe von [xlfRegister](xlfregister-form-1.md) registrieren, wobei die Anzahl der Gesamt Argumente von der Anzahl von Argumenten abhängt, die von der registrierten Funktion übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="60fdf-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="60fdf-133">**Excel4v** und **Excel12v** sind auch nützlich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12**schreiben.</span><span class="sxs-lookup"><span data-stu-id="60fdf-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="60fdf-134">In diesen Fällen müssen Sie eine Variable Argumentliste, wie normalerweise an **Excel4** oder **Excel12**, in ein einzelnes Array Argument mit variabler Größe konvertieren, um mithilfe von **Excel4v** oder **Excel12v**zurück in Excel aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="60fdf-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="60fdf-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60fdf-135">Example</span></span>

<span data-ttu-id="60fdf-136">Codebeispiele finden Sie im Code für die **Excel** -und **Excel12f** -Funktionen im Excel 2010 XLL-SDK an der Stelle, an der Sie das SDK installiert haben:</span><span class="sxs-lookup"><span data-stu-id="60fdf-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="60fdf-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="60fdf-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60fdf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60fdf-138">See also</span></span>



[<span data-ttu-id="60fdf-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="60fdf-139">Excel4/Excel12</span></span>](excel4-excel12.md)

