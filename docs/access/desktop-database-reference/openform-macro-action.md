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
# <a name="openform-macro-action"></a>OpenForm-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **OpenForm** -Aktion verwenden, um ein Formular in der Formularansicht, in der Entwurfsansicht, in der Seitenansicht oder in der Datenblatt Anzeige zu öffnen. Sie können den Dateneingabe- und den Fenstermodus für das Formular auswählen und die Datensätze einschränken, die das Formular anzeigt.

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
<td><p><strong>Formular Name</strong></p></td>
<td><p>Der Name des zu öffnenden Formulars. Im Feld <strong>Formular Name</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator werden alle Formulare in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, das <strong></strong> die OpenForm-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Formular mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Die Ansicht, in der das Formular geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Formular</strong>, <strong>Entwurf</strong>, <strong>Seiten</strong>Ansicht, <strong>Datenblatt</strong>, <strong>PivotTable</strong>oder <strong>PivotChart</strong> . Der Standardwert ist <strong>Form</strong>.</p><p><strong>Hinweis</strong>: die Einstellung für das Argument <STRONG>View</STRONG> setzt die Einstellungen der Eigenschaften <STRONG>DefaultView</STRONG> und <STRONG>ViewsAllowed</STRONG> des Formulars außer Kraft. Wenn beispielsweise die <STRONG>ViewsAllowed</STRONG> -Eigenschaft eines Formulars auf <STRONG>Datenblatt</STRONG>festgelegt ist, können Sie die <STRONG>OpenForm</STRONG> -Aktion verwenden, um das Formular in der Formularansicht zu öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Filter Name</strong></p></td>
<td><p>Ein Filter, der die Datensätze des Formulars einschränkt oder sortiert. Sie können den Namen einer vorhandenen Abfrage oder eines Filters, der als eine Abfrage gespeichert wurde, eingeben. Die Abfrage muss jedoch alle Felder in dem Formular enthalten, das Sie öffnen, oder die <strong>AlleFelderAusgeben</strong> -Eigenschaft ist auf <strong>Ja</strong>festgelegt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bedingung</strong></p></td>
<td><p>Eine gültige SQL-WHERE-Klausel (ohne das Wort WHERE) oder Expression, die Access zum Auswählen von Datensätzen aus der zugrunde liegenden Tabelle oder Abfrage des Formulars verwendet. Wenn Sie einen Filter mit dem Argument <strong>Filter Name</strong> auswählen, wendet Access diese WHERE-Klausel auf die Ergebnisse des Filters an. Verwenden Sie den folgenden Ausdruck, um ein Formular zu öffnen und seine Datensätze auf die zu beschränken, die durch den Wert eines Steuerelements in einem anderen Formular angegeben werden: <strong>[</strong><em>FieldName</em><strong>] = Forms! [</strong> <em>Formularname</em> <strong>]! [</strong><em>Steuerelementname in anderen Formularen</em><strong>]</strong> <em>FieldName</em> durch den Namen eines Felds in der zugrunde liegenden Tabelle oder Abfrage des zu öffnenden Formulars ersetzen. Ersetzen <em></em> Sie FormName und <em>Steuerelement</em> Name in einem anderen Formular durch den Namen des anderen Formulars und das Steuerelement auf dem anderen Formular, das den Wert enthält, den die Datensätze im ersten Formular übereinstimmen sollen.</p><p><strong>Hinweis</strong>: die maximale Länge des Arguments <STRONG>Where Condition</STRONG> beträgt 255 Zeichen. Wenn Sie eine komplexere SQL-WHERE-Klausel länger als diese eingeben müssen, verwenden <STRONG></STRONG> Sie stattdessen die OpenForm-Methode des <STRONG>DoCmd</STRONG> -Objekts in einem VBA-Modul (Visual Basic für Applikationen). Sie können SQL WHERE-Klauselanweisungen in VBA mit bis zu 32.768 Zeichen eingeben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenmodus</strong></p></td>
<td><p>Der Dateneingabemodus für das Formular. Dies gilt nur für Formulare, die in der Formularansicht oder in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht bearbeiten), auf <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue hinzufügen) oder auf <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>. <strong>Hinweise</strong></p>
<ul>
<li><p>Die Einstellung des <strong>Datenmodus</strong> -Arguments setzt die Einstellungen der Eigenschaften <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>und <strong>DataEntry</strong> des Formulars außer Kraft. Wenn die <strong>AllowEdits</strong> -Eigenschaft eines Formulars beispielsweise auf <strong>Nein</strong>festgelegt ist, können Sie die OpenForm-Aktion verwenden, um das Formular im Bearbeitungsmodus zu öffnen. <strong></strong></p></li>
<li><p>Wenn Sie dieses Argument leer lassen, öffnet Access das Formular im Dateneingabemodus, der von den <strong>AllowEdits</strong>-, <strong>AllowDeletions</strong>-, <strong>AllowAdditions</strong>-und <strong>DataEntry</strong> -Eigenschaften des Formulars festgelegt wird.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Window Mode</strong></p></td>
<td><p>Der Fenstermodus, in dem das Formular geöffnet wird. Klicken Sie auf <strong>Normal</strong> (das Formular wird in dem Modus geöffnet, der durch seine Eigenschaften festgelegt ist), <strong>ausgeblendet</strong> (das Formular ist ausgeblendet), <strong>Symbol</strong> (das Formular wird minimiert als kleine Titelleiste am unteren Rand des Bildschirms geöffnet) oder <strong>Dialog Feld</strong> (das Formular <strong>Modal</strong> und <strong>Popup </strong>Eigenschaften sind auf <strong>Ja</strong>festgelegt. Die Standardeinstellung ist <strong>Normal</strong>.</p><p><strong>Hinweis</strong>: einige Einstellungen im <STRONG>Fenstermodus</STRONG> -Argument gelten nicht bei der Verwendung von Registerkarten Dokumenten. So wechseln Sie zu überlappenden Fenstern:</p>
<ol>
<li><p>Klicken Sie auf die Registerkarte Datei und dann auf <strong>Optionen</strong>.</p></li>
<li><p>Klicken Sie im Dialogfeld <strong>Access-Optionen</strong> auf <strong>Aktuelle Datenbank</strong>.</p></li>
<li><p>Klicken Sie im Abschnitt <strong>Anwendungsoptionen</strong>unter <strong>dokumentfensterOptionen</strong>auf über <strong>Lapp Ende Fenster</strong>.</p></li>
<li><p>Klicken Sie auf <strong>OK</strong>, schließen Sie die Datenbank dann, und öffnen Sie sie erneut.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Diese Aktion ähnelt dem Doppelklicken auf ein Formular im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Formular im Navigationsbereich und dem Auswählen einer Ansicht.

Ein Formular kann modal sein (es muss geschlossen oder ausgeblendet werden, bevor der Benutzer eine andere Aktion ausführen kann) oder ohne Modus (der Benutzer kann zu anderen Fenstern wechseln, während das Formular geöffnet ist). Es kann auch ein Popupformular sein (ein Formular, mit dem Informationen gesammelt oder angezeigt werden, die über allen anderen Access-Fenstern liegen). Sie legen die Eigenschaften **Modal** und **Popup** beim Entwerfen des Formulars fest. Wenn Sie für das Argument **Window Mode** den **Standard** verwenden, wird das Formular in dem durch diese Eigenschafteneinstellungen angegebenen Modus geöffnet. Wenn Sie **Dialog** für das Argument **Window Mode** verwenden, werden diese Eigenschaften auf **Ja**festgelegt. Ein Formular, das als ausgeblendet oder als Symbol geöffnet wurde, wird beim Anzeigen oder Wiederherstellen des Modus zurückgegeben, der durch seine Eigenschafteneinstellungen angegeben wird.

Wenn Sie ein Formular öffnen, dessen **Fenstermodus** -Argument auf **Dialog**festgelegt ist, wird das Makro von Access angehalten, bis das Formular geschlossen oder ausgeblendet ist. Sie können ein Formular ausblenden, indem Sie die **Visible** -Eigenschaft mithilfe der SetValue-Aktion auf **Nein** festlegen. ****

> [!TIP]
> Sie können ein Formular im Navigationsbereich auswählen und in eine Makroaktionszeile ziehen. Dadurch wird automatisch eine **OpenForm** -Aktion erstellt, mit der das Formular in der Formularansicht geöffnet wird.

Der Filter und die WHERE-Bedingung, die Sie anwenden, werden zur Einstellung der **Filter** -Eigenschaft des Formulars.

## <a name="examples"></a>Beispiele

**Festlegen des Werts eines Steuerelements mithilfe eines Makros**

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert ** und **GeheZuSteuerelement**. Mit **** der SetValue-Aktion wird das Lieferanten-ID-Steuerelement im Formular Produkte auf den aktuellen Lieferanten im Formular Lieferanten festgelegt. Die **gotoCONTROL** -Aktion verschiebt dann den Fokus auf das Feld Kategorie-ID, in dem Sie mit der Eingabe von Daten für das neue Produkt beginnen können. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

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
<td><p><strong>Fenster schließen</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>Formularobjekt Name</strong>: Produktlisten <strong>Speicher</strong>: <strong>Nein</strong></p></td>
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formular Name</strong>: Produkt <strong>Ansicht</strong>: <strong>FormData Modus</strong>: <strong>addwindow Mode</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Element</strong>: [Formulare]! [Products]! LieferantenNr <strong>Ausdruck</strong>: Lieferanten-Nr.</p></td>
<td><p>Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Formular Lieferanten fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: CategoryID</p></td>
<td><p>Wechseln Sie zum Steuerelement Category ID.</p></td>
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
<td><p>IsNull ([Lieferanten-Nr.])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Beep</strong>: <strong>jatyp</strong>: <strong>Keinetitel</strong>: Wählen Sie einen Zulieferer aus</p></td>
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
<td><p><strong>Formularname</strong>: Produktlisten <strong>Ansicht</strong>: <strong>Datenblatt Filtername</strong>: <strong>Where Condition</strong>: [suppliercode] = [Forms]! [Lieferanten]! LieferantenNr <strong>Datenmodus</strong>: <strong>Lese-schreibgeschütztfenstermodus-Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Verschiebenundgrößeändernfenster</strong></p></td>
<td><p><strong>rechts</strong>: 0,7799&quot; <strong>unten</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

