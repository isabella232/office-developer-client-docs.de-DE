---
title: Befehle, Funktionen und Status in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zustände [Excel 2007],Befehle [Excel 2007],Arbeitsblattfunktionen[Excel 2007],Makrovorlagenfunktionen [Excel 2007],Excel-Zustände
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310969"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="7e161-104">Excel-Befehle, -Funktionen und -Zustände</span><span class="sxs-lookup"><span data-stu-id="7e161-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="7e161-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e161-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e161-106">Microsoft Excel erkennt zwei sehr verschiedene Arten zusätzlicher Funktionalität: Befehle und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7e161-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="7e161-107">Befehle</span><span class="sxs-lookup"><span data-stu-id="7e161-107">Commands</span></span>

<span data-ttu-id="7e161-108">In Excel haben Befehle die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7e161-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="7e161-109">Sie führen Aktionen auf dieselbe Weise durch wie Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7e161-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="7e161-110">Sie können alles tun, was ein Benutzer tun kann (innerhalb der Grenzen der verwendeten Benutzeroberfläche), z. B. Excel-Einstellungen ändern, Dokumente öffnen, schließen und bearbeiten, Neuberechnungen initiieren usw.</span><span class="sxs-lookup"><span data-stu-id="7e161-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="7e161-111">Sie können so eingerichtet werden, dass sie aufgerufen werden, wenn bestimmte eingeschlossene Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="7e161-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="7e161-112">Sie können Dialogfelder anzeigen und mit dem Benutzer interagieren.</span><span class="sxs-lookup"><span data-stu-id="7e161-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="7e161-113">Sie können verknüpft werden, um Objekte zu steuern, sodass sie aufgerufen werden, wenn eine Aktion für das jeweilige Objekt durchgeführt wird, z. B. mit der linken Maustaste klicken.</span><span class="sxs-lookup"><span data-stu-id="7e161-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="7e161-114">Sie werden von Excel niemals während einer Neuberechnung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7e161-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="7e161-115">Sie können während einer Neuberechnung nicht von Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="7e161-116">Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e161-116">Functions</span></span>

<span data-ttu-id="7e161-117">Funktionen bewirken in Excel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7e161-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="7e161-118">Sie nehmen in der Regel Argumente an und geben immer ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="7e161-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="7e161-119">Sie können als Teil einer Excel-Formel in eine oder mehrere Zellen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="7e161-120">Sie können in definierten Namensdefinitionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="7e161-121">Sie können in Grenzwert- und Schwellenwertausdrücken für die bedingte Formatierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="7e161-122">Sie können von Befehlen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="7e161-123">Sie können keine Befehle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e161-123">They cannot call commands.</span></span>
    
<span data-ttu-id="7e161-p101">Excel macht einen weiteren Unterschied zwischen benutzerdefinierten Tabellenfunktionen und benutzerdefinierten Funktionen, die auf Makrovorlagen ausgelegt sind. Excel schränkt benutzerdefinierte Makrovorlagenfunktionen nicht auf die reine Verwendung in Makrovorlagen ein: Diese Funktionen können überall dort verwendet werden, wo eine normale Tabellenfunktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e161-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="7e161-126">Tabellenfunktionen</span><span class="sxs-lookup"><span data-stu-id="7e161-126">Worksheet Functions</span></span>

<span data-ttu-id="7e161-127">Folgendes gilt für Excel-Arbeitsblattfunktionen:</span><span class="sxs-lookup"><span data-stu-id="7e161-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="7e161-128">Sie können nicht auf Makrovorlagen-Informationsfunktionen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7e161-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="7e161-129">Sie können nicht die Werte für nicht berechnete Zellen erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e161-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="7e161-130">Sie können ab Excel 2007 als threadsicher geschrieben und registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="7e161-131">Makrovorlagenfunktionen</span><span class="sxs-lookup"><span data-stu-id="7e161-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="7e161-132">Folgendes gilt für Excel-Makrovorlagenfunktionen:</span><span class="sxs-lookup"><span data-stu-id="7e161-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="7e161-133">Sie können auf Makrovorlagen-Informationsfunktionen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7e161-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="7e161-134">Sie können die Werte nicht berechneter Zellen erhalten, einschließlich der Werte der aufrufenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="7e161-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="7e161-135">Sie werden ab Excel 2007 nicht als threadsicher eingestuft.</span><span class="sxs-lookup"><span data-stu-id="7e161-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="7e161-136">Wie Excel eine benutzerdefinierte Funktion behandelt, was die Funktion zulässt und wie die Funktion neu berechnet wird, wird festgelegt, wenn Sie die Funktion registrieren.</span><span class="sxs-lookup"><span data-stu-id="7e161-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="7e161-137">Wenn eine Funktion als eine Tabellenfunktion registriert ist, jedoch versucht, etwas zu tun, das nur eine Makrovorlagenfunktion durchführen kann, tritt bei dem Vorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7e161-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="7e161-138">Ab Excel 2007 wird ein Vorgang ebenfalls nicht ausgeführt, wenn eine als threadsicher registrierte Arbeitsblattfunktion versucht, eine Makrovorlagenfunktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e161-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="7e161-139">Excel behandelt Microsoft Visual Basic for Applications (VBA) UDFs insofern als makrovorlagenäquivalente Funktionen, als sie auf Arbeitsbereichinformationen und den Wert nicht berechneter Zellen zugreifen können. Zudem gelten sie ab Excel 2007 nicht als threadsicher.</span><span class="sxs-lookup"><span data-stu-id="7e161-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="7e161-140">Excel-Zustände</span><span class="sxs-lookup"><span data-stu-id="7e161-140">Excel States</span></span>

<span data-ttu-id="7e161-141">Excel kann sich zu einem bestimmten Zeitpunkt in unterschiedlichen Zuständen befinden, abhängig von den Aktionen des Benutzers, einem externen Prozess, einem abgefangenen Ereignis beim Ausführen eines Makros oder einem zeitlich festgelegten Excel-Housekeepingereignis, z. B. **AutoSpeichern**.</span><span class="sxs-lookup"><span data-stu-id="7e161-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="7e161-142">Der Benutzer wird auf die folgenden Status treffen:</span><span class="sxs-lookup"><span data-stu-id="7e161-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="7e161-p103">**Status „Bereit“:** Es werden keine Befehle oder Makros ausgeführt. Es werden keine Dialogfelder angezeigt. Es werden keine Zellen bearbeitet, und der Benutzer ist nicht mitten in einem Vorgang zum Ausschneiden/Kopieren und Einfügen. Kein eingebettetes Objekt besitzt den Fokus.</span><span class="sxs-lookup"><span data-stu-id="7e161-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="7e161-147">**Bearbeitungsmodus:** Der Benutzer hat begonnen, gültige Eingabezeichen in eine nicht gesperrte oder geschützte Zelle einzugeben, oder hat **F2** in einer oder mehreren nicht gesperrten oder geschützten Zellen gedrückt.</span><span class="sxs-lookup"><span data-stu-id="7e161-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="7e161-148">**Auschneiden/Kopieren-und-Einfügen-Modus:** Der Benutzer hat eine Zelle oder einen Zellenbereich ausgeschnitten oder kopiert und noch nicht eingefügt, oder er hat sie über das Dialogfeld „Inhalte einfügen“ eingefügt, das mehrere Einfügevorgänge ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7e161-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="7e161-149">**Punktmodus:** Der Benutzer bearbeitet eine Formel und wählt Zellen aus, deren Adressen der bearbeiteten Formel hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="7e161-p104">Der Benutzer kann die Bearbeitungs-, Punkt- und Ausschneiden/Kopieren-Modi löschen, indem der die **ESC**-Taste drückt, wodurch Excel in den Status „Bereit“ zurückkehrt. Auch andere Ereignisse wie die folgenden können diese Status löschen:</span><span class="sxs-lookup"><span data-stu-id="7e161-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="7e161-152">Der Benutzer öffnet ein integriertes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7e161-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="7e161-153">Der Benutzer initiiert eine Neuberechnung.</span><span class="sxs-lookup"><span data-stu-id="7e161-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="7e161-154">Der Benutzer führt einen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="7e161-154">The user runs a command.</span></span>
    
- <span data-ttu-id="7e161-155">Excel führt einen **AutoSpeichern**-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="7e161-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="7e161-156">Ein Zeitgeberereignis wird eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7e161-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="7e161-157">Das letzte Beispiel ist für Add-In-Entwickler von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="7e161-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="7e161-158">Sie sollten die Auswirkungen der normalen Verwendbarkeit von Excel berücksichtigen, bei der häufige Zeitgeberereignistraps festgelegt und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7e161-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="7e161-159">Wenn dies ein wichtiger Bestandteil der Funktionalität Ihres Add-Ins ist, sollten Sie Benutzern eine leicht zugängliche Möglichkeit bieten, sie anzuhalten, damit sie bei Bedarf normale Ausschneiden/Kopieren-und-Einfügen-Vorgänge ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7e161-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e161-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e161-160">See also</span></span>



[<span data-ttu-id="7e161-161">Konzepte der Excel-Programmierung</span><span class="sxs-lookup"><span data-stu-id="7e161-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="7e161-162">Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="7e161-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

