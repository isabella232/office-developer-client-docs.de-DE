---
title: OpenForm-Makroaktion
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c45f71ed079badfaa6843b5a12734bb82a2e553a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611910"
---
# <a name="openform-macro-action"></a>OpenForm-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **ÖffnenFormular-Aktion** verwenden, um ein Formular in der Formularansicht, der Entwurfsansicht, der Seitenansicht oder der Datenblattansicht zu öffnen. Sie können den Dateneingabe- und den Fenstermodus für das Formular auswählen und die Datensätze einschränken, die das Formular anzeigt.

## <a name="setting"></a>Einstellung

Die **OpenForm-Aktion** hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Formularname</strong></p></td>
<td><p>Der Name des zu öffnenden Formulars. Im Feld <strong>Formularname</strong> im Abschnitt <strong>Aktionsargumente</strong> im Bereich Makro-Generator werden alle Formulare in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das die <strong>OpenForm-Aktion</strong> in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Formular mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der das Formular geöffnet wird. Klicken Sie im <strong>Ansichtsfeld</strong> auf <strong>Formular,</strong> <strong>Entwurf,</strong> <strong>Seitenansicht,</strong> <strong>Datenblatt,</strong> <strong>PivotTable</strong>oder <strong>PivotChart.</strong> Der Standardwert ist <strong>Form</strong>.</p><p><strong>HINWEIS:</strong>Die Einstellung des <STRONG>Arguments View</STRONG> überschreibt die Einstellungen der Eigenschaften <STRONG>DefaultView</STRONG> und <STRONG>ViewsAllowed</STRONG> des Formulars. Wenn z. B. die <STRONG>ViewsAllowed-Eigenschaft</STRONG> eines Formulars auf <STRONG>"Datenblatt"</STRONG>festgelegt ist, können Sie die <STRONG>ÖffnenFormular-Aktion</STRONG> weiterhin verwenden, um das Formular in der Formularansicht zu öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Filter Name</strong></p></td>
<td><p>Ein Filter, der die Datensätze des Formulars einschränkt oder sortiert. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben. Die Abfrage muss jedoch alle Felder in dem Formular enthalten, das Sie öffnen, oder die <strong>OutputAllFields-Eigenschaft</strong> muss auf <strong>"Ja"</strong>festgelegt sein.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bedingung</strong></p></td>
<td><p>Ein gültiger SQL WHERE-Klausel (ohne das Wort WHERE) oder ein Ausdruck, den Access verwendet, um Datensätze aus der dem Formular zugrunde liegenden Tabelle oder Abfrage auszuwählen. Wenn Sie einen Filter mit dem Argument <strong>Filter Name</strong> auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters an. Um ein Formular zu öffnen und seine Datensätze auf diejenigen zu beschränken, die durch den Wert eines Steuerelements in einem anderen Formular angegeben werden, verwenden Sie den folgenden Ausdruck: <strong>[</strong><em>Feldname</em><strong>] = Formulare![</strong> <em>Formname</em><strong>]! [</strong><em>Steuerelementname in einem anderen Formular</em><strong>]</strong> Ersetzen Sie <em>den Feldnamen</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des Formulars, das Sie öffnen möchten. Ersetzen Sie <em>den Formularnamen</em> und <em>den Steuerelementnamen in einem anderen Formular</em> durch den Namen des anderen Formulars und das Steuerelement auf dem anderen Formular, das den Wert enthält, mit dem Datensätze im ersten Formular übereinstimmen sollen.</p><p><strong>HINWEIS:</strong>Die maximale Länge des <STRONG>Where Condition-Arguments</STRONG> beträgt 255 Zeichen. Wenn Sie eine komplexere SQL WHERE-Klausel eingeben müssen, die länger als diese ist, verwenden Sie stattdessen die <STRONG>OpenForm-Methode</STRONG> des <STRONG>DoCmd-Objekts</STRONG> in einem Visual Basic for Applications (VBA)-Modul. Sie können SQL WHERE-Klauselanweisungen in VBA mit bis zu 32.768 Zeichen eingeben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für das Formular. Dies gilt nur für Formulare, die in der Formularansicht oder in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>. <strong>Hinweise</strong></p>
<ul>
<li><p>Die Einstellung des <strong>Datenmodusarguments</strong> überschreibt die Einstellungen der Eigenschaften <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>und <strong>DataEntry</strong> des Formulars. Wenn z. B. die <strong>AllowEdits-Eigenschaft</strong> eines Formulars auf <strong>"Nein"</strong>festgelegt ist, können Sie die <strong>OpenForm-Aktion</strong> weiterhin verwenden, um das Formular im Bearbeitungsmodus zu öffnen.</p></li>
<li><p>Wenn Sie dieses Argument leer lassen, öffnet Access das Formular im Dateneingabemodus, der durch die Eigenschaften <strong>AllowEdits,</strong> <strong>AllowDeletions,</strong> <strong>AllowAdditions</strong>und <strong>DataEntry</strong> des Formulars festgelegt wird.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Window Mode</strong></p></td>
<td><p>Der Fenstermodus, in dem das Formular geöffnet wird. Klicken Sie auf <strong>"Normal"</strong> (das Formular wird im Modus geöffnet, der durch seine Eigenschaften festgelegt ist), <strong>"Ausgeblendet"</strong> (das Formular ist ausgeblendet), <strong>auf "Symbol"</strong> (das Formular wird als kleine Titelleiste am unteren Rand des Bildschirms minimiert) oder <strong>auf "Dialog"</strong> (die Eigenschaften <strong>"Modal"</strong> und <strong>"PopUp"</strong> des Formulars sind auf <strong>"Ja"</strong>festgelegt). Die Standardeinstellung ist <strong>Normal</strong>.</p><p><strong>HINWEIS:</strong>Einige Einstellungen des <STRONG>Window Mode-Arguments</STRONG> gelten nicht, wenn Sie Dokumente mit Registerkarten verwenden. So wechseln Sie zu überlappenden Fenstern:</p>
<ol>
<li><p>Klicken Sie auf die Registerkarte "Datei", und klicken Sie dann auf <strong>"Optionen".</strong></p></li>
<li><p>Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</p></li>
<li><p>Klicken Sie im Abschnitt <strong>"Anwendungsoptionen"</strong>unter <strong>"Dokumentfensteroptionen"</strong>auf <strong>"Überlappende Windows".</strong></p></li>
<li><p>Klicken Sie auf <strong>OK</strong>, schließen Sie die Datenbank dann, und öffnen Sie sie erneut.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Diese Aktion ähnelt dem Doppelklicken auf ein Formular im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Formular im Navigationsbereich und dem anschließenden Auswählen einer Ansicht.

Ein Formular kann modal (es muss geschlossen oder ausgeblendet werden, bevor der Benutzer eine andere Aktion ausführen kann) oder moduslos sein (der Benutzer kann zu anderen Fenstern wechseln, während das Formular geöffnet ist). Es kann auch ein Popupformular sein (ein Formular zum Sammeln oder Anzeigen von Informationen, die auf allen anderen Access-Fenstern verbleiben). Sie legen die **Modal-** und **PopUp-Eigenschaften** fest, wenn Sie das Formular entwerfen. Wenn Sie **"Normal"** für das **Argument "Fenstermodus"** verwenden, wird das Formular in dem durch diese Eigenschafteneinstellungen angegebenen Modus geöffnet. Wenn Sie **dialog** for the **Window Mode** argument, these properties are both set to **Yes**. Ein formular, das als ausgeblendet oder als Symbol geöffnet wird, kehrt zum Modus zurück, der durch die Eigenschafteneinstellungen angegeben wird, wenn Sie es anzeigen oder wiederherstellen.

Wenn Sie ein Formular öffnen, für das das Argument **Fenstermodus** auf **Dialog** festgelegt ist, wird das Makro von Access angehalten, bis das Formular geschlossen oder ausgeblendet wird. Sie können ein Formular ausblenden, indem Sie seine **Visible-Eigenschaft** mithilfe der **SetValue-Aktion** auf **"Nein"** festlegen.

> [!TIP]
> Sie können ein Formular im Navigationsbereich auswählen und in eine Aktionszeile eines Makros ziehen. Dadurch wird automatisch eine **OpenForm-Aktion** erstellt, die das Formular in der Formularansicht öffnet.

Die angewendete Filter- und WHERE-Bedingung wird zur Einstellung der **Filter-Eigenschaft** des Formulars.

## <a name="examples"></a>Beispiele

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert** und **GeheZuSteuerelement**. Die Aktion **"SetValue"** legt das Lieferanten-ID-Steuerelement im Formular "Produkte" auf den aktuellen Lieferanten im Lieferantenformular fest. Die **GoToControl-Aktion** verschiebt dann den Fokus auf das Feld Kategorie-ID, in das Sie beginnen können, Daten für das neue Produkt einzugeben. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo</strong>: <strong>Nein</strong></p></td>
<td><p>Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</p></td>
</tr>
<tr class="even">
<td><p><strong>FensterSchließen</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>FormularObjektname</strong>: Produktliste <strong>Speichern</strong>: <strong>Nein</strong></p></td>
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Ansicht</strong>: <strong>FormData-Modus</strong>: <strong>AddWindow-Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</p></td>
<td><p>Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Lieferantenformular fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: KategorieID</p></td>
<td><p>Wechseln Sie zum Kategorie-ID-Steuerelement.</p></td>
</tr>
</tbody>
</table>


Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.

**Synchronisieren von Formularen mithilfe eines Makros**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo</strong>: <strong>Nein</strong></p></td>
<td><p>Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Einen Lieferanten auswählen</p></td>
<td><p>Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: Firma</p></td>
<td><p>Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Halten Sie das Makro an.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formularname</strong>: <strong>Produktlistenansicht</strong>: <strong>DatasheetFilter-Name:</strong> <strong>Bedingung:</strong>[SupplierID] = [Formulare]! [Lieferanten]! [SupplierID] <strong>Datenmodus:</strong> <strong>Schreibgeschützter Fenstermodus:</strong> <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Rechts</strong>: 0,7799 &quot; <strong>Abwärts</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

