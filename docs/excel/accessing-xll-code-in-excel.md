---
title: Zugriff auf XLL-Code in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugriff auf Xll-Code [excel 2007], XLLs [Excel 2007], den Zugriff auf Code, Befehle [Excel 2007], Registrierung, Funktionen [Excel 2007], Registrierung, Aufrufen von XLLs in Excel, Befehle [Excel 2007] registrieren, registrieren Funktionen [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790391"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="8489b-104">Zugriff auf XLL-Code in Excel</span><span class="sxs-lookup"><span data-stu-id="8489b-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="8489b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8489b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8489b-106">In Microsoft Excel, Funktionen und Befehle, die eine XLL enthält verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="8489b-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="8489b-107">Muss von der XLL exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="8489b-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="8489b-108">Muss mit Excel registriert werden.</span><span class="sxs-lookup"><span data-stu-id="8489b-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="8489b-109">Registrieren von Funktionen und Befehle mit Excel</span><span class="sxs-lookup"><span data-stu-id="8489b-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="8489b-110">Registrierung teilt Excel die folgenden Informationen zu einer DLL-Einstiegspunkt:</span><span class="sxs-lookup"><span data-stu-id="8489b-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="8489b-111">Ob er ausgeblendet wurde oder wenn eine Funktion, wird es gibt an, ob in den Funktions-Assistenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8489b-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="8489b-112">Gibt an, ob es aufrufbare nur aus einer XLM-Makrovorlage oder aus einem Arbeitsblatt ist.</span><span class="sxs-lookup"><span data-stu-id="8489b-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="8489b-113">Wenn ein Befehl, ob ist es einer Tabellenfunktion oder einer gleichwertigen Blatt Makrofunktion.</span><span class="sxs-lookup"><span data-stu-id="8489b-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="8489b-114">Welchen XLL-DLL Exportnamen hat, und welche Namen Excel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8489b-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="8489b-115">Wenn es sich um eine Funktion ist:</span><span class="sxs-lookup"><span data-stu-id="8489b-115">If it is a function:</span></span>
    
  - <span data-ttu-id="8489b-116">Welche Daten gibt es gibt und als Argumente.</span><span class="sxs-lookup"><span data-stu-id="8489b-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="8489b-117">Gibt an, ob sie das Ergebnis zurückgegeben, indem ein Argument direkten ändern.</span><span class="sxs-lookup"><span data-stu-id="8489b-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="8489b-118">Gibt an, ob es veränderliche ist.</span><span class="sxs-lookup"><span data-stu-id="8489b-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="8489b-119">Gibt an, ob es threadsicheren (unterstützte beginnend in Excel 2007) ist.</span><span class="sxs-lookup"><span data-stu-id="8489b-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="8489b-120">Was Text einfügen Funktions-Assistenten und AutoVervollständigen-Editor angezeigt werden soll, das Ihnen bei Aufruf der Funktion.</span><span class="sxs-lookup"><span data-stu-id="8489b-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="8489b-121">Die Funktion Kategorie, die unter aufgelistet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8489b-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="8489b-122">Dies geschieht alle mit der C-API-Funktion [XlfRegister](xlfregister-form-1.md), entspricht die XLM-Funktion **zu registrieren**.</span><span class="sxs-lookup"><span data-stu-id="8489b-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="8489b-123">Aufrufen von XLL-Funktionen direkt in Excel</span><span class="sxs-lookup"><span data-stu-id="8489b-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="8489b-124">Nachdem sie registriert sind, können XLL Arbeitsblatt und Makro Blatt Funktionen unabhängig vom Standort aufgerufen werden, die, denen eine integrierte Funktion aus aufgerufen werden kann:</span><span class="sxs-lookup"><span data-stu-id="8489b-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="8489b-125">Eine einzelne Zelle oder ein Array der Formel in einem Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="8489b-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="8489b-126">Eine einzelne Zelle oder ein Array der Formel in einem Makroblatt.</span><span class="sxs-lookup"><span data-stu-id="8489b-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="8489b-127">Die Definition eines definierten Namens.</span><span class="sxs-lookup"><span data-stu-id="8489b-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="8489b-128">Die Bedingung und höhere Felder in einem Dialogfeld Bedingte Formatierung.</span><span class="sxs-lookup"><span data-stu-id="8489b-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="8489b-129">Aus einer anderen-add-in über die C-API-Funktion [XlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="8489b-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="8489b-130">In Visual Basic für Applikationen (VBA) über die **entsprechende** Methode.</span><span class="sxs-lookup"><span data-stu-id="8489b-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="8489b-131">Sie können einen Verweis auf die aufrufende Zelle oder eines Zellbereichs innerhalb Ihrer Funktion mit der C-API-Funktion **XlfCaller**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8489b-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="8489b-132">Wenn die Funktion die Zelle bedingtes Format Ausdruck aufgerufen wurde, werden Sie dennoch einen Verweis auf die zugeordnete Zelle oder Zellen, zurückgegeben, sodass Sie können nicht davon ausgehen, dass die Formel der Zelle XLL-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="8489b-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="8489b-133">Wenn Ihre Funktion aus einer VBA-benutzerdefinierte Funktion (UDF) aufgerufen wurde, gibt **XlfCaller** erneut die Adresse der Zellen, die die VBA-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8489b-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="8489b-134">Weitere Informationen finden Sie unter [XlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="8489b-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8489b-135">Excel ruft auch XLL-Funktionscode die Dialogfelder **Einfügen Funktions-Assistenten** , und **Ersetzen** .</span><span class="sxs-lookup"><span data-stu-id="8489b-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="8489b-136">Sie müssen möglicherweise Ihr Codes normal ausgeführt, in die Groß-/Kleinschreibung im Dialogfeld **Funktionsargumente einfügen** , insbesondere, in dem Ihre Funktion sehr lange führen Sie ergreifen kann, einschränken.</span><span class="sxs-lookup"><span data-stu-id="8489b-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="8489b-137">Zum Erkennen von einer der folgenden Dialogfelder Ihre Funktion aufgerufen wird, muss Implementierung Teil des Codes in Ihrem Projekt, die durchlaufen und alle geöffneten Fenster zu ermitteln, ob das Front-Fenster ist eines der folgenden Dialogfelder, und wenn Ja, welche.</span><span class="sxs-lookup"><span data-stu-id="8489b-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="8489b-138">Aufrufen von XLL-Befehle direkt in Excel</span><span class="sxs-lookup"><span data-stu-id="8489b-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="8489b-139">Nachdem sie registriert sind, können XLL-Befehle in allen Verfahren aufgerufen werden, dass andere benutzerdefinierte Makros aufgerufen werden können:</span><span class="sxs-lookup"><span data-stu-id="8489b-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="8489b-140">Durch ein Control-Objekt zugeordnet wird, die in einem Arbeitsblatt eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="8489b-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="8489b-141">Im Dialogfeld Makro ausführen.</span><span class="sxs-lookup"><span data-stu-id="8489b-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="8489b-142">In VBA-Makro verwenden Sie die **entsprechende** Methode.</span><span class="sxs-lookup"><span data-stu-id="8489b-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="8489b-143">Über ein benutzerdefiniertes Menüelement oder eine Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="8489b-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="8489b-144">Mithilfe einer Tastenkombination eingerichtet werden, wenn Sie den Befehl registriert.</span><span class="sxs-lookup"><span data-stu-id="8489b-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="8489b-145">Wie der Befehl ausgeführt werden soll, wenn ein bestimmtes Ereignis aufgefangen.</span><span class="sxs-lookup"><span data-stu-id="8489b-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8489b-146">XLL-Befehle werden ausgeblendet, dass sie nicht in der Liste der verfügbaren Makros in Excel-Dialogfelder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8489b-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="8489b-147">Jedoch manuell in das Feld Makro ein eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8489b-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="8489b-148">Excel erwartet, dass der Name registriert als in diesen Dialogfeldern nicht der Name der DLL-Datei exportieren.</span><span class="sxs-lookup"><span data-stu-id="8489b-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="8489b-149">Alle XLL-Befehle mit Excel registriert werden angenommen, dass von Excel im folgenden Format sein:</span><span class="sxs-lookup"><span data-stu-id="8489b-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="8489b-p104">Der Rückgabewert wird von Excel ignoriert, es sei denn, der Aufruf erfolgt aus einer XLM-Makrovorlage; in diesem Fall wird der Rückgabewert in **TRUE** oder **FALSE** konvertiert. Sie m�ssen daher 1 zur�ckgeben, wenn der Befehl erfolgreich ausgef�hrt wurde, und 0 bei einem Fehler oder Benutzerabbruch.</span><span class="sxs-lookup"><span data-stu-id="8489b-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="8489b-152">Erhalten Sie Informationen zu den gewünschten Befehl wie aufgerufen wurde mit der C-API-Funktion **XlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="8489b-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="8489b-153">Weitere Informationen finden Sie unter [XlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="8489b-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="8489b-154">Starten in Excel 2007-Benutzeroberfläche ist sehr unterschiedliche aus früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="8489b-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="8489b-155">In den meisten Fällen werden weiterhin die C-API-Funktionen, die das Hinzufügen und Löschen von benutzerdefinierten Menüleisten, Menüs, Untermenüs, Menüelemente, benutzerdefinierte Symbolleisten und Symbolleistenschaltflächen ermöglichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8489b-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="8489b-156">Jedoch können sie nicht immer das hinzugefügte Element in eine Möglichkeit zur Verfügung, denen Ihre Benutzer mit vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="8489b-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="8489b-157">Sie sollten sorgfältig überprüfen, dass zusätzliche Funktionen weiterhin verfügbar ist, oder implementieren eine versionsspezifischen Anpassung.</span><span class="sxs-lookup"><span data-stu-id="8489b-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="8489b-158">Starten von der Benutzeroberfläche in Excel 2007 ist am besten angepasst, mithilfe eines Moduls von verwaltetem Code, das dann eng mit Ihrer XLL-Befehle verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="8489b-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8489b-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8489b-159">See also</span></span>

- [<span data-ttu-id="8489b-160">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="8489b-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="8489b-161">Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen</span><span class="sxs-lookup"><span data-stu-id="8489b-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="8489b-162">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8489b-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="8489b-163">Entwickeln von Excel-XLLs</span><span class="sxs-lookup"><span data-stu-id="8489b-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



