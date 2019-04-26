---
title: Zugreifen auf XLL-Code in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf XLL-Code [Excel 2007],XLLs [Excel 2007], Zugreifen auf Code, Befehle [Excel 2007], Registrierung, Funktionen [Excel 2007], Registrierung, Aufrufen von XLLs aus Excel, Registrieren von Befehlen [Excel 2007], Registrieren von Funktionen [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304186"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="37b73-104">Zugreifen auf XLL-Code in Excel</span><span class="sxs-lookup"><span data-stu-id="37b73-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="37b73-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37b73-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="37b73-106">Um in Microsoft Excel zur Verfügung zu stehen, müssen die Funktionen und Befehle, die eine XLL enthält:</span><span class="sxs-lookup"><span data-stu-id="37b73-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="37b73-107">von der XLL exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="37b73-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="37b73-108">bei Excel registriert werden.</span><span class="sxs-lookup"><span data-stu-id="37b73-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="37b73-109">Registrieren von Funktionen und Befehlen bei Excel</span><span class="sxs-lookup"><span data-stu-id="37b73-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="37b73-110">Die Registrierung informiert Excel über Folgendes hinsichtlich eines DLL-Einstiegspunkts:</span><span class="sxs-lookup"><span data-stu-id="37b73-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="37b73-111">Ob er ausgeblendet oder, wenn es sich um eine Funktion handelt, ob er im Funktionsassistenten sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="37b73-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="37b73-112">Ob er nur aus einer XLM-Makrovorlage oder auch aus einem Arbeitsblatt aufrufbar ist.</span><span class="sxs-lookup"><span data-stu-id="37b73-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="37b73-113">Wenn es sich um einen Befehl handelt, ob er eine Arbeitsblattfunktion oder eine äquivalente Makrovorlagenfunktion ist.</span><span class="sxs-lookup"><span data-stu-id="37b73-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="37b73-114">Wie der XLL/DLL-Exportname lautet und welchen Namen Excel verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="37b73-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="37b73-115">Wenn es sich um eine Funktion handelt:</span><span class="sxs-lookup"><span data-stu-id="37b73-115">If it is: a.</span></span>
    
  - <span data-ttu-id="37b73-116">Welche Datentypen er als Argumente zurückgibt und erhält.</span><span class="sxs-lookup"><span data-stu-id="37b73-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="37b73-117">Ob er sein Ergebnis zurückgibt, indem er ein vorhandenes Argument ändert.</span><span class="sxs-lookup"><span data-stu-id="37b73-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="37b73-118">Ob er veränderbar ist.</span><span class="sxs-lookup"><span data-stu-id="37b73-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="37b73-119">Ob er Thread-sicher ist (unterstützt ab Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="37b73-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="37b73-120">Welchen Text der Assistent zum Einfügen von Funktionen und der AutoVervollständigen-Editor anzeigen sollen, um beim Funktionsabruf zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37b73-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="37b73-121">Unter welcher Funktionskategorie er aufgelistet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b73-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="37b73-122">Dies wird alles mit der C-API-Funktion [xlfRegister](xlfregister-form-1.md) erreicht, die der XLM-Funktion **REGISTER** entspricht.</span><span class="sxs-lookup"><span data-stu-id="37b73-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="37b73-123">Aufrufen von XLL-Funktionen direkt aus Excel</span><span class="sxs-lookup"><span data-stu-id="37b73-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="37b73-124">Sobald sie registriert sind, können die Funktionen von XLL-Arbeitsblatt und Makrovorlage dort aufgerufen werden, wo eine integrierte Funktion aufgerufen werden kann:</span><span class="sxs-lookup"><span data-stu-id="37b73-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="37b73-125">Einzelzellen- oder Array-Formel in einem Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="37b73-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="37b73-126">Einzelzellen- oder Array-Formel in einer Makrovorlage.</span><span class="sxs-lookup"><span data-stu-id="37b73-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="37b73-127">Definition eines definierten Namens.</span><span class="sxs-lookup"><span data-stu-id="37b73-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="37b73-128">Bedingungs- und Grenzwertfelder in einem Bedingungsformat-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="37b73-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="37b73-129">Anderes Add-In über die C-API-Funktion [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="37b73-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="37b73-130">Aus Visual Basic for Applications (VBA) über die **Application.Run**-Methode.</span><span class="sxs-lookup"><span data-stu-id="37b73-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="37b73-131">Sie erhalten eine Referenz zur aufrufenden Zelle oder zum aufrufenden Zellenbereich in der Funktion mit der C-API-Funktion **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="37b73-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="37b73-132">Wenn die Funktion aus dem Bedingungsformatausdruck der Zelle aufgerufen wurde, erhalten Sie weiterhin eine Referenz zu den verknüpften Zellen. Das heißt, Sie können nicht davon ausgehen, dass die Zellenformel die XLL-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="37b73-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="37b73-133">Wenn Ihre Funktion aus einer benutzerdefinierten VBA-Funktion (UDF) aufgerufen wurde, gibt **xlfCaller** erneut die Adresse der Zellen zurück, die die VBA-Funktion aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="37b73-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="37b73-134">Weitere Informationen finden Sie unter [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="37b73-134">For more information, see:[](xlfcaller.md)</span></span>
  
> [!NOTE]
> <span data-ttu-id="37b73-135">Excel ruft auch XLL-Funktionscode aus den Dialogfelder **Funktionsassistent einfügen** und **Ersetzen** auf.</span><span class="sxs-lookup"><span data-stu-id="37b73-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="37b73-136">Sie müssen evtl. die normale Ausführung Ihres Codes im Dialogfeld **Funktionsargumente einfügen** einschränken, insbesondere wenn Ihre Funktion nur langsam ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b73-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="37b73-137">Um zu erkennen, ob Ihre Funktion aus einem dieser Dialogfelder aufgerufen wird, müssen Sie Code in Ihrem Projekt implementieren, der durch alle geöffneten Fenster iteriert, um zu ermitteln, ob das Fenster im Vordergrund eines dieser Dialogfelder ist, und, wenn ja, welches.</span><span class="sxs-lookup"><span data-stu-id="37b73-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="37b73-138">Direktes Aufrufen von XLL-Befehlen aus Excel</span><span class="sxs-lookup"><span data-stu-id="37b73-138">Calling DLL commands directly from Excel</span></span>

<span data-ttu-id="37b73-139">Sobald sie registriert sind, können XLL-Befehle so wie andere benutzerdefinierte Makros aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="37b73-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="37b73-140">Durch Zuordnung zu einem Steuerungsobjekt in einem Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="37b73-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="37b73-141">Im Dialogfeld „Makro ausführen“.</span><span class="sxs-lookup"><span data-stu-id="37b73-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="37b73-142">Aus einem benutzerdefinierten VBA-Makro mit der **Application.Run**-Methode.</span><span class="sxs-lookup"><span data-stu-id="37b73-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="37b73-143">Aus einem angepassten Menüelement oder einer angepassten Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="37b73-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="37b73-144">Mithilfe einer Tastenkombination, die beim Registrieren des Befehls eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="37b73-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="37b73-145">Als Befehl, der beim Abfangen eines bestimmten Ereignisses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b73-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="37b73-146">XLL-Befehle sind ausgeblendet. Sie werden nicht in der Liste der verfügbaren Makros in Excel-Dialogfeldern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37b73-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="37b73-147">Aber sie können manuell in das Feld „Makroname“ eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37b73-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="37b73-148">Excel erwartet den Registriert als-Namen in diesen Dialogfeldern, nicht den DLL-Exportnamen.</span><span class="sxs-lookup"><span data-stu-id="37b73-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="37b73-149">Für alle bei Excel registrierten XLL-Befehle wird von Excel die folgende Form vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="37b73-149">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="37b73-p104">Der Rückgabewert wird von Excel ignoriert, es sei denn, der Aufruf erfolgt aus einer XLM-Makrovorlage; in diesem Fall wird der Rückgabewert in **TRUE** oder **FALSE** konvertiert. Sie müssen daher 1 zurückgeben, wenn der Befehl erfolgreich ausgeführt wurde, und 0 bei einem Fehler oder Benutzerabbruch.</span><span class="sxs-lookup"><span data-stu-id="37b73-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="37b73-152">Sie erhalten mit der C-API-Funktion **xlfCaller** Informationen darüber, wie Ihr Befehl abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="37b73-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="37b73-153">Weitere Informationen finden Sie unter [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="37b73-153">For more information, see:[](xlfcaller.md)</span></span>
  
<span data-ttu-id="37b73-154">Ab Excel 2007 unterscheidet sich die Benutzeroberfläche deutlich von früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="37b73-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="37b73-155">Die C-API-Funktionen, die das Hinzufügen und Löschen von benutzerdefinierten Menüleisten, Menüs, Untermenüs, Menüelementen, benutzerdefinierten Symbolleisten und Symbolleistenschaltflächen zulassen, werden weiterhin in den meisten Fällen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37b73-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="37b73-156">Jedoch stellen sie evtl. nicht immer das hinzugefügte Element in einer Weise bereit, die Benutzern vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="37b73-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="37b73-157">Sie sollten sorgfältig prüfen, dass jegliche hinzugefügte Funktionalität weiterhin zugänglich ist, oder eine versionsspezifische Anpassung implementieren.</span><span class="sxs-lookup"><span data-stu-id="37b73-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="37b73-158">Beim Starten in Excel 2007 wird die Benutzeroberfläche am besten über ein verwaltetes Codemodul angepasst, das eng mit Ihren XLL-Befehlen gekoppelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37b73-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37b73-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37b73-159">See also</span></span>

- [<span data-ttu-id="37b73-160">Erstellen von XLLs</span><span class="sxs-lookup"><span data-stu-id="37b73-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="37b73-161">Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern</span><span class="sxs-lookup"><span data-stu-id="37b73-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="37b73-162">Add-In-Manager und XLL-Schnittstellenfunktionen</span><span class="sxs-lookup"><span data-stu-id="37b73-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="37b73-163">Entwickeln von XLLs für Excel</span><span class="sxs-lookup"><span data-stu-id="37b73-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



