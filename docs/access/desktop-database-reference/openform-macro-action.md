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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288371"
---
# <a name="openform-macro-action"></a><span data-ttu-id="b0b52-102">OpenForm-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="b0b52-102">OpenForm macro action</span></span>

<span data-ttu-id="b0b52-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0b52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0b52-104">Sie können die **OpenForm** -Aktion verwenden, um ein Formular in der Formularansicht, in der Entwurfsansicht, in der Seitenansicht oder in der Datenblatt Anzeige zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="b0b52-105">Sie können den Dateneingabe- und den Fenstermodus für das Formular auswählen und die Datensätze einschränken, die das Formular anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="b0b52-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b0b52-106">Setting</span></span>

<span data-ttu-id="b0b52-107">Die **OpenForm** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b0b52-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b52-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="b0b52-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b0b52-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b52-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-110"><strong>Formular Name</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-111">Der Name des zu öffnenden Formulars.</span><span class="sxs-lookup"><span data-stu-id="b0b52-111">The name of the form to open.</span></span> <span data-ttu-id="b0b52-112">Im Feld <strong>Formular Name</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator werden alle Formulare in der aktuellen Datenbank angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="b0b52-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="b0b52-113">This is a required argument.</span></span> <span data-ttu-id="b0b52-114">Wenn Sie ein Makro ausführen, das <strong></strong> die OpenForm-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Formular mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-116">Die Ansicht, in der das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b0b52-116">The view in which the form will open.</span></span> <span data-ttu-id="b0b52-117">Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Formular</strong>, <strong>Entwurf</strong>, <strong>Seiten</strong>Ansicht, <strong>Datenblatt</strong>, <strong>PivotTable</strong>oder <strong>PivotChart</strong> .</span><span class="sxs-lookup"><span data-stu-id="b0b52-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="b0b52-118">Der Standardwert ist <strong>Form</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="b0b52-119"><strong>Hinweis</strong>: die Einstellung für das Argument <STRONG>View</STRONG> setzt die Einstellungen der Eigenschaften <STRONG>DefaultView</STRONG> und <STRONG>ViewsAllowed</STRONG> des Formulars außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="b0b52-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="b0b52-120">Wenn beispielsweise die <STRONG>ViewsAllowed</STRONG> -Eigenschaft eines Formulars auf <STRONG>Datenblatt</STRONG>festgelegt ist, können Sie die <STRONG>OpenForm</STRONG> -Aktion verwenden, um das Formular in der Formularansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-121"><strong>Filter Name</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-122">Ein Filter, der die Datensätze des Formulars einschränkt oder sortiert.</span><span class="sxs-lookup"><span data-stu-id="b0b52-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="b0b52-123">Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben.</span><span class="sxs-lookup"><span data-stu-id="b0b52-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="b0b52-124">Die Abfrage muss jedoch alle Felder in dem Formular enthalten, das Sie öffnen, oder die <strong>AlleFelderAusgeben</strong> -Eigenschaft ist auf <strong>Ja</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-125"><strong>Bedingung</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-126">Eine gültige SQL-WHERE-Klausel (ohne das Wort WHERE) oder Expression, die Access zum Auswählen von Datensätzen aus der zugrunde liegenden Tabelle oder Abfrage des Formulars verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0b52-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="b0b52-127">Wenn Sie einen Filter mit dem Argument <strong>Filter Name</strong> auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters an.</span><span class="sxs-lookup"><span data-stu-id="b0b52-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="b0b52-128">Verwenden Sie den folgenden Ausdruck, um ein Formular zu öffnen und seine Datensätze auf die zu beschränken, die durch den Wert eines Steuerelements in einem anderen Formular angegeben werden: <strong>[</strong><em>FieldName</em><strong>] = Forms! [</strong> <em>Formularname</em> <strong>]! [</strong><em>Steuerelementname in anderen Formularen</em><strong>]</strong> <em>FieldName</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des zu öffnenden Formulars ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="b0b52-129">Ersetzen <em></em> Sie FormName und <em>Steuerelement</em> Name in einem anderen Formular durch den Namen des anderen Formulars und das Steuerelement auf dem anderen Formular, das den Wert enthält, den die Datensätze im ersten Formular übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="b0b52-130"><strong>Hinweis</strong>: die maximale Länge des Arguments <STRONG>Where Condition</STRONG> beträgt 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="b0b52-131">Wenn Sie eine komplexere SQL-WHERE-Klausel länger als diese eingeben müssen, verwenden <STRONG></STRONG> Sie stattdessen die OpenForm-Methode des <STRONG>DoCmd</STRONG> -Objekts in einem VBA-Modul (Visual Basic für Applikationen).</span><span class="sxs-lookup"><span data-stu-id="b0b52-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="b0b52-132">Sie können SQL WHERE-Klauselanweisungen in VBA mit bis zu 32.768 Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="b0b52-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-133"><strong>Datenmodus</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-134">Der Dateneingabemodus für das Formular.</span><span class="sxs-lookup"><span data-stu-id="b0b52-134">The data entry mode for the form.</span></span> <span data-ttu-id="b0b52-135">Dies gilt nur für Formulare, die in der Formularansicht oder in der Datenblattansicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0b52-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="b0b52-136">Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen).</span><span class="sxs-lookup"><span data-stu-id="b0b52-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="b0b52-137">Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="b0b52-138"><strong>Hinweise</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="b0b52-139">Die Einstellung des <strong>Datenmodus</strong> -Arguments setzt die Einstellungen der Eigenschaften <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>und <strong>DataEntry</strong> des Formulars außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="b0b52-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="b0b52-140">Wenn die <strong>AllowEdits</strong> -Eigenschaft eines Formulars beispielsweise auf <strong>Nein</strong>festgelegt ist, können Sie die OpenForm-Aktion verwenden, um das Formular im Bearbeitungsmodus zu öffnen. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="b0b52-141">Wenn Sie dieses Argument leer lassen, öffnet Access das Formular im Dateneingabemodus, der von den <strong>AllowEdits</strong>-, <strong>AllowDeletions</strong>-, <strong>AllowAdditions</strong>-und <strong>DataEntry</strong> -Eigenschaften des Formulars festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b0b52-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-142"><strong>Window Mode</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-143">Der Fenstermodus, in dem das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b0b52-143">The window mode in which the form opens.</span></span> <span data-ttu-id="b0b52-144">Klicken Sie auf <strong>Normal</strong> (das Formular wird in dem Modus geöffnet, der durch seine Eigenschaften festgelegt ist), <strong>ausgeblendet</strong> (das Formular ist ausgeblendet), <strong>Symbol</strong> (das Formular wird minimiert als kleine Titelleiste am unteren Rand des Bildschirms geöffnet) oder <strong>Dialog Feld</strong> (das Formular <strong>Modal</strong> und <strong>Popup </strong>Eigenschaften sind auf <strong>Ja</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="b0b52-145">Die Standardeinstellung ist <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="b0b52-146"><strong>Hinweis</strong>: einige Einstellungen im <STRONG>Fenstermodus</STRONG> -Argument gelten nicht bei der Verwendung von Registerkarten Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="b0b52-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="b0b52-147">So wechseln Sie zu überlappenden Fenstern:</span><span class="sxs-lookup"><span data-stu-id="b0b52-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="b0b52-148">Klicken Sie auf die Registerkarte Datei und dann auf <strong>Optionen</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b0b52-149">Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b0b52-150">Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong>unter <strong>dokumentfensterOptionen</strong>auf über <strong>Lapp Ende Fenster</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b52-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b0b52-151">Klicken Sie auf <strong>OK</strong>, schließen Sie die Datenbank dann, und öffnen Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="b0b52-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b0b52-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0b52-152">Remarks</span></span>

<span data-ttu-id="b0b52-153">Diese Aktion ähnelt dem Doppelklicken auf ein Formular im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Formular im Navigationsbereich und dem Auswählen einer Ansicht.</span><span class="sxs-lookup"><span data-stu-id="b0b52-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="b0b52-154">Ein Formular kann modal sein (es muss geschlossen oder ausgeblendet werden, bevor der Benutzer eine andere Aktion ausführen kann) oder ohne Modus (der Benutzer kann zu anderen Fenstern wechseln, während das Formular geöffnet ist).</span><span class="sxs-lookup"><span data-stu-id="b0b52-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="b0b52-155">Es kann auch ein Popupformular sein (ein Formular, mit dem Informationen gesammelt oder angezeigt werden, die über allen anderen Access-Fenstern liegen).</span><span class="sxs-lookup"><span data-stu-id="b0b52-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="b0b52-156">Sie legen die Eigenschaften **Modal** und **Popup** beim Entwerfen des Formulars fest.</span><span class="sxs-lookup"><span data-stu-id="b0b52-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="b0b52-157">Wenn Sie für das Argument **Window Mode** den **Standard** verwenden, wird das Formular in dem durch diese Eigenschafteneinstellungen angegebenen Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b0b52-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="b0b52-158">Wenn Sie **Dialog** für das Argument **Window Mode** verwenden, werden diese Eigenschaften auf **Ja**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="b0b52-159">Ein Formular, das als ausgeblendet oder als Symbol geöffnet wurde, wird beim Anzeigen oder Wiederherstellen des Modus zurückgegeben, der durch seine Eigenschafteneinstellungen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b0b52-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="b0b52-160">Wenn Sie ein Formular öffnen, dessen **Fenstermodus** -Argument auf **Dialog**festgelegt ist, wird das Makro von Access angehalten, bis das Formular geschlossen oder ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="b0b52-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="b0b52-161">Sie können ein Formular ausblenden, indem Sie die **Visible** -Eigenschaft mithilfe der SetValue-Aktion auf **Nein** festlegen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b0b52-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="b0b52-162">Sie können ein Formular im Navigationsbereich auswählen und in eine Makroaktionszeile ziehen.</span><span class="sxs-lookup"><span data-stu-id="b0b52-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="b0b52-163">Dadurch wird automatisch eine **OpenForm** -Aktion erstellt, mit der das Formular in der Formularansicht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b0b52-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="b0b52-164">Der Filter und die WHERE-Bedingung, die Sie anwenden, werden zur Einstellung der **Filter** -Eigenschaft des Formulars.</span><span class="sxs-lookup"><span data-stu-id="b0b52-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="b0b52-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0b52-165">Examples</span></span>

<span data-ttu-id="b0b52-166">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="b0b52-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="b0b52-167">Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="b0b52-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="b0b52-168">Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, \*\*SetzenWert \*\* und **GeheZuSteuerelement**.</span><span class="sxs-lookup"><span data-stu-id="b0b52-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="b0b52-169">Mit \*\*\*\* der SetValue-Aktion wird das Lieferanten-ID-Steuerelement im Formular Produkte auf den aktuellen Lieferanten im Formular Lieferanten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0b52-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="b0b52-170">Die **gotoCONTROL** -Aktion verschiebt dann den Fokus auf das Feld Kategorie-ID, in dem Sie mit der Eingabe von Daten für das neue Produkt beginnen können.</span><span class="sxs-lookup"><span data-stu-id="b0b52-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="b0b52-171">Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0b52-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b52-172">Aktion</span><span class="sxs-lookup"><span data-stu-id="b0b52-172">Action</span></span></p></th>
<th><p><span data-ttu-id="b0b52-173">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="b0b52-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b0b52-174">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b0b52-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-176"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-177">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b0b52-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-178"><strong>Fenster schließen</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-179"><strong>Objekttyp</strong>: <strong>Formularobjekt Name</strong>: Produktlisten <strong>Speicher</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-180">Schließen des Produktlistenformulars</span><span class="sxs-lookup"><span data-stu-id="b0b52-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-182"><strong>Formular Name</strong>: Produkt <strong>Ansicht</strong>: <strong>FormData Modus</strong>: <strong>addwindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-183">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="b0b52-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-184"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-185"><strong>Element</strong>: [Formulare]! [Products]! LieferantenNr <strong>Ausdruck</strong>: Lieferanten-Nr.</span><span class="sxs-lookup"><span data-stu-id="b0b52-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="b0b52-186">Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Formular Lieferanten fest.</span><span class="sxs-lookup"><span data-stu-id="b0b52-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-188"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="b0b52-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="b0b52-189">Wechseln Sie zum Steuerelement Category ID.</span><span class="sxs-lookup"><span data-stu-id="b0b52-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0b52-p116">Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0b52-p116">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="b0b52-194">**Synchronisieren von Formularen mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="b0b52-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b52-195">Bedingung</span><span class="sxs-lookup"><span data-stu-id="b0b52-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="b0b52-196">Aktion</span><span class="sxs-lookup"><span data-stu-id="b0b52-196">Action</span></span></p></th>
<th><p><span data-ttu-id="b0b52-197">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="b0b52-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b0b52-198">Kommentar</span><span class="sxs-lookup"><span data-stu-id="b0b52-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b0b52-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-200"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-201">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b0b52-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-202">IsNull ([Lieferanten-Nr.])</span><span class="sxs-lookup"><span data-stu-id="b0b52-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="b0b52-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-204"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="b0b52-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="b0b52-205"><strong>Beep</strong>: <strong>jatyp</strong>: <strong>Keinetitel</strong>: Wählen Sie einen Zulieferer aus</span><span class="sxs-lookup"><span data-stu-id="b0b52-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="b0b52-206">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="b0b52-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b52-207">...</span><span class="sxs-lookup"><span data-stu-id="b0b52-207"></span></span></p></td>
<td><p><span data-ttu-id="b0b52-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-209"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="b0b52-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="b0b52-210">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="b0b52-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b52-211">...</span><span class="sxs-lookup"><span data-stu-id="b0b52-211"></span></span></p></td>
<td><p><span data-ttu-id="b0b52-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b0b52-213">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="b0b52-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b0b52-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-215"><strong>Formularname</strong>: Produktlisten <strong>Ansicht</strong>: <strong>Datenblatt Filtername</strong>: <strong>Where Condition</strong>: [suppliercode] = [Forms]! [Lieferanten]! LieferantenNr <strong>Datenmodus</strong>: <strong>Lese-schreibgeschütztfenstermodus-Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-216">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="b0b52-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b0b52-217"><strong>Verschiebenundgrößeändernfenster</strong></span><span class="sxs-lookup"><span data-stu-id="b0b52-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b52-218"><strong>rechts</strong>: 0,7799&quot; <strong>unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="b0b52-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="b0b52-219">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="b0b52-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

