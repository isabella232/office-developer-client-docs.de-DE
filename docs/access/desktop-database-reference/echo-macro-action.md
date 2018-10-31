---
title: Echo-Makroaktion (Access PC-Datenbank-Referenz)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39471ea4bab2ec1bbeb8cd22ecb00aa5df3bc411
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863969"
---
# <a name="echo-macro-action"></a><span data-ttu-id="37b33-102">Echo Macro Action</span><span class="sxs-lookup"><span data-stu-id="37b33-102">Echo Macro Action</span></span>


<span data-ttu-id="37b33-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37b33-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37b33-104">Die **Echo** -Aktion können Sie angeben, ob Echo aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37b33-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="37b33-105">Beispielsweise können Sie diese Aktion verwenden, um auszublenden oder die Ergebnisse eines Makros anzuzeigen, während der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="37b33-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="37b33-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="37b33-106">Setting</span></span>


> [!NOTE]
> <span data-ttu-id="37b33-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="37b33-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



<span data-ttu-id="37b33-109">Die **Echo** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="37b33-109">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37b33-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="37b33-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="37b33-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37b33-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37b33-112"><strong>Klicken Sie auf dem Bildschirm</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-112"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-113">Klicken Sie auf <strong>Ja</strong> (Echo aktivieren) oder auf <strong>Nein</strong> (Echo deaktivieren) im Feld <strong>Echo</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators.</span><span class="sxs-lookup"><span data-stu-id="37b33-113">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="37b33-114">Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="37b33-114">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b33-115"><strong>Statusleistentext</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-115"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-116">Der Text in der Statusleiste angezeigt, wenn Echo ausgeschaltet wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37b33-116">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="37b33-117">Beispielsweise wenn Echo deaktiviert ist, die Statusleiste kann anzeigen &quot;das Makro ausgeführt wird.&quot;</span><span class="sxs-lookup"><span data-stu-id="37b33-117">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37b33-118">Wenn führt ein Makro, Bildschirm aktualisieren häufig zeigt Informationen für das Funktionieren des Makros nicht entscheidend.</span><span class="sxs-lookup"><span data-stu-id="37b33-118">When runs a macro, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="37b33-119">Wenn Sie das Argument **Echo** auf **Nein**festlegen, wird das Makro ausgeführt, ohne dass den Bildschirm aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37b33-119">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="37b33-120">Wenn das Makro abgeschlossen ist, werden von Access automatisch Echo wieder eingeschaltet und wird das Fenster aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37b33-120">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="37b33-121">Die Einstellung " **No** " für das Argument **Echo** wirkt sich nicht auf die Funktionalität des Makros oder die Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="37b33-121">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="37b33-122">Die **Echo** -Aktion unterdrückt nicht die Anzeige von modale Dialogfelder, wie Fehlermeldungen oder Popup Formulare, z. B. Eigenschaftenseiten.</span><span class="sxs-lookup"><span data-stu-id="37b33-122">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="37b33-123">Können Dialogfeldern und pop-up-Formulare zum Sammeln und Anzeigen von Informationen, selbst wenn Echo deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37b33-123">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="37b33-124">Um alle Nachricht oder Dialogfelder außer Fehlermeldungsfelder und Dialogfelder, in denen den Benutzer zur Eingabe von Informationen zu unterdrücken, verwenden Sie die **Warnmeldungen** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="37b33-124">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="37b33-125">Sie können die **Echo** -Aktion in einem Makro nur einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="37b33-125">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="37b33-126">Dadurch können Sie den Text in der Statusleiste ändern, während das Makro ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b33-126">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="37b33-127">Wenn Sie Echo deaktivieren, können Sie die **Anzeigensanduhrzeiger** -Aktion verwenden, so ändern Sie den Mauszeiger in ein Sanduhrsymbol (oder jegliches Mauszeigersymbol festlegen "Beschäftigt") visuell bereitstellen, auf denen das Makro ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b33-127">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="37b33-128">Um die **Echo** -Aktion in einem Visual Basic für Applikationen (VBA)-Modul auszuführen, verwenden Sie die **Echo** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="37b33-128">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="37b33-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37b33-129">Examples</span></span>

<span data-ttu-id="37b33-130">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="37b33-130">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="37b33-131">Mit dem folgende Makro wird das Formular Artikel Hinzufügen einer Schaltfläche auf dem Formular Lieferanten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="37b33-131">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="37b33-132">Es wird die Verwendung der **Echo**, **CloseWindow**, **ÖffnenFormular**, **SetzenWert**und **GeheZuSteuerelement** -Aktionen.</span><span class="sxs-lookup"><span data-stu-id="37b33-132">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="37b33-133">Die **SetzenWert** -Aktion wird das Steuerelement Lieferanten-ID auf dem Formular auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37b33-133">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="37b33-134">Klicken Sie dann die **GeheZuSteuerelement** -Aktion verschiebt den Fokus auf das Feld Kategorie-ID, beginnen Sie können Daten für das neue Produkt eingeben.</span><span class="sxs-lookup"><span data-stu-id="37b33-134">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="37b33-135">Dieses Makro sollte der Schaltfläche Artikel hinzufügen im Formular Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="37b33-135">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37b33-136">Aktion</span><span class="sxs-lookup"><span data-stu-id="37b33-136">Action</span></span></p></th>
<th><p><span data-ttu-id="37b33-137">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="37b33-137">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="37b33-138">Kommentar</span><span class="sxs-lookup"><span data-stu-id="37b33-138">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37b33-139"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-139"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-140"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-140"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-141">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="37b33-141">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b33-142"><strong>FensterSchließen</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-142"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-143"><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-143"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-144">Schließen des Produktlistenformulars</span><span class="sxs-lookup"><span data-stu-id="37b33-144">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b33-145"><strong>ÖffnenFormular</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-145"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-146"><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-146"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-147">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="37b33-147">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b33-148"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-148"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-149"><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="37b33-149"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="37b33-150">Legen Sie das Steuerelement auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37b33-150">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b33-151"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-151"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-152"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="37b33-152"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="37b33-153">Wechseln Sie auf die Kategorie-ID-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="37b33-153">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37b33-154">**Synchronisieren von Formularen mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="37b33-154">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="37b33-155">Mit dem folgende Makro wird das Formular Artikelliste geöffnet, in der unteren rechten Ecke des Formulars Lieferanten, die aktuellen Lieferanten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="37b33-155">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="37b33-156">Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**.</span><span class="sxs-lookup"><span data-stu-id="37b33-156">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="37b33-157">Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**.</span><span class="sxs-lookup"><span data-stu-id="37b33-157">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="37b33-158">Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="37b33-158">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37b33-159">Bedingung</span><span class="sxs-lookup"><span data-stu-id="37b33-159">Condition</span></span></p></th>
<th><p><span data-ttu-id="37b33-160">Aktion</span><span class="sxs-lookup"><span data-stu-id="37b33-160">Action</span></span></p></th>
<th><p><span data-ttu-id="37b33-161">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="37b33-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="37b33-162">Kommentar</span><span class="sxs-lookup"><span data-stu-id="37b33-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="37b33-163"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-164"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-165">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="37b33-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b33-166">IsNull ([Lieferanten-Nr])</span><span class="sxs-lookup"><span data-stu-id="37b33-166">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="37b33-167"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-167"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-168"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="37b33-168"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="37b33-169"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</span><span class="sxs-lookup"><span data-stu-id="37b33-169"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="37b33-170">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="37b33-170">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b33-171">...</span><span class="sxs-lookup"><span data-stu-id="37b33-171"></span></span></p></td>
<td><p><span data-ttu-id="37b33-172"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-172"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-173"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="37b33-173"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="37b33-174">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="37b33-174">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b33-175">...</span><span class="sxs-lookup"><span data-stu-id="37b33-175"></span></span></p></td>
<td><p><span data-ttu-id="37b33-176"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-176"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="37b33-177">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="37b33-177">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="37b33-178"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-178"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-179"><strong>Formularname</strong>: Produkt Liste <strong>Anzeigen</strong>: <strong>DatasheetFilter Name</strong>: <strong>Bedingung</strong>: [Lieferanten-Nr] = [Formulare]! [Lieferanten]! [Lieferanten-Nr] <strong>Datenmodus</strong>: <strong>OnlyWindow Lesemodus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-179"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-180">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="37b33-180">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="37b33-181"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="37b33-181"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="37b33-182"><strong>Rechts</strong>: 0.7799&quot; <strong>nach unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="37b33-182"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="37b33-183">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="37b33-183">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

