---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- XlfCaller-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790592"
---
# <a name="xlfcaller"></a><span data-ttu-id="8b273-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="8b273-104">xlfCaller</span></span>

 <span data-ttu-id="8b273-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b273-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8b273-106">Gibt Informationen zu der Zelle, einen Bereich von Zellen, Befehl auf ein Menü, das Tool auf einer Symbolleiste oder das Objekt, das aufgerufen wird, die DLL-Befehl oder eine Funktion, die derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b273-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="8b273-107">**Aufgerufen von Code**</span><span class="sxs-lookup"><span data-stu-id="8b273-107">**Code called from**</span></span>|<span data-ttu-id="8b273-108">**gibt zurück**</span><span class="sxs-lookup"><span data-stu-id="8b273-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b273-109">DLL-DATEI</span><span class="sxs-lookup"><span data-stu-id="8b273-109">DLL</span></span>  <br/> |<span data-ttu-id="8b273-110">Die Register-ID.</span><span class="sxs-lookup"><span data-stu-id="8b273-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="8b273-111">Eine einzelne Zelle</span><span class="sxs-lookup"><span data-stu-id="8b273-111">A single cell</span></span>  <br/> |<span data-ttu-id="8b273-112">Bezug auf eine einzelne Zelle.</span><span class="sxs-lookup"><span data-stu-id="8b273-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="8b273-113">Eine Zelle mit mehreren Arrayformel</span><span class="sxs-lookup"><span data-stu-id="8b273-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="8b273-114">Ein mit mehreren Zellbezug.</span><span class="sxs-lookup"><span data-stu-id="8b273-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="8b273-115">Eine bedingte Formatierung Ausdruck</span><span class="sxs-lookup"><span data-stu-id="8b273-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="8b273-116">Ein Verweis auf die Zelle, die auf der die Formatierung Bedingung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b273-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="8b273-117">Ein Menü</span><span class="sxs-lookup"><span data-stu-id="8b273-117">A menu</span></span>  <br/> | <span data-ttu-id="8b273-118">Ein Array mit vier Elementen einzeilige:</span><span class="sxs-lookup"><span data-stu-id="8b273-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="8b273-119">Die Leiste-ID.</span><span class="sxs-lookup"><span data-stu-id="8b273-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="8b273-120">Die Menüposition im.</span><span class="sxs-lookup"><span data-stu-id="8b273-120">The menu position.</span></span>  <br/>  <span data-ttu-id="8b273-121">Die Position des Untermenü.</span><span class="sxs-lookup"><span data-stu-id="8b273-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="8b273-122">Die Position des Befehls.</span><span class="sxs-lookup"><span data-stu-id="8b273-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="8b273-123">Eine Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="8b273-123">A toolbar</span></span>  <br/> | <span data-ttu-id="8b273-124">Eine einzeilige Matrix mit zwei Elementen:</span><span class="sxs-lookup"><span data-stu-id="8b273-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="8b273-125">Die Anzahl der Symbolleiste für die integrierten Symbolleisten oder den Namen der Symbolleiste für benutzerdefinierte Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="8b273-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="8b273-126">Die Position auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="8b273-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="8b273-127">Ein Graphic-Objekt</span><span class="sxs-lookup"><span data-stu-id="8b273-127">A graphic object</span></span>  <br/> |<span data-ttu-id="8b273-128">Der Objektbezeichner (Objektname).</span><span class="sxs-lookup"><span data-stu-id="8b273-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="8b273-129">Ein Befehl eine XlcOnEnter auf zugeordnet. Geben SIE Ereignis Trapping</span><span class="sxs-lookup"><span data-stu-id="8b273-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="8b273-130">Ein Verweis auf die Zelle oder die Zellen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b273-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="8b273-131">Ein Befehl eine XlcOnDoubleclick auf zugeordnet. DOUBLECLICK, Ereignis Trapping.</span><span class="sxs-lookup"><span data-stu-id="8b273-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="8b273-132">Die Zelle, die wurde doppelgeklickt (was nicht notwendigerweise die aktive Zelle).</span><span class="sxs-lookup"><span data-stu-id="8b273-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="8b273-133">Auto_öffnen-, AutoClose-, Auto_aktivieren- oder Auto_deaktivieren-Makro</span><span class="sxs-lookup"><span data-stu-id="8b273-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="8b273-134">Der Name des Blatts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b273-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="8b273-135">Andere Methoden nicht aufgeführt</span><span class="sxs-lookup"><span data-stu-id="8b273-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="8b273-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="8b273-136">#REF!</span></span> <span data-ttu-id="8b273-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="8b273-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="8b273-138">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b273-138">Property value/Return value</span></span>

<span data-ttu-id="8b273-139">Der Rückgabewert ist eines der folgenden **XLOPER**/ **XLOPER12** Datentypen: **XltypeRef**, **XltypeSRef**, **XltypeNum**, **XltypeStr**, **XltypeErr**oder **XltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="8b273-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="8b273-140">Da drei der folgenden Arten auf reservierter Speicher zeigen, sollten der Rückgabewert der **XlfCaller** immer freigegeben werden in einem Aufruf der [Funktion XlFree](xlfree.md) Wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8b273-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="8b273-141">Weitere Informationen zu **XLOPERs**/ **XLOPER12s** finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="8b273-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b273-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b273-142">Remarks</span></span>

<span data-ttu-id="8b273-143">Diese Funktion ist nur nicht-Arbeitsblatt, die aus einer Tabellenfunktion DLL/XLL aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="8b273-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="8b273-144">Andere XLM-Informationsfunktionen können nur von Befehlen oder Makroblatt Äquivalent aufgerufen werden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8b273-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="8b273-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b273-145">Example</span></span>

 <span data-ttu-id="8b273-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="8b273-146"></span></span> <span data-ttu-id="8b273-147">Diese Funktion ruft ein Makro mit Befehlen (XlcSelect) und funktionieren ordnungsgemäß nur, wenn von einem Makroblatt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8b273-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8b273-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b273-148">See also</span></span>



[<span data-ttu-id="8b273-149">Wichtige und nützliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8b273-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

