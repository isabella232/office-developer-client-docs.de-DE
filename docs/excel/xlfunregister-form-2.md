---
title: xlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310164"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="ed5aa-104">xlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="ed5aa-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="ed5aa-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed5aa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ed5aa-106">Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="ed5aa-107">Dies entspricht dem Aufrufen der **AUFheben der Registrierung** aus einer Excel-XML-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="ed5aa-108">**xlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="ed5aa-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="ed5aa-109">Form 1: hebt die Registrierung eines einzelnen Befehls oder einer Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="ed5aa-110">Form 2: entladen und Deaktivieren einer XLL.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="ed5aa-111">In Form 2 aufgerufen, wird durch diese Funktion erzwungen, dass eine DLL oder Coderessource vollständig entladen wird.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="ed5aa-112">Sie hebt die Registrierung aller Funktionen in einer DLL auf, auch wenn Sie derzeit von einem anderen Makro verwendet werden, unabhängig davon, welche Verwendungsanzahl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="ed5aa-113">Diese Funktion ruft **xlAutoClose**auf und hebt dann alle Funktionen in der dll auf.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="ed5aa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed5aa-114">Parameters</span></span>

<span data-ttu-id="ed5aa-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="ed5aa-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="ed5aa-116">Der Name der DLL.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ed5aa-117">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed5aa-117">Property value/Return value</span></span>

<span data-ttu-id="ed5aa-118">Wenn der Wert erfolgreich ist, wird **true** (**xltypeBool**) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="ed5aa-119">Wenn nicht erfolgreich, gibt **false**zurück.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed5aa-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed5aa-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="ed5aa-121">Rufen Sie diese Form der Funktion nicht aus der Implementierung des [xlAutoClose](xlautoclose.md) auf, um die Registrierung aller Ressourcen der DLL mit einem einfachen Funktionsaufruf aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="ed5aa-122">Dies führt zu einem rekursiven Aufruf von **xlAutoClose** und einem Stapelüberlauf.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="ed5aa-123">Namen löschen</span><span class="sxs-lookup"><span data-stu-id="ed5aa-123">Remember to delete names</span></span>

<span data-ttu-id="ed5aa-124">Wenn Sie das _pxFunctionText_ -Argument für **xlfRegister**angegeben haben, müssen Sie beim Registrieren der DLL-Funktionen und-Befehle die Namen explizit löschen, indem Sie **xlfSetName** für jeden einzelnen aufrufen, wobei das zweite Argument ausgelassen wird, sodass die die Funktion wird nicht mehr im Funktions-Assistenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="ed5aa-125">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="ed5aa-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed5aa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed5aa-126">See also</span></span>

- [<span data-ttu-id="ed5aa-127">xlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="ed5aa-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="ed5aa-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="ed5aa-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="ed5aa-129">xlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="ed5aa-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="ed5aa-130">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ed5aa-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

