---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- Xlfregisterid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790609"
---
# <a name="xlfregisterid"></a><span data-ttu-id="b2ddb-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="b2ddb-104">xlfRegisterId</span></span>

<span data-ttu-id="b2ddb-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2ddb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b2ddb-106">Kann aus einer DLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="b2ddb-107">Wenn bereits eine Funktion registriert ist, wird die vorhandene Register-ID für diese Funktion ohne neu registrieren sie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="b2ddb-108">Wenn eine Funktion noch nicht registriert ist, registriert und gibt die resultierende Register-ID.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="b2ddb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2ddb-109">Parameters</span></span>

<span data-ttu-id="b2ddb-110">_pxModuleText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b2ddb-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b2ddb-111">Der Name der DLL, die mit der Funktion.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="b2ddb-112">_pxProcedure_ (**XltypeStr** oder **XltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="b2ddb-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="b2ddb-113">Wenn eine Zeichenfolge und den Namen der Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="b2ddb-114">Wenn eine Zahl, die Ordinal-Eigenschaft Anzahl der aufzurufenden Funktion exportieren.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="b2ddb-115">Verwenden Sie für die Klarheit und Stabilität immer in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="b2ddb-116">_pxTypeText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b2ddb-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b2ddb-117">Ein optionaler String gibt die Typen der alle Argumente an die Funktion und den Typ des Rückgabewerts der Funktion.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="b2ddb-118">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b2ddb-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="b2ddb-119">Dieses Argument kann für eine eigenständige DLL (XLL) definieren **XlAutoRegister**ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b2ddb-120">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2ddb-120">Property value/Return value</span></span>

<span data-ttu-id="b2ddb-121">Gibt die Register-ID der Funktion (**XltypeNum**), die bei nachfolgenden Aufrufen von **XlfUnregister**verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2ddb-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2ddb-122">Remarks</span></span>

<span data-ttu-id="b2ddb-123">Diese Funktion ist nützlich, wenn Sie keine Gedanken Wartung eine Register-ID möchten, jedoch Sie eine später zum Aufheben der Registrierung benötigen.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="b2ddb-124">Es ist außerdem hilfreich für das Zuweisen von Menüs, Tools und Schaltflächen in einer DLL wird die Funktion, die Sie zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="b2ddb-125">In denen eine DLL oder XLL-Funktion mit einem gültigen _PxFunctionText_ -Argument angegeben, um **XlfRegister**registriert wurde, kann auch seine Register-ID abgerufen werden, indem Sie die _PxFunctionText_ an die Funktion **XlfEvaluate**übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2ddb-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2ddb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2ddb-126">See also</span></span>

- [<span data-ttu-id="b2ddb-127">REGISTRIEREN</span><span class="sxs-lookup"><span data-stu-id="b2ddb-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="b2ddb-128">AUFHEBEN DER REGISTRIERUNG</span><span class="sxs-lookup"><span data-stu-id="b2ddb-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="b2ddb-129">Wichtige und nützliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b2ddb-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

