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
- excel12v-Funktion [excel 2007],Excel4v-Funktion [Excel 2007]
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
# <a name="excel4vexcel12v"></a><span data-ttu-id="da04c-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="da04c-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="da04c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da04c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="da04c-106">Ruft eine interne Microsoft Excel- oder Makroblattfunktion oder -befehl oder XLL-only-Sonderfunktion oder -befehl innerhalb einer DLL-, XLL- oder Coderessource auf.</span><span class="sxs-lookup"><span data-stu-id="da04c-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="da04c-107">Alle aktuellen Versionen von Excel **unterstützen Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="da04c-107">All recent versions of Excel support **Excel4v**.</span></span> <span data-ttu-id="da04c-108">Ab Excel 2007 wird **Excel12v** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da04c-108">Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="da04c-109">Diese Funktionen können nur aufgerufen werden, Excel das Steuerelement an die DLL oder XLL übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="da04c-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="da04c-110">Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic for Applications (VBA) übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="da04c-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="da04c-111">Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="da04c-111">They cannot be called at any other time.</span></span> <span data-ttu-id="da04c-112">Sie können z. B. nicht bei Aufrufen der DllMain-Funktion oder in anderen Zeiten aufgerufen werden, in denen das Betriebssystem die DLL aufgerufen hat, oder aus einem thread, der von der DLL erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="da04c-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="da04c-113">Die [Funktionen Excel4 und Excel12](excel4-excel12.md) akzeptieren ihre Argumente als Liste mit variabler Länge auf dem Stapel, während die **Funktionen Excel4v** und **Excel12v** ihre Argumente als Array akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="da04c-113">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array.</span></span> <span data-ttu-id="da04c-114">In allen anderen Hinsicht verhält sich **Excel4** genauso wie **Excel4v,** und **Excel12** verhält sich genauso wie **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="da04c-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="da04c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="da04c-115">Parameters</span></span>

 <span data-ttu-id="da04c-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="da04c-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="da04c-117">Eine Zahl, die den Befehl, die Funktion oder die Sonderfunktion angibt, die Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="da04c-117">A number that indicates the command, function, or special function you want to call.</span></span> <span data-ttu-id="da04c-118">Eine Liste der  _gültigen iFunction-Werte_ finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="da04c-118">For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="da04c-119">_pxRes_ (**LPXLOPER** oder **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="da04c-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="da04c-120">Ein Zeiger auf einen **XLOPER** (im Fall von **Excel4v**) oder einen **XLOPER12** (im Fall von **Excel12v**), der das Ergebnis der ausgewerteten Funktion hält.</span><span class="sxs-lookup"><span data-stu-id="da04c-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="da04c-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="da04c-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="da04c-122">Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da04c-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="da04c-123">In Versionen von Excel bis 2003 kann dies eine beliebige Zahl zwischen 0 und 30 sein.</span><span class="sxs-lookup"><span data-stu-id="da04c-123">In versions of Excel up to 2003 this can be any number from 0 through 30.</span></span> <span data-ttu-id="da04c-124">Ab Excel 2007 kann dies eine beliebige Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="da04c-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="da04c-125">_rgx_ (**LPXLOPER []** oder **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="da04c-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="da04c-126">Ein Array, das die Argumente für die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="da04c-126">An array that contains the arguments to the function.</span></span> <span data-ttu-id="da04c-127">Alle Argumente im Array müssen Zeiger auf **XLOPER-** oder **XLOPER12-Werte** sein.</span><span class="sxs-lookup"><span data-stu-id="da04c-127">All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="da04c-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da04c-128">Return value</span></span>

<span data-ttu-id="da04c-129">Diese Funktionen geben dieselben Werte wie **Excel4** und **Excel12 zurück.**</span><span class="sxs-lookup"><span data-stu-id="da04c-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da04c-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da04c-130">Remarks</span></span>

<span data-ttu-id="da04c-131">Diese Funktionen sind nützlich, wenn die Anzahl der an den Operator übergebenen Argumente variabel ist.</span><span class="sxs-lookup"><span data-stu-id="da04c-131">These functions are useful where the number of arguments passed to the operator is variable.</span></span> <span data-ttu-id="da04c-132">Beispielsweise sind **Excel4v** und **Excel12v** hilfreich, wenn Sie Funktionen mithilfe von [xlfRegister](xlfregister-form-1.md) registrieren, wobei die Gesamtzahl der Argumente von der Anzahl der Argumente abhängt, die von der zu registrierende Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da04c-132">For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered.</span></span> <span data-ttu-id="da04c-133">**Excel4v** und **Excel12v** sind auch hilfreich, wenn Sie eine Wrapperfunktion für **Excel4** oder **Excel12 schreiben.**</span><span class="sxs-lookup"><span data-stu-id="da04c-133">**Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**.</span></span> <span data-ttu-id="da04c-134">In diesen Fällen müssen Sie eine Variablenargumentliste konvertieren, wie sie normalerweise für **Excel4** oder **Excel12** bereitgestellt wird, in ein einzelnes Arrayargument mit variabler Größe, um mithilfe von **Excel4v** oder **Excel12v** in Excel zurück zu rufen.</span><span class="sxs-lookup"><span data-stu-id="da04c-134">In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="da04c-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="da04c-135">Example</span></span>

<span data-ttu-id="da04c-136">Codebeispiele finden Sie im Code für die **Funktionen Excel** und **Excel12f** im Excel 2010 XLL SDK am folgenden Speicherort, an dem Sie das SDK installiert haben:</span><span class="sxs-lookup"><span data-stu-id="da04c-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="da04c-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="da04c-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da04c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da04c-138">See also</span></span>



[<span data-ttu-id="da04c-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="da04c-139">Excel4/Excel12</span></span>](excel4-excel12.md)

