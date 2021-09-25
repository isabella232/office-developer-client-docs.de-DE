---
title: Echo-Makroaktion (Access-Desktopdatenbankreferenz)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 31e0ce1af8a4943d97197470b13bec3236a80292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615578"
---
# <a name="echo-macro-action"></a>Echo-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **Echo-Aktion** können Sie angeben, ob echo aktiviert ist. Sie können diese Aktion beispielsweise verwenden, um die Ergebnisse eines Makros auszublenden oder anzuzeigen, während es ausgeführt wird.

## <a name="setting"></a>Einstellung

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.

Die **Echo-Aktion** hat die folgenden Argumente.

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
<td><p><strong>Echo einschalten</strong></p></td>
<td><p>Klicken Sie im Feld <strong>"Echo</strong> ein" im Abschnitt <strong>"Aktionsargumente"</strong> des Bereichs "Makro-Generator" auf <strong>"Ja"</strong> (Echo einschalten) oder <strong>"Nein"</strong> (Echo deaktivieren). Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Statusleistentext</strong></p></td>
<td><p>Der Text, der in der Statusleiste angezeigt werden soll, wenn das Echo deaktiviert ist. Wenn echo beispielsweise deaktiviert ist, kann die Statusleiste das &quot; Makro anzeigen, das ausgeführt wird.&quot;</p></td>
</tr>
</tbody>
</table>


Wenn ein Makro ausgeführt wird, werden bei der Bildschirmaktualisierung häufig Informationen angezeigt, die für die Funktionsweise des Makros nicht wesentlich sind. Wenn Sie das Argument **Echo On auf** **"Nein"** festlegen, wird das Makro ausgeführt, ohne den Bildschirm zu aktualisieren. Wenn das Makro abgeschlossen ist, aktiviert Access automatisch das Echo wieder und aktualisiert das Fenster. Die Einstellung **"No"** für das Argument **"Echo On"** wirkt sich nicht auf die Funktionalität des Makros oder dessen Ergebnisse aus.

Die **Echo-Aktion** unterdrückt nicht die Anzeige modaler Dialogfelder, z. B. Fehlermeldungen oder Popupformulare, z. B. Eigenschaftenblätter. Sie können Dialogfelder und Popupformulare verwenden, um Informationen zu sammeln oder anzuzeigen, auch wenn das Echo deaktiviert ist. Verwenden Sie die Aktion **"Warnmeldungen",** um alle Meldungs- oder Dialogfelder außer Fehlermeldungen und Dialogfeldern zu unterdrücken, in denen der Benutzer Informationen eingeben muss.

Sie können die **Echo-Aktion** mehrmals in einem Makro ausführen. Auf diese Weise können Sie den Statusleistentext ändern, während das Makro ausgeführt wird.

Wenn Sie das Echo deaktivieren, können Sie die **DisplayHourglassPointer-Aktion** verwenden, um den Mauszeiger in ein Sanduhrsymbol (oder ein beliebiges Mauszeigersymbol, das Sie für "Beschäftigt" festgelegt haben) zu ändern, um einen visuellen Hinweis darauf bereitzustellen, dass das Makro ausgeführt wird.

Verwenden Sie die Echo-Methode des **DoCmd-Objekts,** um die **Echo-Aktion** in einem Visual Basic for Applications (VBA)-Modul auszuführen. 

## <a name="examples"></a>Beispiele

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Festlegen des Werts eines Steuerelements mithilfe eines Makros

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


### <a name="synchronize-forms-by-using-a-macro"></a>Synchronisieren von Formularen mithilfe eines Makros

Mit dem folgenden Makro wird das Formular "Produktliste" in der unteren rechten Ecke des Formulars "Lieferanten" geöffnet, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.

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
<td><p>IsNull([Supplier ID])</p></td>
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
<td><p><strong>Formularname</strong>: <strong>Produktlistenansicht</strong>: <strong>DatasheetFilter-Name:</strong> <strong>Bedingung:</strong>[Lieferanten-ID] = [Formulare]! [Lieferanten]! [SupplierID] <strong>Datenmodus:</strong> <strong>Schreibgeschützter Fenstermodus:</strong> <strong>Normal</strong></p></td>
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

