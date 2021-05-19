---
title: xlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410084"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="d4e11-104">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="d4e11-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="d4e11-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4e11-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d4e11-106">Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von einem Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d4e11-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="d4e11-107">Dies entspricht dem Aufrufen von **UNREGISTER** aus Excel XLM-Makroblatts.</span><span class="sxs-lookup"><span data-stu-id="d4e11-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="d4e11-108">**xlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="d4e11-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="d4e11-109">Formular 1: Aufheben der Registrierung eines einzelnen Befehls oder einer Einzelnen Funktion.</span><span class="sxs-lookup"><span data-stu-id="d4e11-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="d4e11-110">Formular 2: Entladen und Deaktivieren einer XLL.</span><span class="sxs-lookup"><span data-stu-id="d4e11-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="d4e11-111">In Form 1 aufgerufen, reduziert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder eines Befehls, die zuvor mithilfe von **xlfRegister** oder **REGISTER registriert wurde.**</span><span class="sxs-lookup"><span data-stu-id="d4e11-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="d4e11-112">Wenn die Verwendungsanzahl bereits null ist, hat diese Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="d4e11-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="d4e11-113">Wenn die Verwendungsanzahl aller Funktionen in einer DLL null erreicht, wird die DLL aus dem Arbeitsspeicher entladen.</span><span class="sxs-lookup"><span data-stu-id="d4e11-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="d4e11-114">**xlfRegister** (Form 1) definiert auch einen ausgeblendeten Namen, bei dem es sich um das Funktionstextargument  _pxFunctionText_ handelt und der zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d4e11-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="d4e11-115">Wenn Sie die Registrierung der Funktion aufheben, sollte dieser Name mithilfe von **xlfSetName** gelöscht werden, damit der Funktionsname nicht mehr vom Funktionsassistenten aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e11-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="d4e11-116">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="d4e11-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="d4e11-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4e11-117">Parameters</span></span>

<span data-ttu-id="d4e11-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="d4e11-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="d4e11-119">Die Registrierungs-ID der Funktion, die nicht registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4e11-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d4e11-120">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4e11-120">Property value/Return value</span></span>

<span data-ttu-id="d4e11-121">Wenn dies erfolgreich ist, wird **TRUE** (**xltypeBool**) zurückgegeben, andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="d4e11-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4e11-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4e11-122">Remarks</span></span>

<span data-ttu-id="d4e11-123">Die Registrierungs-ID der Funktion wird von **xlfRegister** zurückgegeben, wenn die Funktion zum ersten Mal registriert wird.</span><span class="sxs-lookup"><span data-stu-id="d4e11-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="d4e11-124">Sie kann auch durch Aufrufen der [xlfRegisterId-Funktion oder](xlfregisterid.md) der [xlfEvaluate-Funktion erhalten werden.](xlfevaluate.md)</span><span class="sxs-lookup"><span data-stu-id="d4e11-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="d4e11-125">Beachten Sie, dass xlfRegisterId versucht, die Funktion zu registrieren, wenn sie noch nicht registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4e11-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="d4e11-126">Wenn Sie daher nur versuchen, die ID zu erhalten, damit Sie die Registrierung der Funktion aufheben können, ist es besser, sie zu erhalten, indem Sie den registrierten Namen an **xlfEvaluate übergeben.**</span><span class="sxs-lookup"><span data-stu-id="d4e11-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="d4e11-127">Wenn die Funktion nicht registriert wurde, **schlägt xlfEvaluate** mit einem #NAME? error.</span><span class="sxs-lookup"><span data-stu-id="d4e11-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d4e11-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4e11-128">Example</span></span>

<span data-ttu-id="d4e11-129">Weitere Informationen finden Sie im Code für die **fExit-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="d4e11-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="d4e11-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4e11-130">See also</span></span>

- [<span data-ttu-id="d4e11-131">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="d4e11-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="d4e11-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="d4e11-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="d4e11-133">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="d4e11-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="d4e11-134">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d4e11-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

