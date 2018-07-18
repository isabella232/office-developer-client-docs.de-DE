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
description: Ruft eine Prozedur in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt.
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796563"
---
# <a name="callthis-function"></a><span data-ttu-id="43540-103">CALLTHIS Function</span><span class="sxs-lookup"><span data-stu-id="43540-103">CALLTHIS Function</span></span>

<span data-ttu-id="43540-104">Ruft eine Prozedur in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt.</span><span class="sxs-lookup"><span data-stu-id="43540-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="43540-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43540-105">Syntax</span></span>

<span data-ttu-id="43540-106">CALLTHIS ("** *Verfahren* **", ["** *Project* **"], [** *arg1* **, ** *arg2* **,...])</span><span class="sxs-lookup"><span data-stu-id="43540-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43540-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43540-107">Parameters</span></span>

|<span data-ttu-id="43540-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="43540-108">**Name**</span></span>|<span data-ttu-id="43540-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="43540-109">**Required/Optional**</span></span>|<span data-ttu-id="43540-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="43540-110">**Data Type**</span></span>|<span data-ttu-id="43540-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43540-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43540-112">_Verfahren_</span><span class="sxs-lookup"><span data-stu-id="43540-112">_procedure_</span></span> <br/> |<span data-ttu-id="43540-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="43540-113">Required</span></span>  <br/> |<span data-ttu-id="43540-114">**String**</span><span class="sxs-lookup"><span data-stu-id="43540-114">**String**</span></span> <br/> | <span data-ttu-id="43540-115">Der Name der Prozedur, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43540-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="43540-116">_Projekt_</span><span class="sxs-lookup"><span data-stu-id="43540-116">_project_</span></span> <br/> |<span data-ttu-id="43540-117">Optional</span><span class="sxs-lookup"><span data-stu-id="43540-117">Optional</span></span>  <br/> |<span data-ttu-id="43540-118">**String**</span><span class="sxs-lookup"><span data-stu-id="43540-118">**String**</span></span> <br/> |<span data-ttu-id="43540-119">Das Projekt, das die Prozedur enthält.</span><span class="sxs-lookup"><span data-stu-id="43540-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="43540-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="43540-120">_arg_</span></span> <br/> |<span data-ttu-id="43540-121">Optional</span><span class="sxs-lookup"><span data-stu-id="43540-121">Optional</span></span>  <br/> |<span data-ttu-id="43540-122">**Number, String, Date oder Currency**</span><span class="sxs-lookup"><span data-stu-id="43540-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="43540-123">Wird als Parameter an die Prozedur übergeben,</span><span class="sxs-lookup"><span data-stu-id="43540-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43540-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43540-124">Remarks</span></span>

<span data-ttu-id="43540-125">In das VBA-Projekt ist *Procedure* wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="43540-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="43540-126">Prozedur (*VsoShape* als Visio.Shape [arg1 als Typ arg2 als Type...])</span><span class="sxs-lookup"><span data-stu-id="43540-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="43540-127">wobei *VsoShape* einen Verweis auf ist sind das **Shape** -Objekt, das das auszuwertende CALLTHIS-Formel enthält, und _arg1_, *arg2* ... die Argumente in dieser Formel angegeben.</span><span class="sxs-lookup"><span data-stu-id="43540-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="43540-128">Beachten Sie, dass diese *VsoShape* sehr ähnlich wie das "this"-Argument in C++ Member-Prozedur übergeben wird. daher der Name "CALLTHIS".</span><span class="sxs-lookup"><span data-stu-id="43540-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="43540-129">Wirksam, kann eine Zelle, die eine Formel enthält, die CALLTHIS gelesen werden, wie "Diese Prozedur aufrufen und sie einen Verweis auf Mein Shape übergeben."</span><span class="sxs-lookup"><span data-stu-id="43540-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="43540-130">Wenn das _Projekt_ angegeben ist, durchsucht Microsoft Visio alle geöffneten Dokumente für die eine enthaltenden _Projekt-_ und Anrufe _Verfahren_ in diesem Projekt.</span><span class="sxs-lookup"><span data-stu-id="43540-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="43540-131">_Projekt_ ist nicht angegeben oder null (""); Visio wird davon ausgegangen, _Prozedur_ befindet sich in das VBA-Projekt des Dokuments, die die CALLTHIS-Formel enthält, die ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="43540-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="43540-132">Zahlen in _arg1_, _arg2..._ werden in externen Einheiten übergeben.</span><span class="sxs-lookup"><span data-stu-id="43540-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="43540-133">Wenn Sie den Wert der Zelle Height aus einem Shape übergeben, die 3 cm hoch ist, wird beispielsweise 3 übergeben.</span><span class="sxs-lookup"><span data-stu-id="43540-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="43540-134">Um andere Einheiten mit einer Zahl zu übergeben, verwenden Sie die FORMATEX-Funktion oder Erstellen einer Einheiten explizit durch null Zahl-Einheit-Paar, z. B. 0Fuß + Höhe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43540-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="43540-135">Das zweite Komma in der CALLTHIS-Funktion ist optional.</span><span class="sxs-lookup"><span data-stu-id="43540-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="43540-136">Es entspricht der Anzahl zusätzlicher Parameter an die Prozedur hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="43540-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="43540-137">Wenn Sie zusätzliche Parameter nicht verwenden, mit Ausnahme der `(vsoShape as Visio.Shape)` , fügen Sie das zweite Komma; keine Verwenden Sie CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="43540-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="43540-138">Wenn Sie zwei zusätzliche Parameter hinzufügen, verwenden Sie beispielsweise CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="43540-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="43540-139">Die CALLTHIS-Funktion wird stets als 0 ausgewertet, und der Aufruf von _Procedure_ erfolgt in der Leerlaufzeit nach Abschluss des neuberechnung Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="43540-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="43540-140">_Procedure_ kann einen Wert zurückgeben, jedoch Visio ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="43540-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="43540-141">_Prozedur_ gibt eines Werts, das durch Festlegen der Formel oder das Ergebnis einer anderen Zelle im Dokument Visio erkennen kann, jedoch nicht auf die Zelle, die _Prozedur_aufgerufen, es sei denn, Sie die CALLTHIS-Formel überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="43540-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="43540-142">Der Unterschied zwischen der CALLTHIS-Funktion und der RUNADDON-Funktion besteht darin, dass das Projekt eines Dokuments auf kein anderes Projekt verweisen muss, um Prozeduren in diesem Projekt aufrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="43540-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="43540-143">VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine CALLTHIS-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird.</span><span class="sxs-lookup"><span data-stu-id="43540-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="43540-144">Wenn Sie das Dokument mit der Zelle, die die CALLTHIS-Funktion nutzt, schließen müssen, nutzen Sie eines der folgenden Verfahren:</span><span class="sxs-lookup"><span data-stu-id="43540-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="43540-145">Schließen Sie das Dokument mit Code, der kein VBA-Code ist.</span><span class="sxs-lookup"><span data-stu-id="43540-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="43540-146">Schließen Sie das Dokument von einem anderen Projekt aus als von jenen, das gerade geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="43540-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="43540-147">Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.</span><span class="sxs-lookup"><span data-stu-id="43540-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="43540-148">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="43540-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="43540-149">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43540-149">Example 1</span></span>

<span data-ttu-id="43540-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="43540-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="43540-151">Ruft die in einem Modul abgelegte Prozedur namens p auf und übergibt den Wert der Zelle Height in Zentimetern, beispielsweise 7,62.</span><span class="sxs-lookup"><span data-stu-id="43540-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="43540-152">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43540-152">Example 2</span></span>

<span data-ttu-id="43540-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="43540-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="43540-154">Ruft die in einem Modul abgelegte Prozedur q auf und übergibt die Höhe der Zelle in Zentimetern und die Breite in internen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="43540-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="43540-155">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="43540-155">Example 3</span></span>

<span data-ttu-id="43540-156">Verwenden Sie das folgende Verfahren im Klassenmodul *ThisDocument* .</span><span class="sxs-lookup"><span data-stu-id="43540-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="43540-157">Verwenden Sie mit den oben beschriebenen Prozeduren eines der folgenden Syntaxbeispiele in der Zelle EventDblClick eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="43540-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="43540-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="43540-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="43540-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="43540-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="43540-160">CALLTHIS("ThisDocument.C",,"Klicken Sie auf", "OK.")</span><span class="sxs-lookup"><span data-stu-id="43540-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

