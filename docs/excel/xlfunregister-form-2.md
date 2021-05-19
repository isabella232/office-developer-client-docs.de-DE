---
title: xlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419905"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="a7db5-104">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="a7db5-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="a7db5-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a7db5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a7db5-106">Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von einem Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a7db5-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="a7db5-107">Dies entspricht dem Aufrufen von **UNREGISTER** aus Excel XLM-Makroblatts.</span><span class="sxs-lookup"><span data-stu-id="a7db5-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="a7db5-108">**xlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="a7db5-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="a7db5-109">Formular 1: Aufheben der Registrierung eines einzelnen Befehls oder einer Einzelnen Funktion.</span><span class="sxs-lookup"><span data-stu-id="a7db5-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="a7db5-110">Formular 2: Entladen und Deaktivieren einer XLL.</span><span class="sxs-lookup"><span data-stu-id="a7db5-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="a7db5-111">In Form 2 aufgerufen, erzwingt diese Funktion, dass eine DLL- oder Coderessource vollständig entladen wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="a7db5-112">Es wird die Registrierung aller Funktionen in einer DLL aufgehoben, auch wenn sie derzeit von einem anderen Makro verwendet werden, unabhängig von der Anzahl der Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="a7db5-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="a7db5-113">Diese Funktion ruft **xlAutoClose** auf und macht dann die Registrierung aller Funktionen in der DLL aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a7db5-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="a7db5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7db5-114">Parameters</span></span>

<span data-ttu-id="a7db5-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="a7db5-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="a7db5-116">Der Name der DLL.</span><span class="sxs-lookup"><span data-stu-id="a7db5-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a7db5-117">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7db5-117">Property value/Return value</span></span>

<span data-ttu-id="a7db5-118">Wenn dies erfolgreich ist, wird **TRUE** (**xltypeBool**) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7db5-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="a7db5-119">Wenn der Wert nicht erfolgreich ist, wird **FALSE zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="a7db5-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7db5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7db5-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="a7db5-121">Rufen Sie diese Form der Funktion nicht aus Ihrer Implementierung von [xlAutoClose](xlautoclose.md) auf, um die Registrierung aller Ressourcen der DLL mit einem einfachen Funktionsaufruf auf zu aufheben.</span><span class="sxs-lookup"><span data-stu-id="a7db5-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="a7db5-122">Dies führt zu rekursiven Aufrufen von **xlAutoClose** und einem Stapelüberlauf.</span><span class="sxs-lookup"><span data-stu-id="a7db5-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="a7db5-123">Vergessen Sie nicht, Namen zu löschen</span><span class="sxs-lookup"><span data-stu-id="a7db5-123">Remember to delete names</span></span>

<span data-ttu-id="a7db5-124">Wenn Sie das  _Argument pxFunctionText_ für **xlfRegister** angegeben haben, müssen Sie beim Registrieren der Funktionen und Befehle der DLL die Namen explizit löschen, indem Sie **xlfSetName** für jedes Argument aufrufen und das zweite Argument auslassen, sodass die Funktion nicht mehr im Funktions-Assistenten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7db5-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="a7db5-125">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a7db5-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7db5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7db5-126">See also</span></span>

- [<span data-ttu-id="a7db5-127">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="a7db5-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="a7db5-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a7db5-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="a7db5-129">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="a7db5-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="a7db5-130">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a7db5-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

