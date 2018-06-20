---
title: Excel-Befehle,-Funktionen und-Zustände
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zustände [excel 2007], Befehle [Excel 2007], Arbeitsblattfunktionen [Excel 2007], Makroblatt Funktionen [Excel 2007], Excel Staaten
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790425"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="6d8a3-104">Excel-Befehle,-Funktionen und-Zustände</span><span class="sxs-lookup"><span data-stu-id="6d8a3-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="6d8a3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d8a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6d8a3-106">Microsoft Excel erkennt zwei sehr unterschiedliche Arten von Funktionalität: Befehle und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="6d8a3-107">Befehle</span><span class="sxs-lookup"><span data-stu-id="6d8a3-107">Commands</span></span>

<span data-ttu-id="6d8a3-108">In Excel weisen Befehle folgende Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="6d8a3-109">Sie führen Aktionen auf die gleiche Weise, die Benutzer ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="6d8a3-110">Sie können alles möglich, ein Benutzer (Betreff auf die Grenzwerte der Schnittstelle verwendet), wie Excel-Einstellungen ändern, öffnen, schließen und Bearbeiten von Dokumenten, initiieren neuberechnungen führen kann und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="6d8a3-111">Sie können eingerichtet werden, aufgerufen werden, wenn bestimmte behandelter Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="6d8a3-112">Sie können Dialogfelder anzeigen und interagieren mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="6d8a3-113">Sie können verknüpft werden, um Objekte zu steuern, sodass sie aufgerufen werden, wenn eine Aktion für dieses Objekt, wie Sie mit der linken Maustaste durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="6d8a3-114">Sie werden von Excel nie während einer neuberechnung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="6d8a3-115">Sie können nicht von Funktionen während einer neuberechnung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="6d8a3-116">Funktionen</span><span class="sxs-lookup"><span data-stu-id="6d8a3-116">Functions</span></span>

<span data-ttu-id="6d8a3-117">Funktionen in Excel wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="6d8a3-118">In der Regel Argumente, und geben immer ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="6d8a3-119">Sie können in eine oder mehrere Zellen als Teil einer Excel-Formel eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="6d8a3-120">Sie können in definierter Name Definitionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="6d8a3-121">Sie können in bedingten Formatierung Grenzwert und Schwellenwert Ausdrücken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="6d8a3-122">Sie können mithilfe der Befehle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="6d8a3-123">Sie können Befehle nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-123">They cannot call commands.</span></span>
    
<span data-ttu-id="6d8a3-124">Excel wird einen weiteren Unterschied zwischen benutzerdefinierten Arbeitsblattfunktionen und benutzerdefinierte Funktionen, mit denen Makrovorlagen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-124">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets.</span></span> <span data-ttu-id="6d8a3-125">Excel wird nicht eingeschränkt Makro benutzerdefinierte Funktionen nur für auf Makroblättern verwendet wird: Diese Funktionen können überall dort verwendet werden eine normalen Tabellenfunktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-125">Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="6d8a3-126">Arbeitsblattfunktionen</span><span class="sxs-lookup"><span data-stu-id="6d8a3-126">Worksheet Functions</span></span>

<span data-ttu-id="6d8a3-127">Das folgende gilt für Excel-Arbeitsblattfunktionen:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="6d8a3-128">Sie können nicht Makro Blatt Informationsfunktionen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="6d8a3-129">Sie können nicht der Werte von Zellen gekennzeichnete erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="6d8a3-130">Diese werden geschrieben und als threadsicheren ab Excel 2007 registriert.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="6d8a3-131">Makrovorlage Funktionen</span><span class="sxs-lookup"><span data-stu-id="6d8a3-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="6d8a3-132">Das folgende gilt der Excel-Makrovorlage Funktionen:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="6d8a3-133">Sie können Funktionen Makro Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="6d8a3-134">Sie können die Werte der gekennzeichnete Zellen, einschließlich der Werte der aufrufenden Zellen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="6d8a3-135">Sie sind nicht Thread sicherer ab Excel 2007 betrachtet.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="6d8a3-136">Wie Excel eine benutzerdefinierte Funktion (UDF) behandelt, was die Funktion genehmigt und wie diese neu berechnet die Funktion sind alle bestimmt wird, wenn Sie die Funktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="6d8a3-137">Wenn eine Funktion als einer Tabellenfunktion registriert ist er versucht, etwas, das nur eine Makrovorlage Funktion möglich ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="6d8a3-138">Ab Excel 2007, wenn eine Tabellenfunktion als threadsicheren registriert versucht, eine Makro Blatt-Funktion aufgerufen, fällt erneut, der Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="6d8a3-139">Excel behandelt Microsoft Visual Basic für Applikationen (VBA) UDFs wie Makro Blatt Entsprechung-Funktionen, um die Arbeitsbereichsinformationen und der Wert der gekennzeichnete Zellen zugreifen können, und sie gelten nicht als wie thread sicherer ab Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="6d8a3-140">Excel-Status</span><span class="sxs-lookup"><span data-stu-id="6d8a3-140">Excel States</span></span>

<span data-ttu-id="6d8a3-141">Excel kann zu einem bestimmten Zeitpunkt gemäß den Aktionen des Benutzers, einen externen Prozess, ein abgefangener Ereignis Ausführen eines Makros oder einer Excel Wartungsaufgaben terminierte wie **Automatisches Speichern**in einer Reihe von Staaten sein.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="6d8a3-142">Die Zustände, die das Benutzererlebnis lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="6d8a3-143">**Status bereit:** Keine Befehle oder Makros werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-143">**Ready state:** No commands or macros are being run.</span></span> <span data-ttu-id="6d8a3-144">Es werden keine Dialogfelder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-144">No dialog boxes are being displayed.</span></span> <span data-ttu-id="6d8a3-145">Keine Zellen bearbeitet werden, und der Benutzer ist nicht in der Mitte eines Vorgangs Ausschneiden/Kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-145">No cells are being edited and the user is not in the middle of a cut/copy and paste operation.</span></span> <span data-ttu-id="6d8a3-146">Kein eingebettetes Objekt besitzt den Fokus.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-146">No embedded object has focus.</span></span> 
    
- <span data-ttu-id="6d8a3-147">**Bearbeitungsmodus:** Der Benutzer gestartet wurde, in eine Zelle ungeschützt sind oder keine gültige Eingabezeichen eingeben oder auf eine oder mehrere ungeschützt sind oder keine Zellen **F2** gedrückt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="6d8a3-148">**Modus Ausschneiden/Kopieren und einfügen:** Der Benutzer ausgeschnitten oder kopiert eine Zelle oder eines Zellbereichs hat und sie nicht noch eingefügt wurde, oder sie über das Dialogfeld Inhalte einfügen, wodurch mehrere Einfügevorgänge eingefügt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="6d8a3-149">**Punktmodus:** Der Benutzer wird eine Formel zu bearbeiten, und ist Markieren von Zellen, die die Formel bearbeitet, deren Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="6d8a3-150">Der Benutzer kann die bearbeiten, Point und Ausschneiden/Kopieren Modi deaktivieren, durch Drücken von **ESC** -Taste, die in den Zustand bereit Excel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-150">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state.</span></span> <span data-ttu-id="6d8a3-151">Andere Ereignisse können die Zustände, wie die folgenden deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6d8a3-151">Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="6d8a3-152">Der Benutzer öffnet ein integriertes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="6d8a3-153">Der Benutzer versucht, eine neuberechnung.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="6d8a3-154">Der Benutzer führt einen Befehl.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-154">The user runs a command.</span></span>
    
- <span data-ttu-id="6d8a3-155">Excel führt eine **Automatische Speicherung** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="6d8a3-156">Es wird ein Timer-Ereignis aufgefangen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="6d8a3-157">Das letzte Beispiel ist von Bedeutung für Add-In-Entwickler.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="6d8a3-158">Sie sollten die Auswirkung der normalen Anwendungsfunktionen für Excel, in dem häufig verwendete Timer-Ereignis Trapping ausgeführt wird, sind wird festlegen und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="6d8a3-159">Wenn dies einen wichtigen Bestandteil von Add-in Funktionalität ist, sollten Sie Benutzer mit Weise leicht zugänglich anhalten, sodass sie können Ausschneiden/Kopieren und Einfügen normalerweise bei Bedarf bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6d8a3-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d8a3-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d8a3-160">See also</span></span>



[<span data-ttu-id="6d8a3-161">Excel-Programmierkonzepte</span><span class="sxs-lookup"><span data-stu-id="6d8a3-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="6d8a3-162">Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge</span><span class="sxs-lookup"><span data-stu-id="6d8a3-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

