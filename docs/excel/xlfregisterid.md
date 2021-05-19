---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420059"
---
# <a name="xlfregisterid"></a><span data-ttu-id="7c6cc-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="7c6cc-104">xlfRegisterId</span></span>

<span data-ttu-id="7c6cc-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c6cc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c6cc-106">Kann von einer DLL aufgerufen werden, die selbst von der Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="7c6cc-107">Wenn eine Funktion bereits registriert ist, gibt sie die vorhandene Register-ID für diese Funktion zurück, ohne sie erneut zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="7c6cc-108">Wenn eine Funktion noch nicht registriert ist, registriert sie sie und gibt die resultierende Register-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="7c6cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c6cc-109">Parameters</span></span>

<span data-ttu-id="7c6cc-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="7c6cc-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="7c6cc-111">Der Name der DLL, die die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="7c6cc-112">_pxProcedure_ (**xltypeStr** oder **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="7c6cc-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="7c6cc-113">Wenn eine Zeichenfolge, der Name der zu aufrufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="7c6cc-114">Wenn eine Zahl, die Ordnungsexportnummer der zu aufrufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="7c6cc-115">Verwenden Sie aus Gründen der Übersichtlichkeit und Robustheit immer das Zeichenfolgenformular.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="7c6cc-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="7c6cc-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="7c6cc-117">Eine optionale Zeichenfolge, die die Typen aller Argumente für die Funktion und den Typ des Rückgabewerts der Funktion an gibt.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="7c6cc-118">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7c6cc-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="7c6cc-119">Dieses Argument kann für eine eigenständige DLL (XLL), die xlAutoRegister definiert, **ausgelassen werden.**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7c6cc-120">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c6cc-120">Property value/Return value</span></span>

<span data-ttu-id="7c6cc-121">Gibt die Register-ID der Funktion (**xltypeNum**) zurück, die bei nachfolgenden Aufrufen von **xlfUnregister verwendet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c6cc-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c6cc-122">Remarks</span></span>

<span data-ttu-id="7c6cc-123">Diese Funktion ist nützlich, wenn Sie sich keine Gedanken über die Verwaltung einer Register-ID machen möchten, sie jedoch später zum Aufheben der Registrierung benötigen.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="7c6cc-124">Es ist auch hilfreich, Menüs, Tools und Schaltflächen zuzuordnen, wenn sich die funktion, die Sie zuweisen möchten, in einer DLL befindet.</span><span class="sxs-lookup"><span data-stu-id="7c6cc-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="7c6cc-125">Wenn eine DLL- oder XLL-Funktion mit einem gültigen _pxFunctionText-Argument_ registriert wurde, das **xlfRegister** bereitgestellt wurde, kann die Register-ID auch durch Übergeben des _pxFunctionText_ an die Funktion **xlfEvaluate erhalten werden.**</span><span class="sxs-lookup"><span data-stu-id="7c6cc-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c6cc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c6cc-126">See also</span></span>

- [<span data-ttu-id="7c6cc-127">REGISTRIEREN</span><span class="sxs-lookup"><span data-stu-id="7c6cc-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="7c6cc-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="7c6cc-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="7c6cc-129">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7c6cc-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

