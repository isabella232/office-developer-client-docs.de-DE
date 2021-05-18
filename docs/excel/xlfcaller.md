---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405730"
---
# <a name="xlfcaller"></a><span data-ttu-id="95fce-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="95fce-104">xlfCaller</span></span>

 <span data-ttu-id="95fce-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="95fce-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="95fce-106">Gibt Informationen über die Zelle, den Zellbereich, den Befehl in einem Menü, ein Tool auf einer Symbolleiste oder ein Objekt zurück, das den aktuell ausgeführten DLL-Befehl oder die -Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="95fce-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="95fce-107">**Code, der von aufgerufen wird**</span><span class="sxs-lookup"><span data-stu-id="95fce-107">**Code called from**</span></span>|<span data-ttu-id="95fce-108">**gibt zurück**</span><span class="sxs-lookup"><span data-stu-id="95fce-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95fce-109">DLL</span><span class="sxs-lookup"><span data-stu-id="95fce-109">DLL</span></span>  <br/> |<span data-ttu-id="95fce-110">Die Register-ID.</span><span class="sxs-lookup"><span data-stu-id="95fce-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="95fce-111">Eine einzelne Zelle</span><span class="sxs-lookup"><span data-stu-id="95fce-111">A single cell</span></span>  <br/> |<span data-ttu-id="95fce-112">Ein Einzelzellenverweis.</span><span class="sxs-lookup"><span data-stu-id="95fce-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="95fce-113">Eine Arrayformel mit mehreren Zellen</span><span class="sxs-lookup"><span data-stu-id="95fce-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="95fce-114">Ein Verweis auf mehrere Zellen.</span><span class="sxs-lookup"><span data-stu-id="95fce-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="95fce-115">Ein bedingter Formatierungsausdruck</span><span class="sxs-lookup"><span data-stu-id="95fce-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="95fce-116">Ein Verweis auf die Zelle, auf die die Formatierungsbedingung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="95fce-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="95fce-117">Ein Menü</span><span class="sxs-lookup"><span data-stu-id="95fce-117">A menu</span></span>  <br/> | <span data-ttu-id="95fce-118">Ein Array mit vier Elementen in einer Zeile:</span><span class="sxs-lookup"><span data-stu-id="95fce-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="95fce-119">Die Balken-ID.</span><span class="sxs-lookup"><span data-stu-id="95fce-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="95fce-120">Die Menüposition.</span><span class="sxs-lookup"><span data-stu-id="95fce-120">The menu position.</span></span>  <br/>  <span data-ttu-id="95fce-121">Die Untermenüposition.</span><span class="sxs-lookup"><span data-stu-id="95fce-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="95fce-122">Die Befehlsposition.</span><span class="sxs-lookup"><span data-stu-id="95fce-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="95fce-123">Eine Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="95fce-123">A toolbar</span></span>  <br/> | <span data-ttu-id="95fce-124">Ein Array mit zwei Elementen in einer Zeile:</span><span class="sxs-lookup"><span data-stu-id="95fce-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="95fce-125">Die Symbolleistennummer für integrierte Symbolleisten oder der Symbolleistenname für benutzerdefinierte Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="95fce-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="95fce-126">Die Position auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="95fce-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="95fce-127">Ein Grafikobjekt</span><span class="sxs-lookup"><span data-stu-id="95fce-127">A graphic object</span></span>  <br/> |<span data-ttu-id="95fce-128">Der Objektbezeichner (Objektname).</span><span class="sxs-lookup"><span data-stu-id="95fce-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="95fce-129">Ein Befehl, der einem xlcOnEnter-On-Wert zugeordnet ist. ENTER, Ereignisfalle</span><span class="sxs-lookup"><span data-stu-id="95fce-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="95fce-130">Ein Verweis auf die eingegebene Zelle oder Zelle.</span><span class="sxs-lookup"><span data-stu-id="95fce-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="95fce-131">Ein Befehl, der einem xlcOnDoubleclick, ON, zugeordnet ist. DOUBLECLICK, Ereignisfalle.</span><span class="sxs-lookup"><span data-stu-id="95fce-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="95fce-132">Die Zelle, auf die doppelgeklickt wurde (nicht unbedingt die aktive Zelle).</span><span class="sxs-lookup"><span data-stu-id="95fce-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="95fce-133">Auto_Open, AutoClose, Auto_Activate oder Auto_Deactivate Makros</span><span class="sxs-lookup"><span data-stu-id="95fce-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="95fce-134">Der Name des Anrufblatts.</span><span class="sxs-lookup"><span data-stu-id="95fce-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="95fce-135">Andere Methoden nicht aufgeführt</span><span class="sxs-lookup"><span data-stu-id="95fce-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="95fce-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="95fce-136">#REF!</span></span> <span data-ttu-id="95fce-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="95fce-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="95fce-138">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95fce-138">Property value/Return value</span></span>

<span data-ttu-id="95fce-139">Der Rückgabewert ist einer der folgenden **XLOPER** /  **XLOPER12-Datentypen:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** oder **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="95fce-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="95fce-140">Da drei dieser Typen auf zugewiesenen Arbeitsspeicher verweisen, sollte der Rückgabewert von **xlfCaller** immer in einem Aufruf der [xlFree-Funktion](xlfree.md) frei, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="95fce-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="95fce-141">Weitere Informationen zu **XLOPERs** /  **XLOPER12s** finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="95fce-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95fce-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95fce-142">Remarks</span></span>

<span data-ttu-id="95fce-143">Diese Funktion ist die einzige Nicht-Arbeitsblatt-Funktion, die von einer DLL/XLL-Arbeitsblattfunktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="95fce-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="95fce-144">Andere XLM-Informationsfunktionen können nur von Befehlen oder makroblattäquivalenten Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="95fce-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="95fce-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="95fce-145">Example</span></span>

 <span data-ttu-id="95fce-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="95fce-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="95fce-147">Diese Funktion ruft ein Befehlsmakro (xlcSelect) auf und funktioniert nur dann ordnungsgemäß, wenn sie von einem Makroblatt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="95fce-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="95fce-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95fce-148">See also</span></span>



[<span data-ttu-id="95fce-149">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="95fce-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

