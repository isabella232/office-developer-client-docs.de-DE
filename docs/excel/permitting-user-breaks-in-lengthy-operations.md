---
title: Zulässige Benutzerumbrüche in langwierigen Vorgängen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort-Funktion [excel 2007],gleichzeitige Aufgaben [Excel 2007],Benutzerumbrüche [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414690"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="80462-104">Zulässige Benutzerumbrüche in langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="80462-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="80462-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="80462-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="80462-106">Auch wenn Windows präemptives Multitasking verwendet, bei dem die Ausführung Ihrer Funktionen oder Befehle sehr lange dauern kann, sollten Sie dem Betriebssystem immer wieder Zeit geben, um gleichzeitige Aufgaben zu planen.</span><span class="sxs-lookup"><span data-stu-id="80462-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="80462-107">Mithilfe von systemeigenen Windows können Sie dies mithilfe der Sleep-Funktion tun.</span><span class="sxs-lookup"><span data-stu-id="80462-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="80462-108">Mithilfe der C-API können Sie dies mithilfe der [xlAbort-Funktion](xlabort.md)tun, die nicht nur den Prozessor für einen Moment ergibt, sondern auch überprüft, ob der Benutzer die Abbruchtaste ESC gedrückt **hat.**</span><span class="sxs-lookup"><span data-stu-id="80462-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="80462-109">Mit **der xlAbort-Funktion** kann Ihr Code daher überprüfen, ob der Benutzer den Prozess beenden, die erforderlichen Bereinigungen tun und dann die Steuerung an Excel.</span><span class="sxs-lookup"><span data-stu-id="80462-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="80462-110">Mit der Funktion können Sie auch die Unterbrechungsbedingung löschen.</span><span class="sxs-lookup"><span data-stu-id="80462-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="80462-111">Auf diese Weise können Die Befehle ein Dialogfeld anzeigen, um zu überprüfen, ob der Benutzer den Befehl beenden möchte.</span><span class="sxs-lookup"><span data-stu-id="80462-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="80462-112">Wenn der Benutzer den Befehl nicht beenden möchte, wird die Unterbrechung durch Aufrufen der **xlAbort-Funktion** mit dem Argument  *FALSE*  beendet.</span><span class="sxs-lookup"><span data-stu-id="80462-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="80462-113">(Das Standardargument ist  *TRUE*  , das die Bedingung einfach überprüft, aber nicht deaktiviert.)</span><span class="sxs-lookup"><span data-stu-id="80462-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="80462-114">Sie können die **xlAbort-Funktion** über eine benutzerdefinierte Funktion (USERF) oder über einen XLL-Befehl aufrufen.</span><span class="sxs-lookup"><span data-stu-id="80462-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="80462-115">Wenn die **xlAbort-Funktion** in einem UDF **TRUE** zurückgibt, nachdem Sie eine Benutzerumbruch erkannt haben, würden Sie in der Regel die Funktionsberechnung kürzen und einen Wert zurückgeben, der angibt, dass die Berechnung nicht abgeschlossen wurde, z. B. einen Fehler oder null.</span><span class="sxs-lookup"><span data-stu-id="80462-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="80462-116">Sie würden die Unterbrechungsbedingung nicht löschen, sodass auch andere Instanzen langwieriger Funktionen, die diese Bedingung überprüfen, nicht mehr funktionierten.</span><span class="sxs-lookup"><span data-stu-id="80462-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="80462-117">Excel diese Bedingung implizit ab, wenn eine Neuberechnung endet.</span><span class="sxs-lookup"><span data-stu-id="80462-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="80462-118">Wenn Sie eine Unterbrechungsbedingung in einem Befehl erkennen, löschen Sie die Bedingung in der Regel, indem Sie die **xlAbort-Funktion** erneut mit dem Argument **FALSE** aufrufen, obwohl Excel diese Bedingung implizit beendet, wenn ein Befehl endet.</span><span class="sxs-lookup"><span data-stu-id="80462-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80462-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80462-119">See also</span></span>



[<span data-ttu-id="80462-120">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="80462-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="80462-121">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="80462-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="80462-122">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="80462-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="80462-123">Zugreifen auf Excel-Instanz- und Hauptfensterhandles</span><span class="sxs-lookup"><span data-stu-id="80462-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

