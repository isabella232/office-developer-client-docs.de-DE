---
title: ClearMacroError-Makroaktion
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721633"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="1cb23-102">ClearMacroError-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="1cb23-102">ClearMacroError macro action</span></span>


<span data-ttu-id="1cb23-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cb23-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1cb23-104">Die **ClearMacroError** -Aktion können Sie um Informationen zu einem Fehler zu löschen, die im **MacroError** -Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1cb23-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="1cb23-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1cb23-105">Setting</span></span>

<span data-ttu-id="1cb23-106">Die **ClearMacroError** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="1cb23-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cb23-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1cb23-107">Remarks</span></span>

- <span data-ttu-id="1cb23-p101">Tritt ein Fehler in einem Makro, werden Informationen zu dem Fehler im **MacroError** -Objekt gespeichert. Wenn Sie Fehlermeldungen unterdrückt nicht die **[BeiFehler](onerror-macro-action.md)** -Aktion verwendet haben, wird das Makro beendet und die Fehlerinformationen in eine Standardfehlermeldung angezeigt. Wenn Sie Fehlermeldungen unterdrückt die **BeiFehler** -Aktion verwendet haben, sollten Sie die im **MacroError** -Objekt in einer Bedingung oder in einer benutzerdefinierten Fehlermeldung gespeicherte Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cb23-p101">When an error occurs in a macro, information about the error is stored in the **MacroError** object. If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message. However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
  <span data-ttu-id="1cb23-p102">Nachdem ein Fehler behandelt wurde, ist die Informationen im **MacroError** -Objekt nicht mehr aktuell, daher es ratsam ist, deaktivieren Sie das Objekt mit der Aktion **ClearMacroError**. Dies setzt die Fehlernummer im **MacroError** -Objekt auf 0 und löscht alle anderen Informationen zu dem Fehler, der in das Objekt, wie die Beschreibung des Fehlers, Makroname, Name der Aktion, Bedingung und Argumente gespeichert ist. Auf diese Weise können Sie **MacroError** -Objekt einem späteren Zeitpunkt erneut überprüfen, um festzustellen, ob ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1cb23-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

- <span data-ttu-id="1cb23-114">**MacroError** -Objekt wird automatisch gelöscht, wenn alle Makro beendet wird, daher Sie keine verwenden Sie die Aktion **ClearMacroError** am Ende eines Makros müssen.</span><span class="sxs-lookup"><span data-stu-id="1cb23-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

- <span data-ttu-id="1cb23-p103">**MacroError** -Objekt enthält Informationen zu nur einem Fehler zu einem Zeitpunkt. Wenn mehr als einen Fehler in einem Makro aufgetreten ist, enthält das **MacroError** -Objekt nur Informationen zu den letzten Fehler.</span><span class="sxs-lookup"><span data-stu-id="1cb23-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

- <span data-ttu-id="1cb23-117">Um die **ClearMacroError** -Aktion in einem VBA-Modul auszuführen, verwenden Sie die **ClearMacroError** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1cb23-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="1cb23-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1cb23-118">Example</span></span>

<span data-ttu-id="1cb23-119">Das folgende Makro verwendet die **BeiFehler** -Aktion mit dem **nächsten** Argument Fehlermeldungen unterdrückt, und klicken Sie dann die **ÖffnenFormular** -Aktion zum Öffnen eines Formulars verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cb23-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="1cb23-120">In diesem Beispiel wird ein Fehler absichtlich erstellt, durch die **GeheZuDatensatz** -Aktion verwenden, um zum vorherigen Datensatz zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1cb23-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="1cb23-121">Die Bedingung \*\* \[MacroError\].\[ Anzahl\]\<\>0\*\* testet **MacroError** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1cb23-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="1cb23-122">Wenn ein Fehler aufgetreten ist, die Fehlernummer ungleich NULL ist, und die **Abfrageergebnis** -Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="1cb23-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="1cb23-123">Das Meldungsfeld zeigt den Namen der Aktion, die (in diesem Fall die **GeheZuDatensatz** -Aktion) den Fehler verursacht hat, und die Fehlernummer wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cb23-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="1cb23-124">Schließlich werden beim Ausführen der Aktion **ClearMacroError** **MacroError** -Objekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1cb23-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cb23-125">Bedingung</span><span class="sxs-lookup"><span data-stu-id="1cb23-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="1cb23-126">Aktion</span><span class="sxs-lookup"><span data-stu-id="1cb23-126">Action</span></span></p></th>
<th><p><span data-ttu-id="1cb23-127">Argumente</span><span class="sxs-lookup"><span data-stu-id="1cb23-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1cb23-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb23-129"><strong>Wechseln Sie zu</strong>: <strong>Weiter</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="1cb23-130"><strong>ÖffnenFormular</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb23-131"><strong>Formularname</strong>: CategoryForm-<strong>Ansicht</strong>: <strong>FormWindow Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1cb23-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb23-133"><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Datensatz</strong>: vorherigen</span><span class="sxs-lookup"><span data-stu-id="1cb23-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb23-134">[MacroError].[Number]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="1cb23-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="1cb23-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb23-136"><strong>Meldung</strong>: =&quot;Fehler # &quot; &amp; [MacroError]. [Anzahl] &amp; &quot; auf &quot; &amp; [MacroError]. [Aktionsname] &amp; &quot; Aktion. &quot; <strong>Signalton</strong>: <strong>YesType</strong>: Informationen</span><span class="sxs-lookup"><span data-stu-id="1cb23-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1cb23-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="1cb23-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

