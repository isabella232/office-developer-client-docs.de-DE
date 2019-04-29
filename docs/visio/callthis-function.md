---
title: CALLTHIS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf.
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413815"
---
# <a name="callthis-function"></a><span data-ttu-id="252c6-103">CALLTHIS Function</span><span class="sxs-lookup"><span data-stu-id="252c6-103">CALLTHIS Function</span></span>

<span data-ttu-id="252c6-104">Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf.</span><span class="sxs-lookup"><span data-stu-id="252c6-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="252c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="252c6-105">Syntax</span></span>

<span data-ttu-id="252c6-106">CALLTHIS ("\* \* *procedure* \* *", ["* \* *project* \* *"], [* \* *arg1* \* \*, \* \* *arg2* \* \*,...])</span><span class="sxs-lookup"><span data-stu-id="252c6-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="252c6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="252c6-107">Parameters</span></span>

|<span data-ttu-id="252c6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="252c6-108">**Name**</span></span>|<span data-ttu-id="252c6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="252c6-109">**Required/Optional**</span></span>|<span data-ttu-id="252c6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="252c6-110">**Data Type**</span></span>|<span data-ttu-id="252c6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="252c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="252c6-112">_Prozedur_</span><span class="sxs-lookup"><span data-stu-id="252c6-112">_procedure_</span></span> <br/> |<span data-ttu-id="252c6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="252c6-113">Required</span></span>  <br/> |<span data-ttu-id="252c6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="252c6-114">**String**</span></span> <br/> | <span data-ttu-id="252c6-115">Der Name der Prozedur, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="252c6-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="252c6-116">_Projekt_</span><span class="sxs-lookup"><span data-stu-id="252c6-116">_project_</span></span> <br/> |<span data-ttu-id="252c6-117">Optional</span><span class="sxs-lookup"><span data-stu-id="252c6-117">Optional</span></span>  <br/> |<span data-ttu-id="252c6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="252c6-118">**String**</span></span> <br/> |<span data-ttu-id="252c6-119">Das Projekt, das die Prozedur enthält.</span><span class="sxs-lookup"><span data-stu-id="252c6-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="252c6-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="252c6-120">_arg_</span></span> <br/> |<span data-ttu-id="252c6-121">Optional</span><span class="sxs-lookup"><span data-stu-id="252c6-121">Optional</span></span>  <br/> |<span data-ttu-id="252c6-122">**Number, String, Date oder Currency**</span><span class="sxs-lookup"><span data-stu-id="252c6-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="252c6-123">Wird als Parameter an die Prozedur übergeben,</span><span class="sxs-lookup"><span data-stu-id="252c6-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="252c6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="252c6-124">Remarks</span></span>

<span data-ttu-id="252c6-125">Im VBA-Projekt wird *Procedure* wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="252c6-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="252c6-126">Procedure (*vsoShape* as Visio. Shape [arg1 As Type, arg2 As Type...])</span><span class="sxs-lookup"><span data-stu-id="252c6-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="252c6-127">Dabei ist *vsoShape* ein Verweis auf das **Shape** -Objekt, das die CALLTHIS-Formel enthält, die ausgewertet wird, und _arg1_, *arg2* ... sind die in dieser Formel angegebenen Argumente.</span><span class="sxs-lookup"><span data-stu-id="252c6-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="252c6-128">Beachten Sie, dass *vsoShape* dem Argument "This" ähnelt, das an eine C++-Member-Prozedur übergeben wird. Daher lautet der Name "CALLTHIS".</span><span class="sxs-lookup"><span data-stu-id="252c6-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="252c6-129">Eine Zelle mit einer Formel, die CALLTHIS enthält, kann in der Tat wie folgt lauten: "diese Prozedur aufrufen und einen Verweis auf meine Form weitergeben."</span><span class="sxs-lookup"><span data-stu-id="252c6-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="252c6-130">Wenn _Project_ angegeben ist, scannt Microsoft Visio alle geöffneten Dokumente für das Projekt und __ die Aufruf _Prozedur_ in diesem Projekt.</span><span class="sxs-lookup"><span data-stu-id="252c6-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="252c6-131">Wenn _Project_ ausgelassen oder NULL ("") ist, wird von Visio die _Prozedur_ im VBA-Projekt des Dokuments, das die CALLTHIS-Formel enthält, die ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="252c6-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="252c6-132">Zahlen in _arg1_, _arg2..._ werden in externen Einheiten übergeben.</span><span class="sxs-lookup"><span data-stu-id="252c6-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="252c6-133">Wenn Sie beispielsweise den Wert der Zelle Height aus einer Form übergeben, die 3 cm hoch ist, wird 3 übergeben.</span><span class="sxs-lookup"><span data-stu-id="252c6-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="252c6-134">Wenn Sie verschiedene Einheiten mit einer Zahl übertragen möchten, verwenden Sie die FORMATEX-Funktion, oder erzwingen Sie explizit Einheiten, indem Sie ein NULL-Nummern Einheiten Paar (beispielsweise 0 Ft + Height) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="252c6-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="252c6-135">Das zweite Komma in der CALLTHIS-Funktion ist optional.</span><span class="sxs-lookup"><span data-stu-id="252c6-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="252c6-136">Es entspricht der Anzahl zusätzlicher Parameter, die der Prozedur hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="252c6-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="252c6-137">Wenn Sie keine zusätzlichen Parameter verwenden, `(vsoShape as Visio.Shape)` dürfen Sie das zweite Komma nicht hinzufügen; Verwenden Sie CALLTHIS ("",).</span><span class="sxs-lookup"><span data-stu-id="252c6-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="252c6-138">Wenn Sie beispielsweise zwei zusätzliche Parameter hinzufügen, verwenden Sie CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="252c6-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="252c6-139">Die CALLTHIS-Funktion wertet immer 0 aus, und der Aufruf der _Prozedur_ tritt während der Leerlaufzeit nach Abschluss des neuberechnungs Prozesses auf.</span><span class="sxs-lookup"><span data-stu-id="252c6-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="252c6-140">_procedure_ kann einen Wert zurückgeben, der jedoch von Visio ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="252c6-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="252c6-141">_Prozedur_ gibt einen Wert zurück, der von Visio erkannt werden kann, indem die Formel oder das Ergebnis einer anderen Zelle im Dokument festgelegt wird, nicht jedoch die Zelle, die _Prozedur_aufgerufen wird, es sei denn, Sie möchten die CALLTHIS-Formel überschreiben.</span><span class="sxs-lookup"><span data-stu-id="252c6-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="252c6-142">Der Unterschied zwischen der CALLTHIS-Funktion und der RUNADDON-Funktion besteht darin, dass das Projekt eines Dokuments auf kein anderes Projekt verweisen muss, um Prozeduren in diesem Projekt aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="252c6-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="252c6-143">VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine CALLTHIS-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird.</span><span class="sxs-lookup"><span data-stu-id="252c6-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="252c6-144">Wenn Sie das Dokument mit der Zelle, die die CALLTHIS-Funktion nutzt, schließen müssen, nutzen Sie eines der folgenden Verfahren:</span><span class="sxs-lookup"><span data-stu-id="252c6-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="252c6-145">Schließen Sie das Dokument mit Code, der kein VBA-Code ist.</span><span class="sxs-lookup"><span data-stu-id="252c6-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="252c6-146">Schließen Sie das Dokument von einem anderen Projekt aus als von jenem, das gerade geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="252c6-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="252c6-147">Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.</span><span class="sxs-lookup"><span data-stu-id="252c6-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="252c6-148">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="252c6-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="252c6-149">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="252c6-149">Example 1</span></span>

<span data-ttu-id="252c6-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="252c6-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="252c6-151">Ruft die in einem Modul abgelegte Prozedur namens p auf und übergibt den Wert der Zelle Height in Zentimetern, beispielsweise 7,62.</span><span class="sxs-lookup"><span data-stu-id="252c6-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="252c6-152">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="252c6-152">Example 2</span></span>

<span data-ttu-id="252c6-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="252c6-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="252c6-154">Ruft die in einem Modul abgelegte Prozedur q auf und übergibt die Höhe der Zelle in Zentimetern und die Breite in internen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="252c6-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="252c6-155">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="252c6-155">Example 3</span></span>

<span data-ttu-id="252c6-156">Verwenden Sie das folgende Verfahren im *ThisDocument* -Klassenmodul.</span><span class="sxs-lookup"><span data-stu-id="252c6-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="252c6-157">Verwenden Sie mit den oben beschriebenen Prozeduren eines der folgenden Syntaxbeispiele in der Zelle EventDblClick eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="252c6-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="252c6-158">CALLTHIS ("ThisDocument. A",)</span><span class="sxs-lookup"><span data-stu-id="252c6-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="252c6-159">CALLTHIS ("ThisDocument. B", "Click")</span><span class="sxs-lookup"><span data-stu-id="252c6-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="252c6-160">CALLTHIS("ThisDocument.C",,"Klicken Sie auf", "OK.")</span><span class="sxs-lookup"><span data-stu-id="252c6-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

