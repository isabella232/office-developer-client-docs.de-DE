---
title: XlfUnregister (Formular 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Xlfunregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790604"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="346a9-104">XlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="346a9-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="346a9-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="346a9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="346a9-106">Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="346a9-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="346a9-107">Dies ist gleichbedeutend mit dem **UNREGISTER** aus einer Excel-XLM-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="346a9-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="346a9-108">**XlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="346a9-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="346a9-109">Formular 1: Hebt die Registrierung einen einzelnen Befehl oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="346a9-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="346a9-110">Formular 2: Entlädt und eine XLL deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="346a9-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="346a9-111">In Form 1 aufgerufen, verringert diese Funktion die Verwendungsanzahl einer DLL-Funktion oder den Befehl, der zuvor mit **XlfRegister** oder **Registrieren**registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="346a9-111">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**.</span></span> <span data-ttu-id="346a9-112">Wenn die Anzahl der Nutzung bereits gleich NULL ist, hat diese Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="346a9-112">If the usage count is already zero, this function has no effect.</span></span> <span data-ttu-id="346a9-113">Wenn die Verwendung aller Funktionen in einer DLL erreicht, wird die DLL aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="346a9-113">When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="346a9-114">**xlfRegister** (Form 1) definiert ausgeblendeten Name der im Argument der Funktion Text _PxFunctionText_, und die ausgewertet wird auch für die Funktion oder des Befehls Registration-ID.</span><span class="sxs-lookup"><span data-stu-id="346a9-114">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID.</span></span> <span data-ttu-id="346a9-115">Wenn die Funktion aus der Registrierung, sollte dieser Name mit **XlfSetName** , damit der Name der Funktion mithilfe des Funktions-Assistenten nicht mehr aufgeführt wird gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="346a9-115">When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard.</span></span> <span data-ttu-id="346a9-116">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="346a9-116">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="346a9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="346a9-117">Parameters</span></span>

<span data-ttu-id="346a9-118">_pxRegisterId_ (**XltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="346a9-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="346a9-119">Die Registrierung ID der Funktion nicht aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="346a9-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="346a9-120">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="346a9-120">Property value/Return value</span></span>

<span data-ttu-id="346a9-121">Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**), andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="346a9-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="346a9-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="346a9-122">Remarks</span></span>

<span data-ttu-id="346a9-123">Die Registrierung, die ID der Funktion von **XlfRegister** zurückgegeben wird, wenn die Funktion zuerst registriert.</span><span class="sxs-lookup"><span data-stu-id="346a9-123">The registration ID of the function is returned by **xlfRegister** when the function is first registered.</span></span> <span data-ttu-id="346a9-124">Es kann auch durch Aufrufen der [XlfRegisterId-Funktion](xlfregisterid.md) oder die [Funktion XlfEvaluate](xlfevaluate.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="346a9-124">It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="346a9-125">Hinweis: Diese XlfRegisterId versucht, die Funktion zu registrieren, wenn sie noch nicht registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="346a9-125">Note that xlfRegisterId tries to register the function if it has not already been registered.</span></span> <span data-ttu-id="346a9-126">Aus diesem Grund Wenn Sie nur die ID zu erhalten, damit Sie die Funktion, die Registrierung aufheben können versuchen empfiehlt sich diese abrufen, indem Sie den registrierten Namen an **XlfEvaluate**übergeben.</span><span class="sxs-lookup"><span data-stu-id="346a9-126">For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**.</span></span> <span data-ttu-id="346a9-127">Wenn die Funktion nicht registriert wurde, schlägt **XlfEvaluate** #NAME? Fehler.</span><span class="sxs-lookup"><span data-stu-id="346a9-127">If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="346a9-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="346a9-128">Example</span></span>

<span data-ttu-id="346a9-129">Anzeigen des Codes für die **fExit** -Funktion in `\SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="346a9-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="346a9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="346a9-130">See also</span></span>

- [<span data-ttu-id="346a9-131">XlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="346a9-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="346a9-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="346a9-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="346a9-133">XlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="346a9-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="346a9-134">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="346a9-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

