---
title: OpenForm-Makroaktion
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1813a80c43eb77f8fb90442ecd6e0336b636191
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998973"
---
# <a name="openform-macro-action"></a>OpenForm-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **ÖffnenFormular** -Aktion zum Öffnen eines Formulars in der Formularansicht, Entwurfsansicht, Seitenansicht oder Datenblattansicht verwenden. Sie können den Dateneingabe- und den Fenstermodus für das Formular auswählen und die Datensätze einschränken, die das Formular anzeigt.

## <a name="setting"></a>Einstellung

Die **OpenForm** -Aktion hat die folgenden Argumente.

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
<td><p>Der Name der zu öffnenden Formulars. Das Feld <strong>Formularname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Formulare in der aktuellen Datenbank. Dies ist ein erforderliches Argument. Wenn Sie ein Makro mit der <strong>ÖffnenFormular</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst für das Formular mit diesem Namen in die Bibliotheksdatenbank, und klicken Sie dann in der aktuellen Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der das Formular geöffnet wird. Klicken Sie auf <strong>Formular</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>Datenblatt</strong>, <strong>PivotTable-</strong>oder <strong>PivotChart</strong> in das Feld <strong>Anzeigen</strong> . Der Standardwert ist <strong>Formular</strong>.</p><p><strong>Hinweis</strong>: die Einstellung des Arguments <STRONG>Ansicht</STRONG> setzt die Einstellungen der Eigenschaften für das Formular <STRONG>DefaultView</STRONG> und <STRONG>ViewsAllowed</STRONG> außer Kraft. Beispielsweise wenn <STRONG>ViewsAllowed</STRONG> -Eigenschaft eines Formulars auf <STRONG>Datenblatt</STRONG>festgelegt ist, können weiterhin die <STRONG>ÖffnenFormular</STRONG> -Aktion Sie das Formular in der Formularansicht geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Filter Name</strong></p></td>
<td><p>Ein Filter, der Datensätze des Formulars einschränkt oder sortiert. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben. Die Abfrage muss jedoch alle Felder enthalten, in der Form, die Sie öffnen oder dessen <strong>OutputAllFields</strong> -Eigenschaft auf <strong>Ja</strong>festgelegt haben.</p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Eine gültige SQL WHERE-Klausel (ohne das Wort, in dem) oder ein Ausdruck, der Zugriff verwendet, um Datensätze aus dem Formular zugrunde liegenden Tabelle oder Abfrage. Wenn Sie einen Filter mit dem Argument <strong>Filtername</strong> auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters. Wenn Sie ein Formular öffnen und seine Datensätze auf diejenigen angegeben durch den Wert eines Steuerelements in ein anderes Formular zu beschränken, verwenden Sie den folgenden Ausdruck: <strong>[</strong><em>Fieldname</em><strong>] = Formulare! [</strong> <em>Formularname</em> <strong>]! [</strong><em>Steuerelementname in anderem Formular</em><strong>]</strong> ersetzen <em>Fieldname</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des zu öffnenden Formulars. Ersetzen Sie <em>Formname</em> und <em>Steuerelementname in anderen Formular</em> mit dem Namen des anderen Formulars und das Steuerelement, Formular, das den Wert enthält, den Datensätze im ersten Formular übereinstimmen sollen.</p><p><strong>Hinweis</strong>: die maximale Länge des Arguments <STRONG>Bedingung</STRONG> beträgt 255 Zeichen. Wenn Sie eine komplexere SQL WHERE-Klausel eingeben müssen, verwenden Sie die <STRONG>OpenForm</STRONG> -Methode des <STRONG>DoCmd</STRONG> -Objekts in einem Visual Basic für Applikationen (VBA) Modul stattdessen. Sie können in VBA SQL WHERE-Klausel Anweisungen von bis zu 32.768 Zeichen eingeben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode</strong></p></td>
<td><p>Der Dateneingabemodus für das Formular. Dies gilt nur für Formulare, die in der Formularansicht oder in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>. <strong>Hinweise</strong></p>
<ul>
<li><p>Die Einstellung des Arguments <strong>Datenmodus</strong> setzt die Einstellungen der Eigenschaften für das Formular <strong>BearbeitungenZulassen</strong>, <strong>LöschenZulassen</strong>, <strong>AnfügenZulassen</strong>und <strong>DatenEingeben</strong> außer Kraft. Beispielsweise wenn <strong>AllowEdits</strong> -Eigenschaft eines Formulars auf <strong>Nein</strong>festgelegt ist, können weiterhin die <strong>ÖffnenFormular</strong> -Aktion Sie zum Öffnen des Formulars im Bearbeitungsmodus.</p></li>
<li><p>Wenn Sie dieses Argument leer lassen, öffnet Access das Formular in der Dateneingabemodus des Formulars <strong>BearbeitungenZulassen</strong>, <strong>LöschenZulassen</strong>, <strong>AnfügenZulassen</strong>und <strong>DatenEingeben</strong> Eigenschaften festgelegt.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Window Mode</strong></p></td>
<td><p>Der Fenstermodus, in dem das Formular wird geöffnet. Klicken Sie auf <strong>Normal</strong> (das Formular wird in den Modus durch seine Eigenschaften festgelegt), <strong>ausgeblendet</strong> (das Formular ist ausgeblendet), <strong>Symbol</strong> (das Formular wird als kleine Titelleiste am unteren Rand des Bildschirms geöffnet), oder ein <strong>Dialogfeld</strong> (des Formulars <strong>Modal</strong> und PopUp <strong> </strong>auf <strong>Ja</strong>festgelegt). Die Standardeinstellung ist <strong>Normal</strong>.</p><p><strong>Hinweis</strong>: Einige Einstellungen für das Argument <STRONG>Fenstermodus</STRONG> beim Verwenden von Dokumenten im Registerkartenformat nicht angewendet. So wechseln Sie zu überlappenden Fenstern:</p>
<ol>
<li><p>Klicken Sie auf der Registerkarte Datei, und klicken Sie dann auf <strong>Optionen</strong>.</p></li>
<li><p>Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</p></li>
<li><p>Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong>unter <strong>Dokumentfensteroptionen</strong>auf <strong>Überlappende Fenster</strong>.</p></li>
<li><p>Klicken Sie auf <strong>OK</strong>, schließen Sie die Datenbank dann, und öffnen Sie sie erneut.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion entspricht dem Doppelklicken auf ein Formular im Navigationsbereich oder der rechten Maustaste auf das Formular im Navigationsbereich und dann eine Ansicht auswählen.

Ein Formular ist Modal (es muss geschlossen oder ausgeblendet werden, bevor der Benutzer eine andere Aktion ausführen kann) oder ungebunden (der Benutzer kann zu anderen Fenstern wechseln, während das Formular geöffnet ist). Es kann auch ein Popup-Formular (ein Formular zum Sammeln oder Anzeigen von Informationen, die vor allen anderen Access-Fenster angezeigt) sein. Die Eigenschaften **Modal** und **PopUp** wird festgelegt, wenn Sie das Formular entwerfen. Wenn Sie für das Argument **Fenstermodus** **Normal** verwenden, öffnet sich das Formular im Modus durch diese Einstellungen angegeben sind. Wenn Sie das **Dialogfeld** für das Argument **Fenstermodus** verwenden, werden diese Eigenschaften beide auf **Ja**festgelegt. Als ausgeblendet oder als Symbol öffnen ein Formulars in den Modus durch seine Einstellungen angegeben werden, wenn Sie anzeigen oder Wiederherstellen zurückgegeben.

Beim Öffnen eines Formulars mit das Argument **Fenstermodus** auf **Dialog**festgelegt unterbricht Access das Makro aus, bis das Formular geschlossen oder ausgeblendet wird. Sie können ein Formular ausblenden, indem die **Visible** -Eigenschaft mithilfe der **SetzenWert** -Aktion auf **Nein** festlegen.

> [!TIP]
> Sie können ein Formular im Navigationsbereich auswählen und ziehen Sie ihn in einer Zeile der Makro-Aktion. Dadurch wird automatisch eine **ÖffnenFormular** -Aktion, die das Formular in der Formularansicht geöffnet wird erstellt.

Der Filter und die WHERE-Bedingung ergeben die Einstellung der **Filter** -Eigenschaft des Formulars.

## <a name="examples"></a>Beispiele

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Mit dem folgende Makro wird das Formular Artikel Hinzufügen einer Schaltfläche auf dem Formular Lieferanten geöffnet. Es wird die Verwendung der **Echo**, **CloseWindow**, **ÖffnenFormular**, **SetzenWert**und **GeheZuSteuerelement** -Aktionen. Die **SetzenWert** -Aktion wird das Steuerelement Lieferanten-ID auf dem Formular auf den aktuellen Lieferanten im Formular Suppliers angezeigt. Klicken Sie dann die **GeheZuSteuerelement** -Aktion verschiebt den Fokus auf das Feld Kategorie-ID, beginnen Sie können Daten für das neue Produkt eingeben. Dieses Makro sollte der Schaltfläche Artikel hinzufügen im Formular Lieferanten zugeordnet werden.

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
<td><p><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></p></td>
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>ÖffnenFormular</strong></p></td>
<td><p><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</p></td>
<td><p>Legen Sie das Steuerelement auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: CategoryID</p></td>
<td><p>Wechseln Sie auf die Kategorie-ID-Steuerelement.</p></td>
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
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</p></td>
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
<td><p><strong>Formularname</strong>: Produkt Liste <strong>Anzeigen</strong>: <strong>DatasheetFilter Name</strong>: <strong>Bedingung</strong>: [Lieferanten-Nr] = [Formulare]! [Lieferanten]! [Lieferanten-Nr] <strong>Datenmodus</strong>: <strong>OnlyWindow Lesemodus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Rechts</strong>: 0.7799&quot; <strong>nach unten</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

