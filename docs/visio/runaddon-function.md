---
title: RUNADDON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Führt ein Add-On oder ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt aus.
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432009"
---
# <a name="runaddon-function"></a><span data-ttu-id="2e8cf-103">RUNADDON Function</span><span class="sxs-lookup"><span data-stu-id="2e8cf-103">RUNADDON Function</span></span>

<span data-ttu-id="2e8cf-104">Führt ein Add-On oder ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2e8cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e8cf-105">Syntax</span></span>

<span data-ttu-id="2e8cf-106">RUNADDON(" *string*  ")</span><span class="sxs-lookup"><span data-stu-id="2e8cf-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e8cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e8cf-107">Parameters</span></span>

|<span data-ttu-id="2e8cf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e8cf-108">**Name**</span></span>|<span data-ttu-id="2e8cf-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2e8cf-109">**Required/Optional**</span></span>|<span data-ttu-id="2e8cf-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2e8cf-110">**Data Type**</span></span>|<span data-ttu-id="2e8cf-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e8cf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e8cf-112">_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2e8cf-112">_string_</span></span> <br/> |<span data-ttu-id="2e8cf-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2e8cf-113">Required</span></span>  <br/> |<span data-ttu-id="2e8cf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2e8cf-114">**String**</span></span> <br/> | <span data-ttu-id="2e8cf-115">Der Name eines Add-Ons in der **Addons**-Auflistung oder ein Makro in einem VBA-Projekt.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e8cf-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e8cf-116">Remarks</span></span>

<span data-ttu-id="2e8cf-117">Wenn das Projekt des Dokuments, das den RUNADDON-Funktionsaufruf enthält (oder ein anderes Projekt, auf das verwiesen wird), kein Makro (eine Prozedur ohne Argumente) mit der Zeichenfolge _hat,_ führt Microsoft Visio die benannte Add-On-Zeichenfolge _aus._</span><span class="sxs-lookup"><span data-stu-id="2e8cf-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="2e8cf-118">Wenn keine benannte  Add-On-Zeichenfolge gefunden werden kann, führt Visio nichts aus und meldet keinen Fehler.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="2e8cf-119">(Sie können mit der **TraceFlags**-Eigenschaft die Prozeduren und Add-Ons überwachen, die Visio versucht auszuführen.)</span><span class="sxs-lookup"><span data-stu-id="2e8cf-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="2e8cf-120">Wenn Sie eine Prozedur in einem Standardmodul aufrufen, wird empfohlen, der Zeichenfolge den Modulnamen voran zu geben, der die Prozedur enthält (z. B.  *moduleName.procName*), da mehrere Module eine Prozedur mit demselben Namen haben können.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="2e8cf-121">Verwenden Sie zum Aufrufen einer Prozedur in einem anderen Projekt als dem Projekt des Dokuments, das den RUNADDON-Funktionsaufruf enthält, die Syntax  *projName.modName.procName*  (Sie müssen in Ihrem #A0 explizit einen Verweis auf  *projName*  festgelegt haben).</span><span class="sxs-lookup"><span data-stu-id="2e8cf-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="2e8cf-p102">Ab Visio 2002 kann die RUNADDON-Funktion keine Zeichenfolgen mit beliebigem VBA-Code ausführen. Code, der früher an die RUNADDON-Funktion übergeben wurde, kann in eine Prozedur im VBA-Projekt eines Dokuments verschoben werden, das aus der RUNADDON-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="2e8cf-124">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="2e8cf-p103">In früheren Visio-Versionen wird diese Funktion in der Form _RUNADDON geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2e8cf-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e8cf-127">Example 1</span></span>

<span data-ttu-id="2e8cf-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="2e8cf-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="2e8cf-129">Startet ein Add-On namens Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2e8cf-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2e8cf-130">Example 2</span></span>

<span data-ttu-id="2e8cf-131">RUNADDON("Shapes anordnen")</span><span class="sxs-lookup"><span data-stu-id="2e8cf-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="2e8cf-132">Startet das (VSL-implementierte) Add-On Shapes anordnen.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2e8cf-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2e8cf-133">Example 3</span></span>

<span data-ttu-id="2e8cf-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="2e8cf-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="2e8cf-135">Ruft das Makro ReportStatistics im **ThisDocument-Modul** im Dokumentprojekt auf, das diesen Funktionsaufruf enthält.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="2e8cf-136">Zum Aufrufen eines Makros im Modul **ThisDocument** müssen Sie der Zeichenfolge wie dargestellt "ThisDocument" voranstellen.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="2e8cf-137">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2e8cf-137">Example 4</span></span>

<span data-ttu-id="2e8cf-138">RUNADDON(" *ModuleName*  . ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="2e8cf-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="2e8cf-139">Ruft das ReportStatistics-Makro in ModuleName im Dokumentprojekt  *auf,*  das diesen Funktionsaufruf enthält.</span><span class="sxs-lookup"><span data-stu-id="2e8cf-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

