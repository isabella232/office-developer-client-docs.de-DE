---
title: SETATREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Leitet aktualisierte Werte, die Aktionen in der Benutzeroberfläche (UI) oder die Automatisierung in eine andere Zelle entsteht.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797994"
---
# <a name="setatref-function"></a><span data-ttu-id="05071-103">SETATREF Function</span><span class="sxs-lookup"><span data-stu-id="05071-103">SETATREF Function</span></span>

<span data-ttu-id="05071-104">Leitet aktualisierte Werte, die Aktionen in der Benutzeroberfläche (UI) oder die Automatisierung in eine andere Zelle entsteht.</span><span class="sxs-lookup"><span data-stu-id="05071-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="05071-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05071-105">Syntax</span></span>

<span data-ttu-id="05071-106">SETATREF (** *Verweis* ** [, ** *Set_expression* ** [, ** *Ignore_eval* **]])</span><span class="sxs-lookup"><span data-stu-id="05071-106">SETATREF(** *reference* ** [, ** *set_expression* ** [, ** *ignore_eval* ** ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="05071-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="05071-107">Parameters</span></span>

|<span data-ttu-id="05071-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="05071-108">**Name**</span></span>|<span data-ttu-id="05071-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="05071-109">**Required/Optional**</span></span>|<span data-ttu-id="05071-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="05071-110">**Data Type**</span></span>|<span data-ttu-id="05071-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05071-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="05071-112">_Referenz (engl.)_</span><span class="sxs-lookup"><span data-stu-id="05071-112">_reference_</span></span> <br/> |<span data-ttu-id="05071-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="05071-113">Required</span></span>  <br/> |<span data-ttu-id="05071-114">**String**</span><span class="sxs-lookup"><span data-stu-id="05071-114">**String**</span></span> <br/> |<span data-ttu-id="05071-115">Ein Bezug auf die Zelle, in die Aktualisierungen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="05071-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="05071-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="05071-116">_set_expression_</span></span> <br/> |<span data-ttu-id="05071-117">Optional</span><span class="sxs-lookup"><span data-stu-id="05071-117">Optional</span></span>  <br/> |<span data-ttu-id="05071-118">**String**</span><span class="sxs-lookup"><span data-stu-id="05071-118">**String**</span></span> <br/> |<span data-ttu-id="05071-119">Ein Ausdruck, der _Reference_zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="05071-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="05071-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="05071-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="05071-121">Optional</span><span class="sxs-lookup"><span data-stu-id="05071-121">Optional</span></span>  <br/> |<span data-ttu-id="05071-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="05071-122">**Boolean**</span></span> <br/> |<span data-ttu-id="05071-123">Wenn "true" ergibt die SETATREF-Funktion (0) 0 (null); ist der Wert FALSE ergibt (Standardeinstellung) die SETATREF-Funktion den Wert des _Verweises_.</span><span class="sxs-lookup"><span data-stu-id="05071-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05071-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05071-124">Remarks</span></span>

<span data-ttu-id="05071-125">Wenn eine Benutzeraktion im Zeichnungsfenster oder eine Automatisierungsmethode bewirkt, Microsoft Visio dass, eine Zelle mit einer SETATREF-Formel zu aktualisieren, wird der Wert stattdessen auf die Zelle, die durch die SETATREF-Formel ( _Referenz_) umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05071-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="05071-126">Die Formel in die Zelle mit der SETATREF-Funktion bleibt intakt.</span><span class="sxs-lookup"><span data-stu-id="05071-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="05071-127">Wenn _Set_expression_ ausgelassen wird, wird der Wert festgelegt, in der Benutzeroberfläche oder mithilfe der Automatisierung der referenzierten Zelle zugewiesen. Andernfalls werden der Inhalt von _Set_expression_ der referenzierten Zelle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="05071-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="05071-128">Dadurch wird den neuen Wert geändert oder transformiert werden, bevor der referenzierten Zelle zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="05071-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="05071-129">Die SETATREF-Funktion besitzt zwei verwandte Funktionen:</span><span class="sxs-lookup"><span data-stu-id="05071-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="05071-130">Die SETATREFEXPR-Funktion, die Sie verwenden können, den neuen Wert innerhalb von _Set_expression_dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05071-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="05071-131">Beispielsweise _Set_expression_ () SETATREFEXPR-2 in.</span><span class="sxs-lookup"><span data-stu-id="05071-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="05071-132">kann verwendet werden, 2 Zoll vom SETATREFEXPR-Ergebnis subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="05071-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="05071-133">Die SETATREFEVAL-Funktion, die Sie verwenden können, um anzugeben, dass ein Teil von _Set_expression_ ausgewertet und durch das Ergebnis ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="05071-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="05071-134">Die SETATREF-Funktion dient zur Verwendung in Zellen, die durch Benutzeraktionen im Zeichnungsfenster geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="05071-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="05071-135">Folgenden Zellen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="05071-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="05071-136">Abschnitt ShapeTransform - Zelle Width, Height, Angle, PinX und PinY</span><span class="sxs-lookup"><span data-stu-id="05071-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="05071-137">Abschnitt Text Transform - Zelle TxtWidth, TxtHeight, TxtAngle, TxtPinX und TxtPinY</span><span class="sxs-lookup"><span data-stu-id="05071-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="05071-138">Abschnitt 1-D Endpoints - Zelle BeginX, BeginY, EndX und EndY</span><span class="sxs-lookup"><span data-stu-id="05071-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="05071-139">Abschnitt Controls - Zelle Controls.X und Controls.Y</span><span class="sxs-lookup"><span data-stu-id="05071-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="05071-140">Abschnitt Shape Data</span><span class="sxs-lookup"><span data-stu-id="05071-140">Shape Data section</span></span>
    
<span data-ttu-id="05071-141">Da SETATREF den Speicherort geändert wird, in dem-Werte Zelle ändern, wirkt sich dies auf das Auslösen von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="05071-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="05071-142">Wenn eine Zelle SETATREF enthält, ausgelöst, die **FormulaChanged** und **CellChanged** -Ereignisse für die Zelle, die von SETATREF Zelle SETATREF verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="05071-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="05071-143">Wenn eine Zelle mit SETATREF auch SETATREFEXPR enthält, wird das **FormulaChanged** -Ereignis auch für die Zelle mit SETATREF ausgelöst, da ein Parameter-Funktion geändert wird.</span><span class="sxs-lookup"><span data-stu-id="05071-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="05071-144">Beachten Sie folgende weiteren wichtigen Hinweise zur SETATREF-Funktion:</span><span class="sxs-lookup"><span data-stu-id="05071-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="05071-145">SETATREF-Funktionen können bis zu 10 Referenzen auf andere SETATREF-Funktionen verketten.</span><span class="sxs-lookup"><span data-stu-id="05071-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="05071-146">Zellen können zusätzlich zur SETATREF-Funktion andere Ausdrücke enthalten, einschließlich mehrerer Vorkommen von SETATREF in einer einzigen Zelle.</span><span class="sxs-lookup"><span data-stu-id="05071-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="05071-147">Wenn Shapes verbunden werden, folgt Visio der SETATREF-Referenzkette innerhalb desselben Blatts und platziert Klebeformeln in der referenzierten Zelle.</span><span class="sxs-lookup"><span data-stu-id="05071-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="05071-148">Die Automatisierung erkennt die SETATREF-Funktion und folgt der Kette referenzierter Zellen.</span><span class="sxs-lookup"><span data-stu-id="05071-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="05071-149">Ebenso wie GUARD schützt SETATREF die Zellen nicht vor Änderungen, die über die SETF-Funktion im ShapeSheet-Fenster vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="05071-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="05071-150">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05071-150">Example1</span></span>

<span data-ttu-id="05071-151">Angenommen, ein Shape besitzt die benutzerdefinierte Eigenschaft Breite und die Zelle Width im Abschnitt Shape Transform enthält folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="05071-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="05071-152">=SETATREF(Prop.Width)</span><span class="sxs-lookup"><span data-stu-id="05071-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="05071-153">Wenn ein Benutzer die Breite des Shapes in der Benutzeroberfläche ändern, wird der neue Wert der Zelle Prop.Width nicht auf die Zelle Width im Abschnitt ShapeTransform-Zelle zugewiesen. die Formel in die Zelle Width bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="05071-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="05071-154">Sie können auch die Breite des Shapes mithilfe von Shape-Daten festlegen.</span><span class="sxs-lookup"><span data-stu-id="05071-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="05071-155">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="05071-155">Example2</span></span>

<span data-ttu-id="05071-p107">Visio-Lösungen enthalten oft Shapes mit hierarchischen Beziehungen, bei denen untergeordnete Shapes verschoben werden müssen, wenn ein übergeordnetes Shape verschoben wird. Im folgenden Beispiel wird beschrieben, wie Sie diese Beziehung mithilfe der SETATREF-Funktion im ShapeSheet-Fenster verwalten können.</span><span class="sxs-lookup"><span data-stu-id="05071-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="05071-p108">Folgende Formeln sind im Abschnitt Shape Transform des untergeordneten Shapes enthalten. Außerdem werden die benutzerdefinierten Zellen User.DeltaX und User.DeltaY definiert, die den Abstand von ParentShape verfolgen. Auf diese Weise kann das untergeordnete Shape verschoben werden, wenn das übergeordnete Shape verschoben wird, und die hierarchische Beziehung bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="05071-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="05071-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="05071-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="05071-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="05071-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="05071-163">Wenn das untergeordnete Shape mithilfe der Benutzeroberfläche verschoben wird, werden die neuen Werte für DrehbezX und DrehbezY als Parameter der SETATREFEXPR-Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05071-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="05071-164">Die SETATREF-Funktion wertet die Formel in SETATREFEVAL eingeschlossen und ersetzt Sie durch ihre Ergebnisse DrehbezX und DrehbezY, und klicken Sie dann die Benutzerzellen verwiesen wird, in der enthaltene und User.DeltaY definiert die resultierende Formel zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="05071-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="05071-165">Schließlich werden die von SETATREF (User.DeltaX oder User.DeltaY definiert) zurückgegebenen Werte den Pin-Speicherort des ParentShape zum Berechnen des untergeordneten Shapes Pin Speicherort hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05071-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

