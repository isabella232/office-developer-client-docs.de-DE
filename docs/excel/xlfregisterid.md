---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303878"
---
# <a name="xlfregisterid"></a><span data-ttu-id="b139e-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="b139e-104">xlfRegisterId</span></span>

<span data-ttu-id="b139e-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b139e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b139e-106">Kann von einer DLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b139e-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="b139e-107">Wenn eine Funktion bereits registriert ist, wird die vorhandene Register-ID für diese Funktion zurückgegeben, ohne Sie erneut zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b139e-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="b139e-108">Wenn eine Funktion noch nicht registriert ist, registriert Sie Sie und gibt die resultierende Register-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="b139e-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="b139e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b139e-109">Parameters</span></span>

<span data-ttu-id="b139e-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b139e-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b139e-111">Der Name der DLL, die die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="b139e-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="b139e-112">_pxProcedure_ (**xltypeStr** oder **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="b139e-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="b139e-113">Wenn eine Zeichenfolge, der Name der Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b139e-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="b139e-114">Wenn eine Zahl, die ordinale Export Nummer der Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b139e-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="b139e-115">Aus Gründen der Klarheit und Robustheit sollte immer die Zeichenfolgeform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b139e-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="b139e-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b139e-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b139e-117">Eine optionale Zeichenfolge, die die Typen aller Argumente für die Funktion und den Typ des Rückgabewerts der Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="b139e-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="b139e-118">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b139e-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="b139e-119">Dieses Argument kann für eine eigenständige DLL (XLL), die **xlAutoRegister**definiert, ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="b139e-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b139e-120">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b139e-120">Property value/Return value</span></span>

<span data-ttu-id="b139e-121">Gibt die Register-ID der Funktion (**xltypeNum**) zurück, die in nachfolgenden Aufrufen von **xlfUnregister**verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b139e-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b139e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b139e-122">Remarks</span></span>

<span data-ttu-id="b139e-123">Diese Funktion ist nützlich, wenn Sie sich nicht um die Verwaltung einer Register-ID kümmern möchten, aber Sie müssen Sie später für die Registrierung aufheben.</span><span class="sxs-lookup"><span data-stu-id="b139e-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="b139e-124">Es eignet sich auch für die Zuweisung zu Menüs, Tools und Schaltflächen, wenn die Funktion, die Sie zuweisen möchten, sich in einer DLL befindet.</span><span class="sxs-lookup"><span data-stu-id="b139e-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="b139e-125">Wenn eine DLL-oder XLL-Funktion mit einem gültigen _pxFunctionText_ -Argument registriert wurde, das an **xlfRegister**übermittelt wurde, kann die Register-ID auch abgerufen werden, indem die _pxFunctionText_ an die Funktion **xlfEvaluate**übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b139e-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b139e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b139e-126">See also</span></span>

- [<span data-ttu-id="b139e-127">Registrieren</span><span class="sxs-lookup"><span data-stu-id="b139e-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="b139e-128">Registrierung</span><span class="sxs-lookup"><span data-stu-id="b139e-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="b139e-129">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b139e-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

