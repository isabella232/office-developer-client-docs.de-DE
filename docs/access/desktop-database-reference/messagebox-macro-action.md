---
title: MessageBox Macro Action
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6654d2994b472ff2d495b60fffd5fcdbd6e58089
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885234"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="233ee-102">MessageBox Macro Action</span><span class="sxs-lookup"><span data-stu-id="233ee-102">MessageBox Macro Action</span></span>


<span data-ttu-id="233ee-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="233ee-103">**Applies to**: Access 2013, Office 2013</span></span>




<span data-ttu-id="233ee-p101">Sie können die **MessageBox** -Aktion verwenden, um ein Nachrichtenfeld mit einer Warnung oder einer Informationsmeldung anzuzeigen. Sie können die **MessageBox** -Aktion beispielsweise mit Validierungsmakros verwenden. Wenn bei einem Steuerelement oder einem Datensatz ein Fehler bezüglich einer Überprüfungsbedingung im Makro auftritt, können eine Fehlermeldung in einem Nachrichtenfeld angezeigt und Anweisungen zu der Art von Daten gegeben werden, die eingegeben werden sollten.</span><span class="sxs-lookup"><span data-stu-id="233ee-p101">You can use the **MessageBox** action to display a message box containing a warning or an informational message. For example, you can use the **MessageBox** action with validation macros. When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="233ee-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="233ee-107">Setting</span></span>

<span data-ttu-id="233ee-108">Die **MessageBox** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="233ee-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="233ee-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="233ee-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="233ee-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="233ee-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="233ee-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-p102">Der Text im Nachrichtenfeld. Geben Sie den Nachrichtentext in das Feld <strong>Nachricht</strong> im Abschnitt <strong>Aktionsargumente</strong> des Makro-Generators ein. Sie können bis zu 255 Zeichen oder einen Ausdruck (mit einem vorangestellten Gleichheitszeichen) eingeben.  </span><span class="sxs-lookup"><span data-stu-id="233ee-p102">The text in the message box. Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-p103">Gibt an, ob aus dem Lautsprecher des Computers ein Signalton ertönt, wenn die Meldung angezeigt wird. Klicken Sie auf <strong>Ja</strong> (Signalton abspielen) oder <strong>Nein</strong> (Signalton nicht abspielen). Die Standardeinstellung ist <strong>Ja</strong>.  </span><span class="sxs-lookup"><span data-stu-id="233ee-p103">Specifies whether your computer's speaker sounds a beep tone when the message displays. Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233ee-119"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-p104">Der Typ des Nachrichtenfelds. Jeder Typ weist ein anderes Symbol auf. Klicken Sie auf <strong>Keiner</strong>, <strong>Kritisch</strong>, <strong>Warnung?</strong>, <strong>Warnung!</strong>, oder <strong>Information</strong>. Der Standardwert lautet <strong>Keine</strong>.  </span><span class="sxs-lookup"><span data-stu-id="233ee-p104">The type of message box. Each type has a different icon. Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>. The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-124"><strong>Title</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-125">Der in der Titelleiste des Nachrichtfelds angezeigte Text.</span><span class="sxs-lookup"><span data-stu-id="233ee-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="233ee-126">Sie können beispielsweise die Anzeige der Titel haben &quot;Kundennummer&quot;.</span><span class="sxs-lookup"><span data-stu-id="233ee-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="233ee-127">Wenn Sie dieses Argument leer lassen &quot;Microsoft Access&quot; wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="233ee-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="233ee-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="233ee-128">Remarks</span></span>

<span data-ttu-id="233ee-p106">Sie können die **MessageBox** -Aktion verwenden, um eine formatierte Fehlermeldung zu erstellen, ähnlich wie integrierte Meldungen, die von Microsoft Access angezeigt werden. Mit der **MessageBox** -Aktion können Sie eine Nachricht in drei Abschnitten für das Message-Argument bereitstellen. Trennen Sie die Abschnitte mit dem "@"-Zeichen voneinander.</span><span class="sxs-lookup"><span data-stu-id="233ee-p106">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access. The **MessageBox** action permits you to supply a message in three sections for the Message argument. You separate the sections with the "@" character.</span></span>

<span data-ttu-id="233ee-p107">Das folgende Beispiel zeigt ein formatiertes Meldungsfeld mit einer unterteilten Meldung. Der erste Textabschnitt in der Nachricht wird als fett formatierte Überschrift angezeigt. Der zweite Abschnitt wird als reiner Text unterhalb dieser Überschrift angezeigt. Der dritte Abschnitt wird als reiner Textt unter dem zweiten Abschnitt mit einer leeren Zeile dazwischen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="233ee-p107">The following example displays a formatted message box with a sectioned message. The first section of text in the message is displayed as a bold heading. The second section is displayed as plain text beneath that heading. The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="233ee-136">Geben Sie die folgende Zeichenfolge in das **Message** -Argument ein:</span><span class="sxs-lookup"><span data-stu-id="233ee-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="233ee-137">**Falsche Schaltfläche\!@This Schaltfläche nicht work.@Try eine andere.**</span><span class="sxs-lookup"><span data-stu-id="233ee-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="233ee-p108">Die **MessageBox** -Aktion kann nicht in einem VBA-Modul (Visual Basic für Applikationen) ausgeführt werden. Verwenden Sie stattdessen die **Msg** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="233ee-p108">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module. Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="233ee-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="233ee-140">Examples</span></span>

<span data-ttu-id="233ee-141">**Synchronisieren von Formularen mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="233ee-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="233ee-p109">Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="233ee-p109">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="233ee-146">Bedingung</span><span class="sxs-lookup"><span data-stu-id="233ee-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="233ee-147">Aktion</span><span class="sxs-lookup"><span data-stu-id="233ee-147">Action</span></span></p></th>
<th><p><span data-ttu-id="233ee-148">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="233ee-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="233ee-149">Kommentar</span><span class="sxs-lookup"><span data-stu-id="233ee-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="233ee-150"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-151"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-152">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="233ee-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="233ee-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="233ee-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-155"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="233ee-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="233ee-156"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</span><span class="sxs-lookup"><span data-stu-id="233ee-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="233ee-157">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="233ee-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233ee-158">...</span><span class="sxs-lookup"><span data-stu-id="233ee-158"></span></span></p></td>
<td><p><span data-ttu-id="233ee-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-160"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="233ee-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="233ee-161">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="233ee-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-162">...</span><span class="sxs-lookup"><span data-stu-id="233ee-162"></span></span></p></td>
<td><p><span data-ttu-id="233ee-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="233ee-164">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="233ee-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="233ee-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-166"><strong>Formularname</strong>: Produkt Liste <strong>Anzeigen</strong>: <strong>DatasheetFilter Name</strong>: <strong>Bedingung</strong>: [Lieferanten-Nr] = [Formulare]! [Lieferanten]! [Lieferanten-Nr] <strong>Datenmodus</strong>: <strong>OnlyWindow Lesemodus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-167">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="233ee-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="233ee-168"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-169"><strong>Rechts</strong>: 0.7799&quot; <strong>nach unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="233ee-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="233ee-170">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="233ee-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="233ee-171">\*\* Überprüfen der Gültigkeit von Daten mithilfe eines Makros\*\*</span><span class="sxs-lookup"><span data-stu-id="233ee-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="233ee-p111">Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden. Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**. Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden. Wenn die Postleitzahl nicht das richtige Format für das Land oder die Region aufweist, wird vom Makro ein Meldungsfeld angezeigt, und das Speichern des Datensatzes wird abgebrochen. Sie kehren dann zum PostalCode-Steuerelement zurück, in dem Sie den Fehler korrigieren können. Dieses Makro sollte mit der **BeforeUpdate** -Eigenschaft des Lieferantenformulars verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="233ee-p111">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the PostalCode control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="233ee-178">Bedingung</span><span class="sxs-lookup"><span data-stu-id="233ee-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="233ee-179">Aktion</span><span class="sxs-lookup"><span data-stu-id="233ee-179">Action</span></span></p></th>
<th><p><span data-ttu-id="233ee-180">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="233ee-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="233ee-181">Kommentar</span><span class="sxs-lookup"><span data-stu-id="233ee-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="233ee-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="233ee-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="233ee-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="233ee-184">Wenn „Land/Region" den Wert <strong>Null</strong> hat, kann die Postleitzahl nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="233ee-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-185">[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Länge([Postleitzahl]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="233ee-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="233ee-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-187"><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="233ee-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="233ee-188"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="233ee-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="233ee-189">Zeigt eine Meldung an, wenn die Postleitzahl nicht 5 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="233ee-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233ee-190">...</span><span class="sxs-lookup"><span data-stu-id="233ee-190"></span></span></p></td>
<td><p><span data-ttu-id="233ee-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="233ee-192">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="233ee-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="233ee-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-194"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="233ee-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233ee-195">[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Länge([Postleitzahl]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="233ee-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="233ee-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-197"><strong>Message</strong>: Die Postleitzahl muss 4 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="233ee-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="233ee-198"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="233ee-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="233ee-199">Zeigt eine Meldung an, wenn die Postleitzahl nicht 4 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="233ee-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-200">...</span><span class="sxs-lookup"><span data-stu-id="233ee-200"></span></span></p></td>
<td><p><span data-ttu-id="233ee-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="233ee-202">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="233ee-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="233ee-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-204"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="233ee-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="233ee-205">([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="233ee-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="233ee-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="233ee-207"><strong>Meldung</strong>: Die Postleitzahl ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="233ee-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="233ee-208">Beispiel für kanadische Postleitzahl: H1J 1 c 3 <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: PLZ Codefehler</span><span class="sxs-lookup"><span data-stu-id="233ee-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="233ee-p115">Zeigt eine Meldung an, wenn eine für Kanada ungültige Postleitzahl angegeben wird. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</span><span class="sxs-lookup"><span data-stu-id="233ee-p115">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="233ee-211">...</span><span class="sxs-lookup"><span data-stu-id="233ee-211"></span></span></p></td>
<td><p><span data-ttu-id="233ee-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="233ee-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="233ee-213">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="233ee-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

