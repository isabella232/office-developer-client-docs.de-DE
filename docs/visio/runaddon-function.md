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
description: Führt ein Add-on oder ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt aus.
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797966"
---
# <a name="runaddon-function"></a><span data-ttu-id="73e57-103">RUNADDON Function</span><span class="sxs-lookup"><span data-stu-id="73e57-103">RUNADDON Function</span></span>

<span data-ttu-id="73e57-104">Führt ein Add-on oder ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="73e57-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="73e57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73e57-105">Syntax</span></span>

<span data-ttu-id="73e57-106">RUNADDON (" *String* ")</span><span class="sxs-lookup"><span data-stu-id="73e57-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="73e57-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73e57-107">Parameters</span></span>

|<span data-ttu-id="73e57-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="73e57-108">**Name**</span></span>|<span data-ttu-id="73e57-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="73e57-109">**Required/Optional**</span></span>|<span data-ttu-id="73e57-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="73e57-110">**Data Type**</span></span>|<span data-ttu-id="73e57-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73e57-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="73e57-112">_string_</span><span class="sxs-lookup"><span data-stu-id="73e57-112">_string_</span></span> <br/> |<span data-ttu-id="73e57-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="73e57-113">Required</span></span>  <br/> |<span data-ttu-id="73e57-114">**String**</span><span class="sxs-lookup"><span data-stu-id="73e57-114">**String**</span></span> <br/> | <span data-ttu-id="73e57-115">Der Name eines Add-Ons in der **Addons**-Auflistung oder ein Makro in einem VBA-Projekt.</span><span class="sxs-lookup"><span data-stu-id="73e57-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73e57-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73e57-116">Remarks</span></span>

<span data-ttu-id="73e57-117">Wenn das Projekt des Dokuments, die den RUNADDON-Funktionsaufruf enthält (oder einem anderen Projekt, wenn darauf verwiesen wird) Makro (eine Prozedur ohne Argumente) namens _String_nicht vorhanden ist, wird in Microsoft Visio das Add-on _String_ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73e57-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="73e57-118">Wenn kein Add-on mit dem Namen _String_ gefunden werden kann, wird von Visio hat keine Auswirkung und kein Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="73e57-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="73e57-119">(Mit die **TraceFlags** -Eigenschaft können Sie die Prozeduren und Add-ons, die zum Ausführen von Visio versucht überwachen.)</span><span class="sxs-lookup"><span data-stu-id="73e57-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="73e57-120">Wenn Sie eine Prozedur in einem Standardmodul aufrufen, wird empfohlen, mit dem Modulnamen, der die Prozedur (beispielsweise *moduleName.procName*), enthält die Zeichenfolge als Präfix, da mehrere Module eine Prozedur mit dem gleichen Namen aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="73e57-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="73e57-121">Zum Aufrufen einer Prozedur in einem Projekt auf das Projekt des Dokuments, die den RUNADDON-Funktionsaufruf enthält verwenden die Syntax *projName.modName.procName* (Sie müssen im VBA-Projekt ausdrücklich einen Verweis auf *Projektname bezeichnete* festgelegt haben).</span><span class="sxs-lookup"><span data-stu-id="73e57-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="73e57-p102">Ab Visio 2002 kann die RUNADDON-Funktion keine Zeichenfolgen mit beliebigem VBA-Code ausführen. Code, der früher an die RUNADDON-Funktion übergeben wurde, kann in eine Prozedur im VBA-Projekt eines Dokuments verschoben werden, das aus der RUNADDON-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="73e57-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="73e57-124">Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz.</span><span class="sxs-lookup"><span data-stu-id="73e57-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="73e57-p103">In früheren Visio-Versionen wird diese Funktion in der Form _RUNADDON geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73e57-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="73e57-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73e57-127">Example 1</span></span>

<span data-ttu-id="73e57-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="73e57-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="73e57-129">Startet das Add-on Calendar.exe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73e57-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="73e57-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73e57-130">Example 2</span></span>

<span data-ttu-id="73e57-131">RUNADDON("Shapes anordnen")</span><span class="sxs-lookup"><span data-stu-id="73e57-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="73e57-132">Startet das (VSL-implementierte) Add-On Shapes anordnen.</span><span class="sxs-lookup"><span data-stu-id="73e57-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="73e57-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="73e57-133">Example 3</span></span>

<span data-ttu-id="73e57-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="73e57-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="73e57-135">Ruft das Makro ReportStatistics im Modul ThisDocument im Dokumentprojekt auf, das diesen Funktionsaufruf enthält.</span><span class="sxs-lookup"><span data-stu-id="73e57-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="73e57-136">Zum Aufrufen eines Makros im Modul **ThisDocument** müssen Sie der Zeichenfolge wie dargestellt "ThisDocument" voranstellen.</span><span class="sxs-lookup"><span data-stu-id="73e57-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="73e57-137">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="73e57-137">Example 4</span></span>

<span data-ttu-id="73e57-138">RUNADDON (" *ModuleName* . ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="73e57-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="73e57-139">Ruft das Makro ReportStatistics in *ModuleName* im Dokumentprojekt auf, das diesen Funktionsaufruf enthält.</span><span class="sxs-lookup"><span data-stu-id="73e57-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

