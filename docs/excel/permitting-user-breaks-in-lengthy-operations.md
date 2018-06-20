---
title: Genehmigungsverfahren Benutzer Zeilenumbrüche in langen Vorgänge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Bereichsgröße-Funktion [excel 2007], gleichzeitige Aufgaben [Excel 2007], Benutzer Breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790558"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="e79ac-104">Genehmigungsverfahren Benutzer Zeilenumbrüche in langen Vorgänge</span><span class="sxs-lookup"><span data-stu-id="e79ac-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="e79ac-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e79ac-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e79ac-106">Obwohl Windows unterbrechen Multitasking verwendet wird, in dem können Ihre Funktionen oder Befehle eine auszuführende Zeit, ist es empfehlenswert, einige Zeit für das Betriebssystem und wieder, die es planen gleichzeitige Aufgaben unterstützen ergeben.</span><span class="sxs-lookup"><span data-stu-id="e79ac-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="e79ac-107">Systemeigenen Windows-Anrufe verwenden, können Sie hierzu mithilfe der Funktion dem Standbymodus.</span><span class="sxs-lookup"><span data-stu-id="e79ac-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="e79ac-108">Der C-API verwenden, können Sie tun sie mithilfe der [Bereichsgröße-Funktion](xlabort.md), die nicht nur den Prozessor für eine Sofortnachrichtensitzung ergibt, sondern auch überprüft, ob der Benutzer die Cancel-Taste **ESC-Taste**gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="e79ac-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="e79ac-109">Die Funktion **Bereichsgröße** kann daher Code, um zu überprüfen, ob der Benutzer möchte, beenden Sie den Prozess, führen Sie die erforderliche Bereinigung, und klicken Sie dann die Steuerung an Excel zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e79ac-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="e79ac-110">Die Funktion können auch die Unterbrechung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e79ac-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="e79ac-111">Auf diese Weise können die Befehle zum Anzeigen eines Dialogfelds, um zu überprüfen, ob der Benutzer den Befehl beenden möchte.</span><span class="sxs-lookup"><span data-stu-id="e79ac-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="e79ac-112">Wenn der Benutzer nicht den Befehl beenden möchten, löscht die **Bereichsgröße** -Funktion mit dem Argument *FALSE* Aufrufen den Umbruch.</span><span class="sxs-lookup"><span data-stu-id="e79ac-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="e79ac-113">(Das Argument der Standardwert ist *TRUE* , die einfach überprüft die Bedingung jedoch nicht gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="e79ac-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="e79ac-114">Sie können die Funktion **Bereichsgröße** aus einer benutzerdefinierten Funktion (UDF) oder aus einem XLL-Befehl aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e79ac-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="e79ac-115">In einer UDF beenden die **Bereichsgröße** Funktion **TRUE**, dass eine Unterbrechung Benutzer erkannt können Sie in der Regel die Funktion Berechnung abgeschnitten und einige Wert, um anzugeben, dass die Berechnung nicht wurde abgeschlossen, möglicherweise ein Fehler oder 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e79ac-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="e79ac-116">Sie möchten nicht, die Unterbrechung, damit andere Instanzen des langen Funktionen, die diese Bedingung ferner Seitenumbruch auch deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e79ac-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="e79ac-117">Excel löscht implizit diese Bedingung, wenn eine neuberechnung endet.</span><span class="sxs-lookup"><span data-stu-id="e79ac-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="e79ac-118">Wenn Sie eine Unterbrechung in einem Befehl nicht erkennen, löschen Sie Sie in der Regel die Bedingung durch Aufrufen der **Bereichsgröße** Funktion erneut mit dem Argument **FALSE**, obwohl Excel diese Bedingung implizit gelöscht, wenn ein Befehl abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e79ac-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e79ac-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e79ac-119">See also</span></span>



[<span data-ttu-id="e79ac-120">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="e79ac-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="e79ac-121">Multithread-Neuberechnung in Excel</span><span class="sxs-lookup"><span data-stu-id="e79ac-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="e79ac-122">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="e79ac-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="e79ac-123">Zugriff auf Excel-Instanz und im Hauptfenster von Handles</span><span class="sxs-lookup"><span data-stu-id="e79ac-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

