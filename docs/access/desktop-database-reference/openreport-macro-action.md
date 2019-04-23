---
title: OpenReport-Makroaktion
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288350"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="b4e75-102">OpenReport-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="b4e75-102">OpenReport macro action</span></span>

<span data-ttu-id="b4e75-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4e75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4e75-p101">Sie können die **ÖffnenBericht**-Aktion verwenden, um einen Bericht in der Entwurfsansicht oder in der Seitenansicht zu öffnen oder den Bericht direkt an den Drucker zu senden. Sie können die im Bericht gedruckten Datensätze außerdem einschränken.</span><span class="sxs-lookup"><span data-stu-id="b4e75-p101">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer. You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="b4e75-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b4e75-106">Setting</span></span>

<span data-ttu-id="b4e75-107">Die **ÖffnenBericht**-Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b4e75-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4e75-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="b4e75-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b4e75-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4e75-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4e75-110">Berichtname</span><span class="sxs-lookup"><span data-stu-id="b4e75-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="b4e75-111">Der Name des zu öffnenden Berichts.</span><span class="sxs-lookup"><span data-stu-id="b4e75-111">The name of the report to open.</span></span> <span data-ttu-id="b4e75-112">Im Feld <strong>Berichtsname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> werden alle Berichte angezeigt, die in der aktuellen Datenbank enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4e75-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="b4e75-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="b4e75-113">This is a required argument.</span></span> <span data-ttu-id="b4e75-114">Wenn Sie ein Makro ausführen, das die Aktion OpenReport in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach dem Bericht mit diesem Namen und anschließend in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b4e75-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4e75-115">Ansicht</span><span class="sxs-lookup"><span data-stu-id="b4e75-115">View</span></span></p></td>
<td><p><span data-ttu-id="b4e75-p103">Die Ansicht, in der der Bericht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Drucken</strong> (Bericht wird sofort gedruckt), <strong>Entwurf</strong> oder <strong>Seitenansicht</strong>. Die Standardeinstellung ist <strong>Drucken</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-p103">The view in which the report will open. Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box. The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4e75-119">Filtername</span><span class="sxs-lookup"><span data-stu-id="b4e75-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="b4e75-p104">Ein Filter, der die Datensätze des Berichts einschränkt. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben. Die Abfrage muss jedoch alle Felder in dem Bericht enthalten, den Sie öffnen, oder die <strong>AlleFelderAusgeben</strong>-Eigenschaft muss auf <strong>Ja</strong> festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b4e75-p104">A filter that restricts the report's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4e75-123">Bedingung</span><span class="sxs-lookup"><span data-stu-id="b4e75-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="b4e75-124">Eine gültige SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, den Access zur Auswahl der Datensätze der dem Bericht zugrunde liegenden Tabelle oder Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4e75-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="b4e75-125">Wenn Sie einen Filter mit dem Argument Filter Name auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters an.</span><span class="sxs-lookup"><span data-stu-id="b4e75-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="b4e75-126">Verwenden Sie den folgenden Ausdruck, um einen Bericht zu öffnen und seine Datensätze auf die durch den Wert eines Steuerelements in einem Formular angegebenen zu beschränken:</span><span class="sxs-lookup"><span data-stu-id="b4e75-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="b4e75-127">
<strong>[</strong><em>FieldName</em><strong>] = Formulare! [</strong><em>Formularname</em><strong>]! [</strong><em>Steuer Elementname im Formular</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="b4e75-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="b4e75-128">Ersetzen <em></em> Sie fieldName durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des zu öffnenden Berichts.</span><span class="sxs-lookup"><span data-stu-id="b4e75-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="b4e75-129">Ersetzen Sie <em>Formularname</em> und <em>Steuerelementname im Formular</em> durch den Namen des Formulars und das Steuerelement in dem Formular, das den Wert enthält, mit dem die Datensätze in dem Bericht übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="b4e75-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="b4e75-130"><b>Hinweis</b>: die maximale Länge des Arguments WHERE Condition beträgt 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b4e75-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="b4e75-131">Wenn Sie eine komplexere SQL WHERE-Klausel eingeben müssen, die mehr als 255 Zeichen umfasst, verwenden Sie stattdessen die <b>OpenForm</b>-Methode des <b>DoCmd</b>-Objekts in einem VBA-Modul (Visual Basic für Applikationen).</span><span class="sxs-lookup"><span data-stu-id="b4e75-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="b4e75-132">Sie können SQL WHERE-Klauselanweisungen in VBA mit bis zu 32.768 Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="b4e75-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4e75-133">Window Mode</span><span class="sxs-lookup"><span data-stu-id="b4e75-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="b4e75-134">Der Modus, in dem der Bericht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b4e75-134">The mode in which the report will open.</span></span> <span data-ttu-id="b4e75-135">Klicken Sie im Feld <strong>Fenstermodus</strong> auf <strong>Normal</strong>, auf <strong>Ausgeblendet</strong>, auf <strong>Symbol</strong> oder auf <strong>Dialogfeld</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="b4e75-136">Die Standardeinstellung ist <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="b4e75-137"><b>Hinweis</b>: einige Einstellungen im Fenstermodus-Argument gelten nicht bei der Verwendung von Registerkarten Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="b4e75-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="b4e75-138">So wechseln Sie zu überlappenden Fenstern:</span><span class="sxs-lookup"><span data-stu-id="b4e75-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="b4e75-139">Klicken Sie auf <strong>Optionen</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b4e75-140">Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b4e75-141">Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong> unter <strong>Dokumentfensteroptionen</strong> auf <strong>Überlappende Fenster</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4e75-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b4e75-142">Klicken Sie auf <strong>OK</strong>, und schließen Sie die Datenbank, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="b4e75-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4e75-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4e75-143">Remarks</span></span>

<span data-ttu-id="b4e75-144">Die Einstellung **Drucken** des Arguments **Ansicht** druckt sofort den Bericht mit den aktuellen Druckereinstellungen, ohne dass das Dialogfeld **Drucken** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b4e75-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="b4e75-145">Sie können auch die Aktion **ÖffnenBericht** verwenden, um einen Bericht zu öffnen und einzurichten, und dann die Aktion PrintOut zum Drucken verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4e75-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="b4e75-146">Dies empfiehlt sich beispielsweise, wenn Sie den Bericht vor dem Drucken ändern oder die Aktion **PrintOut** zum Ändern der Druckereinstellungen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b4e75-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="b4e75-147">Der von Ihnen angewendete Filter sowie die WHERE-Bedingung ergeben die Einstellung der Berichtseigenschaft **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b4e75-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="b4e75-148">Die **ÖffnenBericht**-Aktion ist mit dem Doppelklicken auf den Bericht im Navigationsbereich, mit dem Klicken auf den Bericht im Navigationsbereich mit der rechten Maustaste und mit dem Auswählen einer Ansicht oder des Befehls **Drucken** vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="b4e75-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="b4e75-149">Verwenden Sie zum Drucken ähnlicher Berichte für verschiedene Datensätze einen Filter oder eine WHERE-Klausel, um die im Bericht gedruckten Datensätze einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="b4e75-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="b4e75-150">Bearbeiten Sie das Makro dann, um einen anderen Filter anzuwenden oder das Argument Where Condition zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b4e75-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="b4e75-p112">Sie können einen Bericht aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenBericht**-Aktion erstellt, die den Bericht in der Berichtsansicht öffnet.</span><span class="sxs-lookup"><span data-stu-id="b4e75-p112">You can drag a report from the Navigation Pane to a macro action row. This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="b4e75-153">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4e75-153">Example</span></span>

<span data-ttu-id="b4e75-154">Im folgenden Beispiel wird erläutert, wie die Aktion OpenReport verwendet werden kann, um einen Parameter zu übergeben, der einen geöffneten Bericht filtert.</span><span class="sxs-lookup"><span data-stu-id="b4e75-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="b4e75-155">Der Bericht **rptChapters** zeigt die Datensätze für den angegebenen Autor an, indem das ausgewählte Element im Kombinationsfeld **cboAuthors** an den Parameter SelectedAuthor übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4e75-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="b4e75-156">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b4e75-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
