---
title: xlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303892"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="194e7-104">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="194e7-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="194e7-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="194e7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="194e7-106">Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="194e7-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="194e7-107">Dies entspricht dem Aufrufen der **AUFheben der Registrierung** aus einer Excel-XML-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="194e7-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="194e7-108">**xlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="194e7-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="194e7-109">Form 1: hebt die Registrierung eines einzelnen Befehls oder einer Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="194e7-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="194e7-110">Form 2: entladen und Deaktivieren einer XLL.</span><span class="sxs-lookup"><span data-stu-id="194e7-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="194e7-111">In Form 1 aufgerufen, reduziert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder eines Befehls, der zuvor mit **xlfRegister** oder **Register**registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="194e7-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="194e7-112">Wenn die Verwendungsanzahl bereits NULL ist, hat diese Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="194e7-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="194e7-113">Wenn die Verwendungsanzahl aller Funktionen in einer DLL 0 (null) erreicht, wird die DLL aus dem Arbeitsspeicher entladen.</span><span class="sxs-lookup"><span data-stu-id="194e7-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="194e7-114">**xlfRegister** (Form 1) definiert auch einen ausgeblendeten Namen, bei dem es sich um das Funktionstext Argument, _pxFunctionText_, handelt und das zur Registrierungs-ID der Funktion oder des Befehls ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="194e7-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="194e7-115">Beim Aufheben der Registrierung der Funktion sollte dieser Name mit **xlfSetName** gelöscht werden, damit der Funktionsname nicht mehr im Funktions-Assistenten aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="194e7-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="194e7-116">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="194e7-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="194e7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="194e7-117">Parameters</span></span>

<span data-ttu-id="194e7-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="194e7-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="194e7-119">Die Registrierungs-ID der Funktion, die aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="194e7-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="194e7-120">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="194e7-120">Property value/Return value</span></span>

<span data-ttu-id="194e7-121">Wenn erfolgreich, gibt **true** (**xltypeBool**) zurück, andernfalls wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="194e7-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="194e7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="194e7-122">Remarks</span></span>

<span data-ttu-id="194e7-123">Die Registrierungs-ID der Funktion wird von **xlfRegister** zurückgegeben, wenn die Funktion zuerst registriert wird.</span><span class="sxs-lookup"><span data-stu-id="194e7-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="194e7-124">Sie kann auch abgerufen werden, indem die [xlfRegisterId-Funktion](xlfregisterid.md) oder die [xlfEvaluate-Funktion](xlfevaluate.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="194e7-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="194e7-125">Beachten Sie, dass xlfRegisterId versucht, die Funktion zu registrieren, wenn Sie noch nicht registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="194e7-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="194e7-126">Aus diesem Grund sollten Sie, wenn Sie nur versuchen, die ID abzurufen, sodass Sie die Registrierung der Funktion aufheben können, diese abrufen, indem Sie den registrierten Namen an **xlfEvaluate**übergeben.</span><span class="sxs-lookup"><span data-stu-id="194e7-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="194e7-127">Wenn die Funktion nicht registriert wurde, schlägt **xlfEvaluate** mit einem #NAME fehl? Fehler.</span><span class="sxs-lookup"><span data-stu-id="194e7-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="194e7-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="194e7-128">Example</span></span>

<span data-ttu-id="194e7-129">Weitere Informationen finden Sie im \*\*\*\* Code für die `\SAMPLES\GENERIC\GENERIC.C`fExit-Funktion in.</span><span class="sxs-lookup"><span data-stu-id="194e7-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="194e7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="194e7-130">See also</span></span>

- [<span data-ttu-id="194e7-131">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="194e7-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="194e7-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="194e7-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="194e7-133">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="194e7-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="194e7-134">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="194e7-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

