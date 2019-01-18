---
title: OpenForm-Makroaktion
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707626"
---
# <a name="openform-macro-action"></a><span data-ttu-id="0e2ba-102">OpenForm-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="0e2ba-102">OpenForm macro action</span></span>

<span data-ttu-id="0e2ba-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e2ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e2ba-104">Sie können die **ÖffnenFormular** -Aktion zum Öffnen eines Formulars in der Formularansicht, Entwurfsansicht, Seitenansicht oder Datenblattansicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="0e2ba-105">Sie können den Dateneingabe- und den Fenstermodus für das Formular auswählen und die Datensätze einschränken, die das Formular anzeigt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="0e2ba-106">Setting</span><span class="sxs-lookup"><span data-stu-id="0e2ba-106">Setting</span></span>

<span data-ttu-id="0e2ba-107">Die **OpenForm** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e2ba-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="0e2ba-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e2ba-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-110"><strong>Formularname</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-111">Der Name der zu öffnenden Formulars.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-111">The name of the form to open.</span></span> <span data-ttu-id="0e2ba-112">Das Feld <strong>Formularname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Formulare in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="0e2ba-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-113">This is a required argument.</span></span> <span data-ttu-id="0e2ba-114">Wenn Sie ein Makro mit der <strong>ÖffnenFormular</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst für das Formular mit diesem Namen in die Bibliotheksdatenbank, und klicken Sie dann in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-116">Die Ansicht, in der das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-116">The view in which the form will open.</span></span> <span data-ttu-id="0e2ba-117">Klicken Sie auf <strong>Formular</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>Datenblatt</strong>, <strong>PivotTable-</strong>oder <strong>PivotChart</strong> in das Feld <strong>Anzeigen</strong> .</span><span class="sxs-lookup"><span data-stu-id="0e2ba-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="0e2ba-118">Der Standardwert ist <strong>Formular</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="0e2ba-119"><strong>Hinweis</strong>: die Einstellung des Arguments <STRONG>Ansicht</STRONG> setzt die Einstellungen der Eigenschaften für das Formular <STRONG>DefaultView</STRONG> und <STRONG>ViewsAllowed</STRONG> außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="0e2ba-120">Beispielsweise wenn <STRONG>ViewsAllowed</STRONG> -Eigenschaft eines Formulars auf <STRONG>Datenblatt</STRONG>festgelegt ist, können weiterhin die <STRONG>ÖffnenFormular</STRONG> -Aktion Sie das Formular in der Formularansicht geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-121"><strong>Filter Name</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-122">Ein Filter, der Datensätze des Formulars einschränkt oder sortiert.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="0e2ba-123">Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="0e2ba-124">Die Abfrage muss jedoch alle Felder enthalten, in der Form, die Sie öffnen oder dessen <strong>OutputAllFields</strong> -Eigenschaft auf <strong>Ja</strong>festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-125"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-126">Eine gültige SQL WHERE-Klausel (ohne das Wort, in dem) oder ein Ausdruck, der Zugriff verwendet, um Datensätze aus dem Formular zugrunde liegenden Tabelle oder Abfrage.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="0e2ba-127">Wenn Sie einen Filter mit dem Argument <strong>Filtername</strong> auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="0e2ba-128">Wenn Sie ein Formular öffnen und seine Datensätze auf diejenigen angegeben durch den Wert eines Steuerelements in ein anderes Formular zu beschränken, verwenden Sie den folgenden Ausdruck: <strong>[</strong><em>Fieldname</em><strong>] = Formulare! [</strong> <em>Formularname</em> <strong>]! [</strong><em>Steuerelementname in anderem Formular</em><strong>]</strong> ersetzen <em>Fieldname</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des zu öffnenden Formulars.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="0e2ba-129">Ersetzen Sie <em>Formname</em> und <em>Steuerelementname in anderen Formular</em> mit dem Namen des anderen Formulars und das Steuerelement, Formular, das den Wert enthält, den Datensätze im ersten Formular übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="0e2ba-130"><strong>Hinweis</strong>: die maximale Länge des Arguments <STRONG>Bedingung</STRONG> beträgt 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="0e2ba-131">Wenn Sie eine komplexere SQL WHERE-Klausel eingeben müssen, verwenden Sie die <STRONG>OpenForm</STRONG> -Methode des <STRONG>DoCmd</STRONG> -Objekts in einem Visual Basic für Applikationen (VBA) Modul stattdessen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="0e2ba-132">Sie können in VBA SQL WHERE-Klausel Anweisungen von bis zu 32.768 Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-133"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-134">Der Dateneingabemodus für das Formular.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-134">The data entry mode for the form.</span></span> <span data-ttu-id="0e2ba-135">Dies gilt nur für Formulare, die in der Formularansicht oder in der Datenblattansicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="0e2ba-136">Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen).</span><span class="sxs-lookup"><span data-stu-id="0e2ba-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="0e2ba-137">Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="0e2ba-138"><strong>Hinweise</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="0e2ba-139">Die Einstellung des Arguments <strong>Datenmodus</strong> setzt die Einstellungen der Eigenschaften für das Formular <strong>BearbeitungenZulassen</strong>, <strong>LöschenZulassen</strong>, <strong>AnfügenZulassen</strong>und <strong>DatenEingeben</strong> außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="0e2ba-140">Beispielsweise wenn <strong>AllowEdits</strong> -Eigenschaft eines Formulars auf <strong>Nein</strong>festgelegt ist, können weiterhin die <strong>ÖffnenFormular</strong> -Aktion Sie zum Öffnen des Formulars im Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="0e2ba-141">Wenn Sie dieses Argument leer lassen, öffnet Access das Formular in der Dateneingabemodus des Formulars <strong>BearbeitungenZulassen</strong>, <strong>LöschenZulassen</strong>, <strong>AnfügenZulassen</strong>und <strong>DatenEingeben</strong> Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-142"><strong>Window Mode</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-143">Der Fenstermodus, in dem das Formular wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-143">The window mode in which the form opens.</span></span> <span data-ttu-id="0e2ba-144">Klicken Sie auf <strong>Normal</strong> (das Formular wird in den Modus durch seine Eigenschaften festgelegt), <strong>ausgeblendet</strong> (das Formular ist ausgeblendet), <strong>Symbol</strong> (das Formular wird als kleine Titelleiste am unteren Rand des Bildschirms geöffnet), oder ein <strong>Dialogfeld</strong> (des Formulars <strong>Modal</strong> und PopUp <strong> </strong>auf <strong>Ja</strong>festgelegt).</span><span class="sxs-lookup"><span data-stu-id="0e2ba-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="0e2ba-145">Die Standardeinstellung ist <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="0e2ba-146"><strong>Hinweis</strong>: Einige Einstellungen für das Argument <STRONG>Fenstermodus</STRONG> beim Verwenden von Dokumenten im Registerkartenformat nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="0e2ba-147">So wechseln Sie zu überlappenden Fenstern:</span><span class="sxs-lookup"><span data-stu-id="0e2ba-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="0e2ba-148">Klicken Sie auf der Registerkarte Datei, und klicken Sie dann auf <strong>Optionen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0e2ba-149">Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0e2ba-150">Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong>unter <strong>Dokumentfensteroptionen</strong>auf <strong>Überlappende Fenster</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0e2ba-151">Klicken Sie auf <strong>OK</strong>, schließen Sie die Datenbank dann, und öffnen Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e2ba-152">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e2ba-152">Remarks</span></span>

<span data-ttu-id="0e2ba-153">Diese Aktion entspricht dem Doppelklicken auf ein Formular im Navigationsbereich oder der rechten Maustaste auf das Formular im Navigationsbereich und dann eine Ansicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="0e2ba-154">Ein Formular ist Modal (es muss geschlossen oder ausgeblendet werden, bevor der Benutzer eine andere Aktion ausführen kann) oder ungebunden (der Benutzer kann zu anderen Fenstern wechseln, während das Formular geöffnet ist).</span><span class="sxs-lookup"><span data-stu-id="0e2ba-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="0e2ba-155">Es kann auch ein Popup-Formular (ein Formular zum Sammeln oder Anzeigen von Informationen, die vor allen anderen Access-Fenster angezeigt) sein.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="0e2ba-156">Die Eigenschaften **Modal** und **PopUp** wird festgelegt, wenn Sie das Formular entwerfen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="0e2ba-157">Wenn Sie für das Argument **Fenstermodus** **Normal** verwenden, öffnet sich das Formular im Modus durch diese Einstellungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="0e2ba-158">Wenn Sie das **Dialogfeld** für das Argument **Fenstermodus** verwenden, werden diese Eigenschaften beide auf **Ja**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="0e2ba-159">Als ausgeblendet oder als Symbol öffnen ein Formulars in den Modus durch seine Einstellungen angegeben werden, wenn Sie anzeigen oder Wiederherstellen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="0e2ba-160">Beim Öffnen eines Formulars mit das Argument **Fenstermodus** auf **Dialog**festgelegt unterbricht Access das Makro aus, bis das Formular geschlossen oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="0e2ba-161">Sie können ein Formular ausblenden, indem die **Visible** -Eigenschaft mithilfe der **SetzenWert** -Aktion auf **Nein** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="0e2ba-162">Sie können ein Formular im Navigationsbereich auswählen und ziehen Sie ihn in einer Zeile der Makro-Aktion.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="0e2ba-163">Dadurch wird automatisch eine **ÖffnenFormular** -Aktion, die das Formular in der Formularansicht geöffnet wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="0e2ba-164">Der Filter und die WHERE-Bedingung ergeben die Einstellung der **Filter** -Eigenschaft des Formulars.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="0e2ba-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e2ba-165">Examples</span></span>

<span data-ttu-id="0e2ba-166">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="0e2ba-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="0e2ba-167">Mit dem folgende Makro wird das Formular Artikel Hinzufügen einer Schaltfläche auf dem Formular Lieferanten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="0e2ba-168">Es wird die Verwendung der **Echo**, **CloseWindow**, **ÖffnenFormular**, **SetzenWert**und **GeheZuSteuerelement** -Aktionen.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="0e2ba-169">Die **SetzenWert** -Aktion wird das Steuerelement Lieferanten-ID auf dem Formular auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="0e2ba-170">Klicken Sie dann die **GeheZuSteuerelement** -Aktion verschiebt den Fokus auf das Feld Kategorie-ID, beginnen Sie können Daten für das neue Produkt eingeben.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="0e2ba-171">Dieses Makro sollte der Schaltfläche Artikel hinzufügen im Formular Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e2ba-172">Aktion</span><span class="sxs-lookup"><span data-stu-id="0e2ba-172">Action</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-173">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="0e2ba-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-174">Kommentar</span><span class="sxs-lookup"><span data-stu-id="0e2ba-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-176"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-177">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0e2ba-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-178"><strong>FensterSchließen</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-179"><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-180">Schließen des Produktlistenformulars</span><span class="sxs-lookup"><span data-stu-id="0e2ba-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-181"><strong>ÖffnenFormular</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-182"><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-183">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="0e2ba-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-184"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-185"><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="0e2ba-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-186">Legen Sie das Steuerelement auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-188"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="0e2ba-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-189">Wechseln Sie auf die Kategorie-ID-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e2ba-p116">Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-p116">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="0e2ba-194">**Synchronisieren von Formularen mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="0e2ba-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e2ba-195">Bedingung</span><span class="sxs-lookup"><span data-stu-id="0e2ba-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-196">Aktion</span><span class="sxs-lookup"><span data-stu-id="0e2ba-196">Action</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-197">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="0e2ba-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="0e2ba-198">Kommentar</span><span class="sxs-lookup"><span data-stu-id="0e2ba-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0e2ba-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-200"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-201">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0e2ba-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="0e2ba-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-204"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="0e2ba-205"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</span><span class="sxs-lookup"><span data-stu-id="0e2ba-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-206">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2ba-207">...</span><span class="sxs-lookup"><span data-stu-id="0e2ba-207"></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-209"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="0e2ba-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-210">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2ba-211">...</span><span class="sxs-lookup"><span data-stu-id="0e2ba-211"></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0e2ba-213">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0e2ba-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-215"><strong>Formularname</strong>: Produkt Liste <strong>Anzeigen</strong>: <strong>DatasheetFilter Name</strong>: <strong>Bedingung</strong>: [Lieferanten-Nr] = [Formulare]! [Lieferanten]! [Lieferanten-Nr] <strong>Datenmodus</strong>: <strong>OnlyWindow Lesemodus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-216">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="0e2ba-217"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="0e2ba-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2ba-218"><strong>Rechts</strong>: 0.7799&quot; <strong>nach unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="0e2ba-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="0e2ba-219">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="0e2ba-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

