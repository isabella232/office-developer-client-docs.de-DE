---
title: XlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- Xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790619"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="5e172-104">XlfUnregister (Formular 2)</span><span class="sxs-lookup"><span data-stu-id="5e172-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="5e172-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5e172-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5e172-106">Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5e172-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="5e172-107">Dies ist gleichbedeutend mit dem **UNREGISTER** aus einer Excel-XLM-Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="5e172-107">This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="5e172-108">**XlfUnregister** kann in zwei Formen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="5e172-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="5e172-109">Formular 1: Hebt die Registrierung einen einzelnen Befehl oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="5e172-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="5e172-110">Formular 2: Entlädt und eine XLL deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e172-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="5e172-111">In Form 2 aufgerufen, erzwingt diese Funktion eine DLL oder Code-Ressource vollständig entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5e172-111">Called in Form 2, this function forces a DLL or code resource to be unloaded completely.</span></span> <span data-ttu-id="5e172-112">Es hebt die Registrierung aller die Funktionen in einer DLL, auch wenn sie gerade von einem anderen Makro, unabhängig davon, welche die Verwendungszähler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e172-112">It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count.</span></span> <span data-ttu-id="5e172-113">Diese Funktion ruft **XlAutoClose**und hebt die Registrierung klicken Sie dann auf alle Funktionen in der DLL.</span><span class="sxs-lookup"><span data-stu-id="5e172-113">This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="5e172-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e172-114">Parameters</span></span>

<span data-ttu-id="5e172-115">_pxModuleText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5e172-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5e172-116">Der Name der DLL.</span><span class="sxs-lookup"><span data-stu-id="5e172-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5e172-117">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e172-117">Property value/Return value</span></span>

<span data-ttu-id="5e172-118">Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="5e172-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="5e172-119">Wenn nicht erfolgreich ist, gibt **FALSE**zurück.</span><span class="sxs-lookup"><span data-stu-id="5e172-119">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e172-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e172-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="5e172-121">Rufen Sie diese Form der Funktion nicht die Implementierung von der [XlAutoClose](xlautoclose.md) versucht, alle Ressourcen mit einem einfachen Funktionsaufruf die DLL Aufheben der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="5e172-121">Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call.</span></span> <span data-ttu-id="5e172-122">Dies führt zu rekursiven Aufruf der **XlAutoClose** und einen Stapelüberlauf.</span><span class="sxs-lookup"><span data-stu-id="5e172-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="5e172-123">Denken Sie daran, Namen löschen</span><span class="sxs-lookup"><span data-stu-id="5e172-123">Remember to delete names</span></span>

<span data-ttu-id="5e172-124">Wenn Sie das Argument _PxFunctionText_ **XlfRegister**, bei der Registrierung der DLL Funktionen und Befehle angegeben, Sie müssen explizit löschen die Namen durch Aufrufen von **XlfSetName** für jede Datei das zweite Argument auslassen, damit die Funktion im Funktions-Assistenten wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e172-124">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard.</span></span> <span data-ttu-id="5e172-125">Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="5e172-125">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5e172-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e172-126">See also</span></span>

- [<span data-ttu-id="5e172-127">XlfRegister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="5e172-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="5e172-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="5e172-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="5e172-129">XlfUnregister (Formular 1)</span><span class="sxs-lookup"><span data-stu-id="5e172-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="5e172-130">Wichtige und nützliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5e172-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

