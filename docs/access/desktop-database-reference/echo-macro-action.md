---
title: Echo-Makroaktion (Access-Desktop-Daten Bankreferenz)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293623"
---
# <a name="echo-macro-action"></a><span data-ttu-id="56b6e-102">Echo-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="56b6e-102">Echo macro action</span></span>

<span data-ttu-id="56b6e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56b6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56b6e-104">Sie können die **Echo** -Aktion verwenden, um anzugeben, ob Echo eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="56b6e-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="56b6e-105">Sie können diese Aktion beispielsweise verwenden, um die Ergebnisse eines Makros während der Ausführung ein-oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="56b6e-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="56b6e-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="56b6e-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="56b6e-107">Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="56b6e-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="56b6e-108">Die **Echo** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="56b6e-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56b6e-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="56b6e-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="56b6e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56b6e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56b6e-111"><strong>Echo ein</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-112">Klicken Sie im Feld <strong>Echo on</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator auf <strong>Ja</strong> (Echo aktivieren) oder <strong>Nein</strong> (Echo aus).</span><span class="sxs-lookup"><span data-stu-id="56b6e-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="56b6e-113">Die Standardeinstellung ist <strong>Ja</strong>.</span><span class="sxs-lookup"><span data-stu-id="56b6e-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b6e-114"><strong>Statusleistentext</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-115">Der Text, der in der Statusleiste angezeigt werden soll, wenn ECHO deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="56b6e-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="56b6e-116">Wenn Echo beispielsweise deaktiviert ist, kann in der Statusleiste angezeigt &quot;werden, dass das Makro gerade läuft.&quot;</span><span class="sxs-lookup"><span data-stu-id="56b6e-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56b6e-117">Wenn ein Makro ausgeführt wird, zeigt die Bildschirmaktualisierung oft Informationen an, die für das Funktionieren des Makros nicht unbedingt erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="56b6e-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="56b6e-118">Wenn Sie das Argument **Echo auf** **Nein**festlegen, wird das Makro ohne Aktualisieren des Bildschirms ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56b6e-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="56b6e-119">Nach Abschluss des Makros schaltet Access das Echo automatisch wieder ein und zeichnet das Fenster neu.</span><span class="sxs-lookup"><span data-stu-id="56b6e-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="56b6e-120">Die Einstellung **keine** für das Argument **Echo on wirkt sich** nicht auf die Funktionalität des Makros oder seiner Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="56b6e-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="56b6e-121">Die **Echo** -Aktion unterdrückt die Anzeige von modalen Dialogfeldern wie beispielsweise Fehlermeldungen oder Popupformularen wie z. b. Eigenschaftenblätter nicht.</span><span class="sxs-lookup"><span data-stu-id="56b6e-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="56b6e-122">Sie können Dialogfelder und Popupformulare verwenden, um Informationen zu erfassen oder anzuzeigen, auch wenn ECHO deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="56b6e-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="56b6e-123">Verwenden Sie die **Warn** Meldungen-Aktion, um alle Nachrichten oder Dialogfelder außer Fehler Meldungsfeldern und Dialogfeldern zu unterdrücken, in denen der Benutzerinformationen eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="56b6e-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="56b6e-124">Sie können die **Echo** -Aktion in einem Makro mehrmals ausführen.</span><span class="sxs-lookup"><span data-stu-id="56b6e-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="56b6e-125">Auf diese Weise können Sie den Text der Statusleiste ändern, während das Makro ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56b6e-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="56b6e-126">Wenn Sie Echo deaktivieren, können Sie die **anzeigen Sanduhrzeiger** -Aktion verwenden, um den Mauszeiger in ein Sanduhrsymbol zu ändern (oder für das Mauszeiger Symbol, das Sie für "busy" festgelegt haben), um einen visuellen Hinweis darauf zu geben, dass das Makro ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56b6e-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="56b6e-127">Verwenden Sie die **Echo** -Methode des **DoCmd** -Objekts, um die **Echo** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="56b6e-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="56b6e-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56b6e-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="56b6e-129">Festlegen des Werts eines Steuerelements mithilfe eines Makros</span><span class="sxs-lookup"><span data-stu-id="56b6e-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="56b6e-130">Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="56b6e-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="56b6e-131">Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, \*\*SetzenWert \*\* und **GeheZuSteuerelement**.</span><span class="sxs-lookup"><span data-stu-id="56b6e-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="56b6e-132">Mit \*\*\*\* der SetValue-Aktion wird das Lieferanten-ID-Steuerelement im Formular Produkte auf den aktuellen Lieferanten im Formular Lieferanten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="56b6e-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="56b6e-133">Die **gotoCONTROL** -Aktion verschiebt dann den Fokus auf das Feld Kategorie-ID, in dem Sie mit der Eingabe von Daten für das neue Produkt beginnen können.</span><span class="sxs-lookup"><span data-stu-id="56b6e-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="56b6e-134">Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="56b6e-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56b6e-135">Aktion</span><span class="sxs-lookup"><span data-stu-id="56b6e-135">Action</span></span></p></th>
<th><p><span data-ttu-id="56b6e-136">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="56b6e-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="56b6e-137">Kommentar</span><span class="sxs-lookup"><span data-stu-id="56b6e-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56b6e-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-139"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-140">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="56b6e-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b6e-141"><strong>Fenster schließen</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-142"><strong>Objekttyp</strong>: <strong>Formularobjekt Name</strong>: Produktlisten <strong>Speicher</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-143">Schließen des Produktlistenformulars</span><span class="sxs-lookup"><span data-stu-id="56b6e-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b6e-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-145"><strong>Formular Name</strong>: Produkt <strong>Ansicht</strong>: <strong>FormData Modus</strong>: <strong>addwindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-146">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="56b6e-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b6e-147"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-148"><strong>Element</strong>: [Formulare]! [Products]! LieferantenNr <strong>Ausdruck</strong>: Lieferanten-Nr.</span><span class="sxs-lookup"><span data-stu-id="56b6e-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="56b6e-149">Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Formular Lieferanten fest.</span><span class="sxs-lookup"><span data-stu-id="56b6e-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b6e-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-151"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="56b6e-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="56b6e-152">Wechseln Sie zum Steuerelement Category ID.</span><span class="sxs-lookup"><span data-stu-id="56b6e-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="56b6e-153">Synchronisieren von Formularen mithilfe eines Makros</span><span class="sxs-lookup"><span data-stu-id="56b6e-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="56b6e-154">Mit dem folgenden Makro wird das Produktlisten Formular in der unteren rechten Ecke des Formulars Lieferanten geöffnet, in dem die Produkte des aktuellen Lieferanten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="56b6e-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="56b6e-155">Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**.</span><span class="sxs-lookup"><span data-stu-id="56b6e-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="56b6e-156">Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**.</span><span class="sxs-lookup"><span data-stu-id="56b6e-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="56b6e-157">Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="56b6e-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56b6e-158">Bedingung</span><span class="sxs-lookup"><span data-stu-id="56b6e-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="56b6e-159">Aktion</span><span class="sxs-lookup"><span data-stu-id="56b6e-159">Action</span></span></p></th>
<th><p><span data-ttu-id="56b6e-160">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="56b6e-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="56b6e-161">Kommentar</span><span class="sxs-lookup"><span data-stu-id="56b6e-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="56b6e-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-163"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-164">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="56b6e-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b6e-165">IsNull ([Lieferanten-ID])</span><span class="sxs-lookup"><span data-stu-id="56b6e-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="56b6e-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-167"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="56b6e-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="56b6e-168"><strong>Beep</strong>: <strong>jatyp</strong>: <strong>Keinetitel</strong>: Wählen Sie einen Zulieferer aus</span><span class="sxs-lookup"><span data-stu-id="56b6e-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="56b6e-169">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="56b6e-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b6e-170">...</span><span class="sxs-lookup"><span data-stu-id="56b6e-170"></span></span></p></td>
<td><p><span data-ttu-id="56b6e-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-172"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="56b6e-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="56b6e-173">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="56b6e-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b6e-174">...</span><span class="sxs-lookup"><span data-stu-id="56b6e-174"></span></span></p></td>
<td><p><span data-ttu-id="56b6e-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="56b6e-176">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="56b6e-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="56b6e-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-178"><strong>Formularname</strong>: Produktlisten <strong>Ansicht</strong>: <strong>Datenblatt Filtername</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Lieferanten]! LieferantenNr <strong>Datenmodus</strong>: <strong>Lese-schreibgeschütztfenstermodus-Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-179">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="56b6e-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="56b6e-180"><strong>Verschiebenundgrößeändernfenster</strong></span><span class="sxs-lookup"><span data-stu-id="56b6e-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="56b6e-181"><strong>rechts</strong>: 0,7799&quot; <strong>unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="56b6e-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="56b6e-182">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="56b6e-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

