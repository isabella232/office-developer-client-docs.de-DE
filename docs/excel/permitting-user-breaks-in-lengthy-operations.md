---
title: Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlAbort-Funktion [Excel 2007], Concurrent Tasks [Excel 2007], User Breaks [Excel 2007]
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
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="5806f-104">Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="5806f-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="5806f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5806f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5806f-106">Auch wenn Windows PreEmptive Multitasking verwendet, wobei die Ausführung ihrer Funktionen oder Befehle sehr viel Zeit in Anspruch nehmen kann, empfiehlt es sich, dem Betriebssystem jetzt und wieder Zeit zu geben, um gleichzeitige Aufgaben zu planen.</span><span class="sxs-lookup"><span data-stu-id="5806f-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="5806f-107">Mit systemeigenen Windows-aufrufen können Sie dies mithilfe der Sleep-Funktion tun.</span><span class="sxs-lookup"><span data-stu-id="5806f-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="5806f-108">Mithilfe der C-API können Sie dies mithilfe der XlAbort- [Funktion](xlabort.md)tun, die den Prozessor nicht nur für einen Augenblick liefert, sondern auch überprüft, ob der Benutzer die Cancel-Taste gedrückt hat, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="5806f-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="5806f-109">Die **xlAbort** -Funktion ermöglicht es Ihrem Code daher zu überprüfen, ob der Benutzer den Prozess beenden, die erforderliche Bereinigung ausführen und dann die Steuerung an Excel zurückgeben möchte.</span><span class="sxs-lookup"><span data-stu-id="5806f-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="5806f-110">Die Funktion ermöglicht auch das Löschen der Unterbrechungsbedingung.</span><span class="sxs-lookup"><span data-stu-id="5806f-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="5806f-111">Dadurch können Ihre Befehle ein Dialogfeld anzeigen, um zu überprüfen, ob der Benutzer den Befehl beenden möchte.</span><span class="sxs-lookup"><span data-stu-id="5806f-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="5806f-112">Wenn der Benutzer den Befehl nicht beenden möchte, wird durch Aufrufen der **xlAbort** -Funktion mit dem Argument *false* der Umbruch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5806f-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="5806f-113">(Das Standardargument ist *true* , das einfach die Bedingung überprüft, aber nicht gelöscht wird.)</span><span class="sxs-lookup"><span data-stu-id="5806f-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="5806f-114">Sie können die **xlAbort** -Funktion von einer benutzerdefinierten Funktion (UDF) oder von einem XLL-Befehl aus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5806f-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="5806f-115">Wenn die **xlAbort** -Funktion in einem UDF **true**zurückgibt und einen Benutzer Bruch erkannt hat, würden Sie in der Regel Short die Funktions Berechnung kürzen und einen Wert zurückgeben, um anzugeben, dass die Berechnung nicht abgeschlossen wurde, vielleichteine Fehlermeldung oder eine NULL.</span><span class="sxs-lookup"><span data-stu-id="5806f-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="5806f-116">Sie würden die Unterbrechungsbedingung nicht deaktivieren, sodass andere Instanzen von langwierigen Funktionen, die auch diese Bedingung überprüfen, ebenfalls unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="5806f-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="5806f-117">Excel löscht diese Bedingung implizit, wenn eine Neuberechnung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5806f-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="5806f-118">Wenn Sie eine Unterbrechungsbedingung in einem Befehl feststellen, löschen Sie in der Regel die Bedingung, indem Sie die **xlAbort** -Funktion erneut mit dem Argument **false**aufrufen, obwohl Excel diese Bedingung implizit löscht, wenn ein Befehl beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5806f-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5806f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5806f-119">See also</span></span>



[<span data-ttu-id="5806f-120">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="5806f-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="5806f-121">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="5806f-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="5806f-122">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="5806f-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="5806f-123">Zugreifen auf Excel-Instanz- und Hauptfensterhandles</span><span class="sxs-lookup"><span data-stu-id="5806f-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

